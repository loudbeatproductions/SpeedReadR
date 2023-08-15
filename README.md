# Speed Read-R
![SpeedReadR-demo](https://github.com/loudbeatproductions/SpeedReadR/blob/master/assets/Promo_cropped_2.gif?raw=true)

- ### [**Demo**](https://youtu.be/nV46OvaFsds)
- ### [**Intro**](#intro)
- ### [**Settings**](#settings)
- ### [**Formats**](#formats)
- ### [**Reader**](#reader)
- ### [**Quick text**](#quick-text)
- ### [**Download**](#download)
- ### [**Usage**](#usage)
- ### [**Known bugs**](#known-bugs)
- ### [**Changelog**](#changelog)
- ### [**About**](#about)
- ### [**Donations**](#donations)

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
## Settings
- ### [Reader size](#reader-size)
- ### [Background size](#background-size)
- ### [Words per minute (WPM)](#words-per-minute-wpm)
- ### [Acceleration](#acceleration)
- ### [Focus pointer](#focus-pointer)
- ### [Word length delay](#word-length-delay)
- ### [Dot Delay](#dot-delay)
- ### [Comma delay](#comma-delay)
- ### [Progress bar](#progress-bar)
- ### [Blink](#blink)
- ### [Blink duration](#blink-duration)
- ### [Blink interval](#blink-interval)
- ### [Blink fade toggle](#blink-fade-toggle)
- ### [Blink fade time](#blink-fade-time)
- ### [Blink color](#blink-color)
### **Reader size:**
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

### **Blink color:**
Select the color of the blink shown on the prompter.

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
## Reader
The reader has a top bar showing the current word and the total word count of the oppened book, a progress bar, a timer that roughly estimates the time left to finish, and the currently selected WPM.
Below is the prompter and on the bottom you'll find the whole text. Double clicking on any word would set the current position of the word count, prompter, and the progress bar (if activated).

The letters "**S**", "**D**", "**F**" and "**Space** bar" are used as shortcuts.
- **S** : Increase WPM by **+10**
- **D** : Decrease WPM by **-10**
- **F** : Toggle **fullscreen**
- **Space** : **Start/Stop** player.

"**S**" "**D**" and "**Space**" also work in the settings screen.

---
---
## Quick text
Quick text provides two fields, in which you can write a title for a new file, and write or paste from the clipboard a new text to save in your setted folder. The new file will be instantly opened and presented on the reader upon the pressing of the "save & read" button.

---
---

## Download
Latest version: **1.2.0**

---

- ### [**Windows**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/SpeedReadR_1.2.0.exe?raw=true)

SHA256 Windows: `75d94cd758f77f08d638f41f63928c74ed6e065aabfc6d96e5c50d292e5ac538`

--- 

- ### [**Linux (Compiled in Ubuntu)**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/SpeedReadR_1.2.0_Ubuntu?raw=true)

SHA256 Ubuntu: `d46f800c09bf0f849b37fe73e70b5040fb904fb227db4ce1a87fec7b22a9fc4f`

---

- ### [**Linux (Compiled in Arch)**](https://github.com/loudbeatproductions/SpeedReadR/blob/master/SpeedReadR_1.2.0_Arch?raw=true)

SHA256 Arch: `0841a353e6328304570be38d2f38c05bdfeb44f99888d2e007922cd13f3abd5e`

---

- Mac (hopefully coming soon)

---
---

## Usage
- ### **Linux:**

    Open a terminal and launch the application.

    ```
    ./SpeedReadR_1.2.0_Ubuntu
    ```
    ```
    ./SpeedReadR_1.2.0_Arch
    ```

- ### **Windows:**

    Execute the launcher (It may need **admin** privileges for reading and writing settings and files.)


No internet connection needed.

---
---
## Known bugs
- Folder selector forces to exit the application in Windows, if possible avoid using it and use the default `Books` folder.
- App icon doesn't work on Linux.
---
---
## Changelog

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


