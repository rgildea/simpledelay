# simpledelay
My project from Kadenze's Into to Audio Plugin Development online course. 

This project relies on the JUCE framework to bootstrap the xcode project and provide build support for various audio plugin formats/platforms:
https://juce.com/discover/projucer

Check out the presentation PDF to understand a bit about the context of this project.

There are a few interesting files to point out:
* Source/PluginProcessor.h and .cpp
* Source/PluginEditor.h and .cpp

The processor is where the actual work of processing audio takes place. This is the main method for processing blocks of audio data:
```    void processBlock (AudioBuffer<float>&, MidiBuffer&) override; ```

The editor is where you can define the user interface. This project focuses mainly on the processing, with minimal UI (no labels, no live updaing of UI controls).
