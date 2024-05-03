# mireaCTF-2024

On May 1st my team World Wide Flags and I competed in mireaCTF and we got `#3`!
I worked on the 6 OSINT challenges and was able to solve 4 of them. The last two I could only solve after the CTF had ended, but I'm going to put them into this writeup anyway.

## Infernal Manager

### Description (translated from Russian)
>I recently saw a girl reading and decided to ask what she was reading and at what point. She didn’t answer what kind of book it was, she started talking all sorts of nonsense about sins, that it was on some 15th song of the first part and that the hero of another work was based on the main character of the book, and in the end she sent a link to the track on YouTube as a hint - https ://www.youtube.com/watch?v=XfTWgMgknpY
Nothing is clear, but the book is probably interesting, help me find it.
Flag - the title of the book in English and the year it was written.
Flag format: mireactf{Book_Name_YYYY}

### Writeup

Listening to the song at first it was unclear what to look out for. After figuring out that the song was a soundtrack of the Game *Limbus Company*, we can look at the main characters of this game and find that none of them is Dante.
![image](https://github.com/mead-0w/mireaCTF-2024/assets/147707798/4eda3655-c8b6-490f-b26d-fee893d5830b)

Which fits the challenge description. 
Dante Alighieri's most famous work is "The Divine Comedy", which he started writing in 1308. This leads us to our flag:

`mireactf{Divine_Comedy_1308}`
