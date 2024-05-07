# Speed Read-R
![SpeedReadR-demo](https://github.com/loudbeatproductions/SpeedReadR/blob/master/assets/Promo_cropped_2.gif?raw=true)

- ### [**_Demo**](#speed-read-r)
- ### [**_Intro**](#intro)
- ### [**_Reader screen**](#reader-screen)
- ### [**_Reader**](#reader)
- ### [**_Settings**](#settings)
- ### [**_Formats**](#formats)
- ### [**_Quick text**](#quick-text)
- ### [**_Download**](#download)
- ### [**_Usage**](#usage)
- ### [**_Known bugs**](#known-bugs)
- ### [**_Changelog**](#changelog)
- ### [**_About**](#about)
- ### [**_Donations**](#donations)
- ### [**_License**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/LICENSE.txt)

---
---
## Intro
**Speed Read-R (SRR for short) is an application that aims to greatly improve the reading speed of the user without any more effort than it normally takes to read.**

How is that achieved? That's an interesting question, let me explain.

We normally read text moving our eyes through the rows of letters from one end to the other and repeating the sequence again and again for each row. Actually, our eyes are really good to dettect and follow the movement, which isn't the case when we read, the text is stationary, and the only thing that moves is our eyes, but they aren't following anything, so you're not using them on their strongest feature.

As we run along the rows, our eyes jump on quick movements and stop to focus on a spot, then we see the whole word and pick up it's meaning before we jump again to the next spot. We don't read letter by letter, and we also don't actually see when our eyes are jumping from place to place. All this takes time, in which we are not reading, but moving, focusing and even some times we need to do it multiple times in order to catch what the word says, or to jump to the row below trying to not accidentally skip one.

Your brain can go faster then your eyes. Maybe not all of us, but considering the normal average reading speed is about 200 to 350 words per minute (you can make a test by yourself to know where you are at), I found myself easily jumping above 400 and even 500 words per minute without preparation or training of any type. That's close to double the speed without breaking a sweat.

SRR expliots the advantage of RSVP, which stands for rapid serial visual presentation. This is a technique in which we are presented with images, or words in this case, in series, with a certain lapse between each other. This method pretty much gets rid of the necessity of our eyes to move and enables our brain to focus on what really matters.

Will this degrade my comprehension?

For a start, we are probably not getting 100% comprehension even when we read at our normal old speed. You can test that by yourself doing an online test, but on average we get something around 60%. In my case, I found myself derrailing and my mind starts to wander around the slower the information is broungt up, not to say that I'll be going >1000 words per minute just like a speed reading expert, but keeping the information coming at a good pace could even help keep youreslf focused on the thread and not be distracted by the hundreds of things goung around your mind at a given time.

SRR will break a text into pieces and give you each word the optimal focus spot aligned on a fixed position. You won't have the need to scroll around with your eyes, and your brain won't have to wait on idle until your vision jumps to the next spot and focus on the image of the new word. All the breaks and distractions are ripped off, and the only thing left is the information ready to be processed.

---
---

## Reader screen
![SpeedReadR-screen](https://github.com/loudbeatproductions/SpeedReadR/blob/master/assets/reader-screen.png?raw=true)

1. Menu.
2. Book title.
3. Current word index.
4. Total word count.
5. Progress bar.
6. Calculated time left to finish.
7. Calculated current words per minute.
8. Selected words per minute.
9. Toggle hide book text, shortcut [**F**].
10. Speed up wpm +10, shortcut [**S**].
11. Speed down wpm -10 shortcut [**D**].
12. Play/pause reader, shortcut [**spacebar**].

---
---
## Reader
The reader has a top bar showing the current word index/total words, a progress bar, a timer that roughly estimates the time left to finish, the current measured WPM and the currently selected WPM.

On the bottom half of the screen you'll find the whole text. Double clicking on any word would set the current position of the word count, prompter, and the progress bar (if activated).

The letters "**S**", "**D**", "**F**" and "**Space** bar" are used as shortcuts.
- **S** : Increase WPM by **+10**
- **D** : Decrease WPM by **-10**
- **F** : Toggle **fullscreen**
- **Space** : **Start/Stop** player.

"**S**" "**D**" and "**Space**" also work in the settings screen to control the prompter from settings and the selected WPM of the current configuration.

---
---
## Settings
- ### [_Reader size](#reader-size)
- ### [_Background size](#background-size)
- ### [_Words per minute (WPM)](#words-per-minute-wpm)
- ### [_Acceleration](#acceleration)
- ### [_Focus pointer](#focus-pointer)
- ### [_Word length delay](#word-length-delay)
- ### [_Dot Delay](#dot-delay)
- ### [_Comma delay](#comma-delay)
- ### [_Progress bar](#progress-bar)
- ### [_Blink](#blink)
- ### [_Blink duration](#blink-duration)
- ### [_Blink interval](#blink-interval)
- ### [_Blink fade toggle](#blink-fade-toggle)
- ### [_Blink fade time](#blink-fade-time)
- ### [~~_Blink color~~](#blink-color)
### Reader size:
Changes the size of the text shown by the prompter

### **Background size:**
Changes the text size shown by the navigator.

### **Words per minute (WPM):**
Changes the number of words per minute the prompter will pressent. This will vary deppending on the value of some other parameters like dot delay, comma delay, etc.

### **Acceleration:**
Select the number of secconds since play it'll take to reach the maximum speed selected.

### **Focus pointer:**
Toggle the pointer that aligns with the certer of the prompter to have a visual refference of the optimal focus point.

### **Word length delay (LWD):**
This number changes the delay produced by a word deppending on it's length. The formula used is to first calculate a "step" that'll be the number of milliseconds added per letter, the current equation is the following: 

    step = 60 / WPM / ( LWD / 10 )
Then the steps are calculated upon the current word length.

    current_step = step * (length of the current word)
and then the total delay in milliseconds is added from the following formula:

    total_delay = current_step + ( 1 / current_step / 1000 )

For a more intuituive appreciation, having the same WPM value, a lower WLD value will produce more delay, and a higher value will produce less.
I'll say that a "normal" value could be between 40 and 60. You can however, achieve the same result on a different value with a different WPM, so go along and play with it until you find a value of your comfort.

Have in mind that activating this function would reduce the accuracy of words per minute you'll receive, though that's just a number, and you should tune this setting regarding on how comfortable you feel with it.

### **Dot Delay:**
Add a delay if the word has a dot in the end, simbolyzing the end of the snetence. This delay is not taken into account for the estimated reading time left

### **Comma delay:**
Add a delay if the word has a comma in the end. This delay is not taken into account for the estimated reading time left

### **Progress bar:**
Activate or deactivate a visual progress bar and word index shown on the top.

### **Blink:**
Activate or deactivate the blink function.

### **Blink duration:**
Change the blink duration in miliseconds.

### **Blink interval:**
Change the delay between blinks in seconds.

### **Blink fade toggle:**
When turned on, the blink shown on the prompter as " —.— " will gradually change it's transparency until it fades out. The feature will reset after stopping the prompter.

### **Blink fade time:**
Select the time in which the blink will end up fading completely.

### **~~Blink color:~~**
 (Depercated) ~~Select the color of the blink shown on the prompter.~~

---
---
## Formats
Current formats supported:
- txt
- md
- rtf
- epub
- pdf
- docx
- tex

The inner guts of the different formats may not be all the same, so some can cause a "bad interpretation" and the reader may not pressent the content as it should in the viewer.

---
---
## Quick text
Quick text provides two fields, in which you can write a title for a new file, and write or paste from the clipboard a new text to save in your setted folder. The new file will be instantly opened and presented on the reader upon the pressing of the "save & read" button.

---
---

## Download
Latest version: **1.3.0**

---

- ### [**Windows**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/SpeedReadR_1.3.0.exe?raw=true)

SHA256 Windows: `78b901934cfae0d628e1fb893758a249bdaa1bb258bc66cd6ede3627afe6c109`

--- 

- ### [**Linux (Compiled in Ubuntu)**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/SpeedReadR_1.3.0_Ubuntu?raw=true)

SHA256 Ubuntu: `272b0c095e90454c40d102ad23d28c74c66ca1766a1416339f552d7ea771b3cf`

---

- ### [**Linux (Compiled in Arch)**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/SpeedReadR_1.3.0_Arch?raw=true)

SHA256 Arch: `f591cdcc02eaff4560841668d7c53b45f95f3d26f8ef7f9ac437f1e501a6f055`

---

- Mac (hopefully coming soon)

---
---

## Usage
- ### **Linux:**
    Grant executable permissions to the file
    ```
    chmod +x SpeedReadR_1.3.0_Ubuntu
    ```
    or
    ```
    chmod +x SpeedReadR_1.3.0_Arch
    ```
    Open a terminal and launch the application.

    ```
    ./SpeedReadR_1.3.0_Ubuntu
    ```
    or
    ```
    ./SpeedReadR_1.3.0_Arch
    ```

- ### **Windows:**

    Execute the launcher (It may need **admin** privileges for reading and writing settings and files.)


No internet connection needed.

---
---
## Known bugs
- App icon doesn't work on Linux.
---
---
## Changelog
- **v1.3.0**
    - Update libraries.
    - Processing book content now uses threading and async.
    - Added loading animation when processing book content.
    - Added error handling when missing books and simmilar scenarios.
    - Added measured words per minute as some choosen delays config affects real WPM output.
    - Added lots of new theme colors.
    - Improved timer accuracy.
    - Fix prevent OS to go to sleep mode or turn off screen while playing.
    - Fix glitch on quick text on text input going out of layout.
    - Minor fixes.
    
    - Removed HUE selection.
    - Removed blink color selection.
    
- **v1.2.0**
    - Changed reader to iterator (should improve performance)
    - Fixed total word count glitch in the menu bar.
    - Fixed default paths.
    - Changed absolute paths for relative paths, database should now be portable between OS* and PCs.
    
    \* Feature in development, may not yet work.
- **v1.1.0**
    - Initial public release
---
---

## About
My work and future projects on [@Loudbeat](https://www.instagram.com/loudbeat) and [Github](https://github.com/loudbeatproductions)

---
---
## Donations

- Bitcoin
```
bc1ql8vsr57vctxeqqm0ayer04j6lqgsc6gtpytley
```
---

- ERC20
```
0x7c7C32E8400a2B9EecAD55f94f4F734bA520687f
```

---

- BNB
```
bnb1aheerja9dlfs6tsda5gq6aj3vzxhm2rjm4e620
```

---

- [**Coindrop**](https://coindrop.to/loudbeat)

- [**ko-fi**](https://ko-fi.com/loudbeat)

- [**coffee**](https://www.buymeacoffee.com/loudbeat)

---
---
# Thanks!


\* The entirety of this app was made without the aid of any LLM or language-processing neural network.