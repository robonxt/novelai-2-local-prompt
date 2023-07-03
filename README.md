# Based off of [animerl/novelai-2-local-prompt](https://github.com/animerl/novelai-2-local-prompt)
# novelai-2-local-prompt
Script for Stable-Diffusion WebUI (AUTOMATIC1111) to convert the prompt format used by NovelAI.  

## robonxt's (this fork) changes
The spacing between the text buttons are weird, so I tried fixing them. I'll also try making it look like actual buttons, but idk how to do that yet.

## tldr
Add two new buttons:
1. Button to convert the prompts used in NovelAI-style prompts for use in the WebUI.  
2. Button to recall a previously used prompt.  

## Credits

ORIGINAL: https://github.com/animerl/novelai-2-local-prompt

## INSTALL
Use WebUI's `Extensions` tab  
## Usage
<img width="201" src="https://user-images.githubusercontent.com/113022648/197382468-65f4a96d-48af-4890-8fcf-0ec7c3b9ec3a.png">

Simply click on `NAIConvert`.
It will automatically process the brackets, prefix them with a quality tag, and insert a default value in the negative prompt.
Multipliers are rounded off to four decimal places.

```
(a),{b},[c]
↓NAIConvert
masterpiece, best quality,
\(a\),(b:1.05),(c:0.9524)
```
Click `History` to call back previously generated prompts, starting with the newest. The default maximum number of saves is 10 (`MaxHistory`).
