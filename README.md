# Archive

A taxonomy system for organizing ~10TB of personal files. Designed not for perfect retrieval, but to shape attention and invite discovery.

## Philosophy

This archive is built on several core principles:

1. **Taxonomy over Ontology** - Folders answer "where should this live so it can be encountered?" not "what is this thing truly?" The structure is a usable map, not a perfect model of reality.

2. **Browsing over Querying** - Search is a safety net, not the primary interface. The archive is meant to be walked. Each directory should be small enough to browse without fatigue and rich enough to invite exploration.

3. **One Canonical Home** - Each artifact lives in exactly one location. That location reflects a choice about behavior and intention, not abstract truth.

4. **Depth Where It Matters** - Different media demand different structures:
   - **Shallow hierarchies** for Photos, Documents, Data (goal-directed retrieval)
   - **Deep hierarchies** for Books, Music, Movies (browsing and serendipity)

5. **Projects Stay Separate** - Projects are messy and temporary by design. Completed outputs get promoted into the archive and reclassified.

6. **Constraint Enables Discovery** - Flat abundance collapses curiosity. Structure reintroduces texture so that discovery becomes possible again.

## The Notebook

`Tax_Builder.ipynb` defines and enforces the physical structure. It:

- Creates the complete directory taxonomy
- Generates README.md files as contracts for each directory
- Serves as the single source of truth for the structure
- Is idempotent (safe to run multiple times)

Run all cells to build the archive structure:

```bash
jupyter execute Tax_Builder.ipynb
```

## Taxonomy Overview

### Level 1 Categories (16)

| Category | Purpose | Depth |
|----------|---------|-------|
| **Applications** | Tool ecosystems (DAWs, game engines, IDEs) | Medium |
| **Audio** | Non-music audio: recordings, experiments, AI | Shallow |
| **Books** | Long-form written works (PDF, EPUB, MOBI) | Deep |
| **Code** | Source code, scripts, repositories | Medium |
| **Compressed** | Archive containers (staging area) | Shallow |
| **Data** | Structured data: CSV, JSON, databases | Medium |
| **Docs** | Documents that aren't books | Medium |
| **Images** | Photography, scans, artwork, screenshots | Medium |
| **Intake** | Temporary landing zone (nothing permanent) | Shallow |
| **Journal** | Chronological personal writing | Shallow |
| **Movies** | Cinematic works | Deep |
| **Music** | Music for listening and browsing | Deep |
| **Notes** | Short-form thinking artifacts | Medium |
| **Projects** | Active workspaces (messy by design) | Medium |
| **Systems** | Backups, disk images, installers, configs | Medium |
| **Video** | Non-cinematic moving images | Medium |

### Detailed Structure

#### Applications (9 categories, 14 apps)
```
Applications/
├── 3D/Blender
├── Audio/Audacity, Reaper
├── Electronics/Arduino_IDE, PlatformIO
├── Game_Engines/Godot, Unreal
├── IDEs/Atom, VSCode
├── Music_Theory/MuseScore
├── Video/DaVinci_Resolve
├── Visual_Design/GIMP
└── Writing/LaTeX_Toolchain, Obsidian
```

#### Books (10 domains, 63 subcategories)
```
Books/
├── Art/Art_History, Architecture, Theory, Visual_Arts
├── Computing/AI, Algorithms, Game_Development, Graphics, Programming, Software_Engineering, Systems
├── History/Ancient, Early_Modern, History_of_Philosophy, History_of_Science, Medieval, Modern
├── Literature/Classicism, Drama, Essays, Fantasy, Historical_Fiction, Horror, Literary_Criticism,
│             Magical_Realism, Modernism, Mystery, Mythic, Poetry, Postmodernism, Romance,
│             Science_Fiction, Speculative, Thriller
├── Mathematics/Algebra, Analysis, Discrete_Math, Geometry, Graph_Theory, Logic, Number_Theory,
│              Probability, Topology
├── Misc/Unsorted
├── Music/Composition, Ethnomusicology, History, Music_Theory
├── Philosophy/Aesthetics, Daoism, Epistemology, Ethics, Logic, Metaphysics, Philosophy_of_Science
├── Psychology/Behavioral, Cognitive, Developmental, Neuroscience
└── Science/Biology, Chemistry, Complexity, Earth_Science, Physics, Systems
```

#### Music (17 genres, 230 subgenres)

The deepest taxonomy, designed for wandering and serendipity:

