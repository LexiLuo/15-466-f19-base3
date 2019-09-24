
BLENDER=/Applications/Blender.app/Contents/MacOS/Blender

all : ../dist/park.pnct ../dist/park.scene ../dist/brunch.pnct ../dist/brunch.scene ../dist/garden.pnct ../dist/garden.scene ../dist/city.pnct ../dist/city.scene #hexapod.pnct hexapod.scene

../dist/park.pnct: park.blend export-meshes.py
	$(BLENDER) --background --python export-meshes.py -- park.blend:Parts '$@'
../dist/park.scene : park.blend export-scene.py
	$(BLENDER) --background --python export-scene.py -- park.blend:Scene '$@'
../dist/city.pnct : city.blend export-meshes.py
	$(BLENDER) --background --python export-meshes.py -- city.blend:Parts '$@'
../dist/city.scene : city.blend export-scene.py
	$(BLENDER) --background --python export-scene.py -- city.blend:Scene '$@'
../dist/brunch.pnct : brunch.blend export-meshes.py
	$(BLENDER) --background --python export-meshes.py -- brunch.blend '$@'
../dist/brunch.scene : brunch.blend export-scene.py
	$(BLENDER) --background --python export-scene.py -- brunch.blend '$@'

../dist/garden.pnct : garden.blend export-meshes.py
	$(BLENDER) --background --python export-meshes.py -- garden.blend '$@'
../dist/garden.scene : garden.blend export-scene.py
	$(BLENDER) --background --python export-scene.py -- garden.blend '$@'

hexapod.pnct : hexapod.blend export-meshes.py
	$(BLENDER) --background --python export-meshes.py -- hexapod.blend:Main '$@'

hexapod.scene : hexapod.blend export-scene.py
	$(BLENDER) --background --python export-scene.py -- hexapod.blend:Main '$@'
