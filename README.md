This is inspired by an old MP3 sampler in the land of 8.3 that loaded a M3U playlist, looked for the peak sound, and mixed it with the other tracks and exported to a WAV file. Supercut-O-Matic Plus was fabulous, written in C++ with a GUI wrapper. I recently managed to get it working on the command line as the GUI just keep failing, and brought it back to life. 

I do not know who originally coded it and have tried for years to find out but credit to the "unknown". Thank you.

I have  taken the code and libraries, and with the help of Claude, converted it in a single offline HTML GPL file and improved it. I have added accepting different MP3 bitrates, as well as including the option to output to MP3 or WAV with different lengths, peaks, and options.

This is a passion piece as I regularly use it for my music quizzes, hence Dr D's Music Quiz, and Dr D's MP3 Mixer. I will see how far I can tinker with it to improve all I need.

1.2 vs 1.3

This is how the two versions compare. Version 1.3 is purely a visual and usability pass on 1.2. The audio side is untouched: peak detection, loudness matching, crossfades, MP3/WAV encoding and the embedded lamejs encoder are byte-for-byte identical.

Size	   v1.2	       v1.3
File size	175.7 KB	182.0 KB (+3.6%)
CSS	39 lines	      82 lines (43 added, none removed)
HTML body	33 lines	45 lines
App JavaScript	204 lines	226 lines

What 1.3 improves

Area	v1.2 v1.3
First screen	Drop zone, a full settings panel and a disabled Build button all visible at once	Only the drop zone, plus a music icon. Settings and Build appear once songs are added, and the drop zone shrinks Song rows	Name, status and five small buttons on one line, which squeezes the name on phones	Grip handle, numbered badge, 40px buttons grouped together. The name gets its own line on narrow screens
Reordering	Rows are draggable, but with only a faint fade as feedback	A line shows where the row will land Waveforms	46px tall, plain bars, no explanation	64px tall, rounded bars, a caption with peak and clip times, and a legend explaining the colours and click-to-set-peak
Settings	One flat grid of eight fields in one box	Two cards, “Clip” and “Mix and output”, with a hint under each field. Search from/to are sliders with live percentages, and the step and window settings sit under “Advanced” 

Progress	Grey status text only	A sticky bottom bar with the status, a progress bar and a full-width Build button. The “Done” message is bold
Result	Plain download link, tracklist in a proportional font	A proper download button, and the tracklist in a monospace font so the timestamps line up

Dark-mode errors	Red at about 3.3:1 contrast	Lighter red that passes the 4.5:1 guideline
Theme	Follows the system setting only	Light/dark toggle in the corner, remembered between visits
Small touches	None	Emoji favicon, stronger drag-over state on the drop zone, and each waveform has a text label for screen readers

What’s the same in both

Clip length, crossfade, peak position and loudness matching
Click-to-set-peak, preview buttons and the copyable tracklist
Drag-to-reorder, and saved settings
Worker-based MP3 encoding and the memory-saving clip extraction

If you only need the audio features, 1.2 and 1.3 behave identically. 1.3 is the one to share with other people, because it’s easier to read on a phone and easier to use for the first time.e original source is included.
