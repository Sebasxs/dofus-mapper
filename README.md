# Dofus context generator for Corinna
Takes Dofus game files and makes them readable:
- Exported *markdown* files are used for AI context injection.
- Data uploaded to the database (or exported as JSON files) are treated as menu components.

*Input data must be located in the **`src/input`** folder in JSON format.*

## Breeds
A brief introduction to Dofus breeds and their gameplay.
```Shell
$ node ExportBreeds
# Output: src/pages/breeds/*.md
# Database root updated 'dofus_breeds'
```

## Spells
Update all character/monster spells including effects, criterions and details.
```Shell
$ node UpdateSpells
# Database root updated 'dofus_spells'
```

## Jobs
Update the information of all jobs.
```Shell
$ node UpdateJobs
# Output: src/pages/jobs/*.md
# Database root updated 'dofus_jobs'
```

## Recipes
Update all item recipes.
```Shell
$ node UpdateRecipes
# Database root updated 'dofus_recipes'
```

## Maps
Update the information of every map in the game.
```Shell
$ node UpdateMaps
# Database root updated 'dofus_maps'
```

## Subareas
- Update all subareas info.
- Update NPCs positions based on subareas data.
- Export markdown files with named-maps info and image urls.
```Shell
$ node ExportSubareas
# Database root updated 'dofus_subareas'
# Database root updated 'dofus_npcs'
# Output: src/pages/subareas/*.md
```

## Hints
Export coords of key places in Dofus.
```shell
$ node ExportHints
# Output: src/pages/hints/*.md
```

## Documents
Transcription of game books and documents with their respective images.
```Shell
$ node ExportDocuments
# Output: src/pages/documents/*.md
```

## Feature descriptions
Information about the main features of Dofus.
```Shell
$ node ExportFeatureDescriptions
# Output: src/pages/guides/*.md
# Output: src/data/guidebookImageNames.json
```

## Map captions
Add captions and watermark to map images.
```Shell
$ node AddCoordsViaCanvas
# Input: src/output/maps/map-images/*.jpg
# Output: src/output/maps/map-coords/*.jpg
```