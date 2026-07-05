# Heroes Contest

Taktyczna gra strategiczna 2D łącząca mechaniki **Might & Magic Heroes 3** z systemem **heksagonalnych pól Civilization 3/7**.

## 🎮 Cechy MVP

### System Mapy
- ✅ **Mapa heksagonalna** (Civ-style) o zmiennych rozmiarach
- ✅ **Krawędź mapy** (outer boundary) - granice otaczające krainę
- ✅ **Obiekty terenu** - kamienie, ruiny, monolity
- ✅ **Zwoje teleportujące** - portale do szybkiego poruszania
- ✅ **Elementy dynamiczne** - stworzenia się poruszają po mapie

### Bohaterowie & Stworzenia
- ✅ **4 klasy bohaterów** - Warrior, Mage, Ranger, Paladin
- ✅ **Bestiariusz** - 25+ typów stworzeń w 5 tierach
- ✅ **System armii** - rekrutacja i zarządzanie jednostkami
- ✅ **Statystyki** - HP, Mana, Attack, Defense, Magic Power, Speed

### System Walki
- ✅ **Turowa mechanika** - kolejność tur oparta na Speed
- ✅ **Obliczenia obrażeń** - uwzględniające Defense i resistancje
- ✅ **System many** - stworzenia kosztują manę do rzucania
- ✅ **Leczenie & Bufory** - wsparcie taktyczne

### Magia & Przedmioty
- ✅ **35+ czarów** - 5 szkół magii (Evocation, Abjuration, Restoration, Transmutation, Necromancy)
- ✅ **Przedmioty** - bronie, zbroje, artefakty
- ✅ **Rzadkości** - Common, Uncommon, Rare, Epic, Legendary
- ✅ **Bonusy statystyczne** - do wszystkich atrybutów

### Tryb Gry
- ✅ **Kilka scenariuszy** - misje z różnym poziomem trudności
- ✅ **UI podstawowy** - log walki, informacje o bohaterach
- ✅ **System złota** - ekonomia gry
- ✅ **Postęp** - doświadczenie i level-upy

## 📁 Struktura Projektu

```
heros-contest/
├── scenes/
│   ├── main.tscn                    # Główna scena gry
│   ├── map/
│   │   ├── hex_grid.tscn
│   │   ├── map_renderer.tscn
│   │   └── terrain_objects.tscn
│   ├── characters/
│   │   ├── hero.tscn
│   │   ├── creature.tscn
│   │   └── creature_sprite.tscn
│   ├── ui/
│   │   ├── hud.tscn
│   │   ├── combat_log.tscn
│   │   ├── hero_panel.tscn
│   │   └── spell_menu.tscn
│   └── battle/
│       ├── battle_scene.tscn
│       └── combat_ui.tscn
├── scripts/
│   ├── core/
│   │   ├── hex_grid.gd              # System heksagonalny
│   │   ├── map_manager.gd           # Zarządzanie mapą
│   │   ├── movement_system.gd       # Ruch po mapie
│   │   └── pathfinding.gd           # Algorytm ścieżki
│   ├── entities/
│   │   ├── character.gd             # Klasa bazowa
│   │   ├── hero.gd                  # Bohater gracza
│   │   ├── creature.gd              # Stworzenie
│   │   ├── spell.gd                 # System czarów
│   │   └── item.gd                  # Przedmioty
│   ├── managers/
│   │   ├── game_manager.gd          # Zarządzanie grą
│   │   ├── combat_manager.gd        # Zarządzanie walką
│   │   ├── ui_manager.gd            # Zarządzanie UI
│   │   └── scenario_manager.gd      # Zarządzanie scenariuszami
│   ├── map/
│   │   ├── terrain_object.gd        # Kamienie, ruiny, etc
│   │   ├── teleport_scroll.gd       # Zwoje teleportujące
│   │   ├── boundary.gd              # Krawędź mapy
│   │   └── map_generator.gd         # Generacja mapy
│   └── ui/
│       ├── game_ui.gd
│       ├── combat_log.gd
│       └── hero_panel.gd
├── assets/
│   ├── sprites/
│   │   ├── heroes/                  # Porterty bohaterów (Heroes 3 style)
│   │   ├── creatures/               # Sprite'y stworzeń
│   │   ├── terrain/                 # Tereny heksów
│   │   ├── objects/                 # Kamienie, ruiny, portale
│   │   └── ui/                      # Elementy interfejsu
│   ├── sounds/
│   │   ├── ambient/
│   │   ├── spells/
│   │   └── ui/
│   └── data/
│       ├── creatures.json           # Bestiariusz
│       ├── spells.json              # Czary
│       ├── items.json               # Przedmioty
│       └── scenarios.json           # Scenariusze
├── project.godot
├── README.md
└── .gitignore
```

## 🚀 Instrukcja Uruchomienia

1. **Pobierz Godot 4.x** - https://godotengine.org/download
2. **Sklonuj repo**: `git clone https://github.com/Git7311520/heros-contest.git`
3. **Otwórz w Godot** - Import projektu
4. **Uruchom** - Naciśnij `F5`

## ⌨️ Sterowanie

| Przycisk | Akcja |
|----------|-------|
| **LPM** | Zaznacz pole/akcja |
| **PPM** | Anuluj |
| **Space** | Zakończ turę |
| **ESC** | Menu |
| **A** | Pokaż zaatakowane pola |
| **S** | Pokaż zasięg zaklęcia |

## 🎨 Inspiracja Wizualna

- **Heroes 3** - Styl grafiki, animacje, interfejs
- **HoTA (Heroes 3: Horn of the Abyss)** - Rozszerzone bestiary i czary
- **Civ 3/7** - System heksagonalnych pól, logika turowa

## 📊 Balans Gry

Stworzenia podzielone na **5 tierów**, każdy mocniejszy i droższy:
- **Tier 1** - Goblin, Sprite (50-60 gold)
- **Tier 2** - Orc, Wolf (140-150 gold)
- **Tier 3** - Ogre, Dragon (300-800 gold)
- **Tier 4** - Demon, Phoenix (700-750 gold, Epic)
- **Tier 5** - Titan, Hydra (950-1000 gold, Epic)

## 🔮 Czary (35+)

**Evocation (Atakowe):**
- Magic Missile, Fireball, Chain Lightning, Inferno, Lightning Bolt, itp.

**Abjuration (Ochronne):**
- Shield, Protection Circle, Mirror Image, itp.

**Restoration (Leczenie):**
- Cure Wounds, Greater Heal, Mass Heal, itp.

**Transmutation (Transmutacja):**
- Haste, Slow, Polymorph, itp.

**Necromancy (Nekromancja):**
- Summon Skeleton, Drain Life, Wither, itp.

## 📈 Rozwój

- [ ] Artefakty epiczne
- [ ] Więcej scenariuszy
- [ ] Kampania narracyjna
- [ ] Multiplayer
- [ ] Custom mapy

## 📜 Licencja

MIT License - Używaj i modyfikuj swobodnie!

---

**Stworzono z ❤️ dla fanów Heroes 3 i taktycznych gier strategicznych**