| Genre | Subgenres | Examples |
|-------|-----------|----------|
| **Classical** | 10 | Baroque, Romantic, Opera, Chamber, Solo_Piano |
| **Jazz** | 14 | Bebop, Cool, Modal, Latin_Jazz, Gypsy_Jazz |
| **Blues** | 10 | Delta, Chicago, Texas, British_Blues, Jump_Blues |
| **Country** | 16 | Outlaw, Bluegrass, Alt_Country, Honky_Tonk, Western_Swing |
| **Rock** | 21 | Shoegaze, Post_Rock, Grunge, Psychedelic, Math_Rock |
| **Metal** | 17 | Black, Death, Doom, Symphonic, Progressive_Metal |
| **Punk** | 11 | Hardcore, Post_Hardcore, Pop_Punk, Crust, D_Beat |
| **Electronic** | 22 | Dubstep, House, Techno, IDM, Trip_Hop, Vaporwave |
| **Hip_Hop** | 20 | Boom_Bap, Trap, Drill, Grime, G_Funk, Phonk |
| **Pop** | 16 | Synth_Pop, Dream_Pop, Hyperpop, K_Pop, City_Pop |
| **Reggae** | 11 | Roots, Dub, Ska, Dancehall, Rocksteady |
| **Soul_RnB** | 13 | Motown, Neo_Soul, Funk, Philadelphia_Soul |
| **Folk** | 11 | Celtic, Americana, Indie_Folk, Neofolk |
| **World** | 20 | Afrobeat, Bossa_Nova, Flamenco, Salsa, Klezmer |
| **Experimental** | 12 | Noise, Drone, Minimalism, Musique_Concrete |
| **New_Age** | 6 | Meditation, Space, Neoclassical |
| **Soundtrack** | 6 | Film, Video_Game, Musical_Theater |

#### Movies (12 genres, 57 subgenres)
```
Movies/
├── Action/Disaster, Heist, Martial_Arts, Military
├── Animation/Anime, CGI, Stop_Motion, Traditional
├── Art_House/Avant_Garde, Minimalist, Slow_Cinema, Surrealist
├── Classic/Golden_Age, New_Hollywood, Pre_Code, Silent
├── Comedy/Absurdist, Dark_Comedy, Romantic_Comedy, Satire, Slapstick
├── Documentary/Music, Nature, Political, Portrait, Science, True_Crime
├── Drama/Character_Study, Family, Historical, Legal, Political, Social
├── Fantasy/Dark_Fantasy, Epic, Fairy_Tale, Mythic, Urban_Fantasy
├── Horror/Body_Horror, Cosmic, Folk, Psychological, Slasher, Supernatural
├── Science_Fiction/Cyberpunk, Dystopian, Hard_SF, Space_Opera, Time_Travel
├── Thriller/Crime, Espionage, Mystery, Neo_Noir, Psychological
└── World_Cinema/African, Asian, European, Latin_American, Middle_Eastern
```

#### Other Categories

| Category | Level 2 | Level 3 | Total |
|----------|---------|---------|-------|
| Audio | 4 | - | 4 |
| Code | 5 | 16 | 21 |
| Compressed | 4 | - | 4 |
| Data | 6 | 18 | 24 |
| Docs | 5 | 17 | 22 |
| Images | 5 | 19 | 24 |
| Intake | 6 | - | 6 |
| Journal | 7 | - | 7 |
| Notes | 6 | 24 | 30 |
| Projects | 6 | 18 | 24 |
| Systems | 5 | 18 | 23 |
| Video | 6 | 22 | 28 |

## Usage

### For Humans

1. **Browse, don't search first** - Walk the directories. Let adjacency suggest what to look at next.
2. **Trust the README** - Each directory has a README explaining what belongs there.
3. **One home per file** - When classifying, choose based on how you want to encounter the file later.
4. **Intake is temporary** - Nothing in Intake is organized. Process it regularly.
5. **Projects are messy** - Don't try to organize active projects. Promote outputs when done.

### For AI Agents

1. **Place artifacts into existing structure** - Do not invent categories.
2. **Read the README** - Each directory's README is a contract.
3. **One canonical location** - Each file gets exactly one home.
4. **Predictable misclassification is acceptable** - Consistency matters more than correctness.
5. **Search is the safety net** - If unsure, search can always find it.

## Statistics

| Metric | Count |
|--------|-------|
| Level 1 Categories | 16 |
| Total Directories | ~530 |
| README Files | ~530 |
| Music Subgenres | 230 |
| Book Subcategories | 63 |
| Movie Subgenres | 57 |

## Evolution

This taxonomy is expected to evolve. Changes should be:
- **Deliberate** - Not reactive
- **Documented** - Update the notebook, not just the folders
- **Consistent** - Memory is reinforced through use, not optimization

The structure should age alongside its owner.

## Success Criteria

The success of this system is not whether a file can be found instantly. The success is whether the archive:
- Invites engagement
- Supports discovery
- Gently resists the pull of the familiar
