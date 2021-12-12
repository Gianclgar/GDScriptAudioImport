# GDScriptAudioImport
A script for Godot in GDScript for importing .wav (via parsing the wav header), .ogg and .mp3 audio files at runtime.

I'm sure there's way more efficient ways to do this, but for me this works so far and it's my little baby.


# Usage instructions and example
1. Import the script in to your project
2. When you want to load you can call the class:
```gdscript
var music = AudioStreamPlayer.new()
var audio_loader = AudioLoader.new()
music.set_stream(audio_loader.loadfile("/path/to/song.ogg"))
music.volume_db = 1
music.pitch_scale = 1
music.play()
```

### TODO:

0. Test with very different wav files in order to see if format parsing works for different chunk sizes (doesn't seem to)
1. Create a light version with only what is needed to set the AudioStreamSample
2. Complete the "full version" - Keep it big for learning/referencing purposes
3. Make it as a script Plugin
4. Look for more efficient ways to parse the data and update it.
5. Hope Godot Community and devs include a ´.wav´ importer at runtime that works at least as fine as the .ogg importer
