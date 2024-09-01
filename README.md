# About 
Scale Mapper is a tool designed to generate a list of repeating frequency values from a source list such that the result covers a comparable range of the 128 frequencies found in the standard 12-tone equal temperament. 

The use case stems from my experiments with the Colundi Sequence, a tuning system that focuses on discrete frequencies as opposed to interval relationships. While the Colundi Sequence contains 128 values, it's much more musical to focus on a smaller subset of frequencies, often between 12 - 15 values.

When using Scala to generate a scale focused on discrete frequencies we run into an issue where the keyboard no longer represents the range of values represented by our custom scale. The goal of this mapper function is to repeat the values in our custom scale such that they occupy positions of a similar frequency in the standard equal temperament. i.e. if our custom scale contained frequencies 33, 55, 70, 105 we would repeat 33 for the first 27 MIDI notes.

It's a bit convoluted to explain, but the goal is to create a closer relationship between standard keyboards and sequencers to the range of values in custom scales focused on discrete frequencies.

# How to Use
1. Ensure you have node installed, you can verify by running `node -v` in your command line from any directory.
1. Replace the values in the customScale array with the values of your custom scale. 
2. Save the file and from the command line run `node scale-mapper.js`.
3. Open the file Output.txt and copy the list of frequencies. You can use the [frequency to cents ratio converter](https://freq-to-cents.netlify.app/) at https://freq-to-cents.netlify.app/ to get a list that is ready to be pasted into a Scala file. I like to paste this result in to [scale workshop](https://sevish.com/scaleworkshop/?version=2.5.7) to verify my work and export to Scala from there.


## Future Plans

- Create a CLI that uses a file path to a Scala file.
- Enable output file naming.
- Eventually create a web deployment and possibly extend the frequency to cents converter to provide an option to generate a list that maps to the range of values found in the 128 MIDI notes tuned to the standard equal temperament.
