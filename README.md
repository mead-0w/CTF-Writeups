# Info

On May 1st my team World Wide Flags and I competed in mireaCTF and we got `#3`!
I worked on the 5 OSINT challenges and was able to solve 3 of them. The last two I could only solve after the CTF had ended, but I'm going to put them into this writeup anyway.

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

## Isekai to nowhere

### Description (translated)
>A friend fell asleep in a minibus under asmrchik, and woke up at the final station in an unknown place. His GPS doesn’t work, and this shy guy doesn’t want to ask passers-by, so he turned to me. Unfortunately, I have topographical cretinism, so I need your help finding a building with a blue roof.

Format flag: mireactf{xx.xxx,yy.yyy}

### Writeup

In this challenge we got a video file and had to find info about the location. We quickly know that we have to find the building number 28, and that is has to be located at the final stop of a bus line in Moscow.
At the end of the video we can very briefly see a number flickering inside the arriving bus, which is 223. This points us to the solution.

![Screenshot 2024-05-01 125138](https://github.com/mead-0w/CTF-Writeups/assets/147707798/bb7f129d-fe3d-4ff3-99f7-6899a0bf9b16)

![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/c29fb400-98d0-4bb4-9ac9-0456d4f2b938)

As we now have the exact address, we can confirm in Google Street view and get the coordinates `55.827990, 37.825043`
Rounding these we get our flag: 

`mireactf{55.828,37.825}`

## 大阪の魔法少女

### Description (translated)
>The magical girls from Tres Magic were already completely tired of the tricks of Magic Baizer, and they decided to take extreme measures - to find out where she lives and make a personal visit. Unfortunately, they have no idea where their rival lives, the only clue is that she most likely goes to high school just like them. Luckily, during the last battle, the villain dropped several pages from her diary, so now they have something to dig for. Help them find where their enemy lives.

Format flag: mireactf{7-chōme-3_Shimoyamatedori} , number do not need to be specified

### Writeup

We get a word document containing the girl's diary. Reading through it we can filter out the main information which will lead us to the solutin of the challenge:
+ she lives in Takatsuki, Osaka
+ she lives near a junior high school
+ has an elementary school with a park to the east
+ has a fabric store across the road
+ has a hair salon in her block

After looking at what feels like every school in that town, googling for "fabric store" in Takatsuki finally did the trick.

![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/d6a597aa-fcf1-4c60-a73e-176360b382d3)

 "Kashiwaya" store points us to the solution.
 
 ![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/f8c60d6e-916d-453e-8a84-eaa2342839c2)

 The girl's block is 1-chōme-6 Matsugaoka which gives us our flag:

 `mireactf{1-chōme-6_Matsugaoka}`

 Unfortunately we were not able to solve the remaining 2 challenges `Fun in the Wasteland` and `Stunning Biter`during the CTF. I solved them right after the CTF ended with some pointers from the challenge author, so I want to include these in my writeup for future reference.

 ## Fun in the Wasteland

 ### Description (translated)
>One of the cult shooter programmers once spoke impartially about the plot in games. Subsequently, fate turned against him - his last project was not very successful, and the programmer himself eventually went into the field of AI. However, the game itself was not abandoned, and relatively recently even a sequel was released, with good ratings. One foreign site even compared the game to more classic representatives of the genre, although it gave the game the lowest rating available for the game on the most famous review aggregator.
We need to find this site.
Flag - the title of a review from this site for the most highly rated RPG of last year and the rating of this RPG. Example - mireactf{Cloud_roza_las_nubes_con_una_entrega_magistral_9.7/10}

### Writeup
The challenge comes with a screenshot from metacritics.com - this will be crucial to finding the solution.

![wasteland](https://github.com/mead-0w/CTF-Writeups/assets/147707798/c5adda65-9623-499c-a662-930567db3d7c)

At first we have have to find which programmer the challenge is talking about. After some googling we find "JOHN CARNACK", whon made some nasty comments about plots in video games.
+ his latest game was `RAGE`

We are looking for the sequel, which is `RAGE 2` and it came out somewhat recently.

Looking on metacritic.com/ for reviews of that game, we find 3 reviews with low scores:

![Screenshot 2024-05-01 182523](https://github.com/mead-0w/CTF-Writeups/assets/147707798/44306d37-54cb-4dc4-81f0-2ef6e2e978a2)

Clicking on the profile pages, we see that the image which was given in the challenge corresponds to the profile of gamer.no

Going on their site we now only have to look for a review of the most hyped RPG game of 2023 (which was Baldur's Gate III) and see how they rated the game:

![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/a1b90c7e-7e39-48b5-b24e-0be5a7ea3a87)

![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/5a7ca57a-d17b-49cf-a332-d261feb576d2)

And we get the flag:
`mireactf{Eit_av_dei_beste_rollespela_nokosinne_9/10}`

## Stunning Biter

### Description (translated)
>Eh, I’m so sick of it that lately bloggers, in order to lure the audience, constantly inflate their emotions and put their shrunken faces on the preview. But I remember that almost 10 years ago, one popular blogger, during his let’s play, unironically fell into shock with his mouth open at the events taking place in the game for a good couple of tens of seconds. I just forgot what kind of video it was...
Flag - the address of the link to the video with the timecode of the start of the reaction.
Flag format: mireactf{ https://www.youtube.com/watch?v=dQw4w9WgXcQ&t=42s}

### Writeup
The challenge comes with a picture that points us in the right direction - we know that we are looking for some video in relation to the game FNAF 4.

![bebra](https://github.com/mead-0w/CTF-Writeups/assets/147707798/4cf20c46-78e0-4f86-9c1e-bbe41f8d556b)

Searching for `FNAF 4 bite` on Youtube shows us a video of famous Youtuber "Markiplier" from 8 years ago. We are on the right track.

![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/4475afb9-592b-4d9c-9333-5ff3744a1973)

https://www.youtube.com/watch?v=AZgnZSmbYn0

Looking through the video and after nearly fainting due to some jumpscares, we find the required reaction:

![image](https://github.com/mead-0w/CTF-Writeups/assets/147707798/81a4a6fa-806d-44c1-9f52-4bcf4e93d74a)

The timestamp to this scene: https://youtu.be/AZgnZSmbYn0?t=563 gives us the flag:

`mireactf{https://www.youtube.com/watch?v=AZgnZSmbYn0&t=563s}`
