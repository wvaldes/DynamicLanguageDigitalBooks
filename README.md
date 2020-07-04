# DynamicLanguageDigitalBooks
Interactive audio supported books that the user can experience in more than one language

Purpose:
This project came about due to the percieved benefit of having better reading materials for learning a new language. The personal story is that my 5 year old daughter was attending Mandarin classes and the materials that I found available online, in libraries, and other places did not reflect the wealth of materials that I was use to for English (hooked on phonics, etc). Traditional books had phonetics (pinyin) but the translations were often geared towards communicating the idea of what the story was rather than a more literal understanding of what was being said. Suffice to say, I concluded that a digital version of Early Readers in Mandarin or other languages could be designed to be a much better solution than what I was finding in the market.

There was one problem ... I'm not a programmer. And so began the journey ...

Summary of efforts to date:
1. Attempt iBooks with iAuthor - too limited
2. Attempt to follow EPUB format leveraging Jutoh - too limited
3. Wordpress - this allowed creation of click a button and play a sound file solutions pretty quickly. Other parents in class found this very helpful. Much of this material and lessons are still available at https://www.minathuvia.com/. These are mostly vocabularly lessons.
4. Stand alone website. I was able to pull together a functional (but horrible looking) demonstration which can be viewed at https://minathuvia.com/mandarin/reader1.0.html. This code a progression of W3 schools, numerous Stack Overflow searches, successive Udemy courses, etc. As such, it is a spagetti bowel of what I've learned over time both good and bad and I'm only now starting to be able to tell the difference. It claims to follow zero design patterns or best practices. 

Current effort - refactor this if not completely rewrite it from scratch using GitHub for version control. I may fork it myself to explore different approaches as I continue to learn C#, serverless, and continue to argue with myself about Angular vs React vs Vue vs Svelt vs plain vanilla JS. There was a lot of use of JQuery that I'm going to attempt to avoid as I look to integrate Boostrap 5 possibly. 

A BIG thank you to: 
Eric Larson for his EPUB course
Maximilian Schwarzmuller, Shaun Pelling (The Net Ninja), Andrei Neagoie, Frank Kane, and the amazing Angela Yu for their awesome Udemy courses.
The insane number of folks who support FreeCodeCamp, W3 Schools, StackOverflow who have pulled me out of the ditch numerous times.
Anyone who wants to suggest ways to make this better.
My daughter Mina who's honesty keeps me from writing boring stories.

Primary book functions and features.
For books with the intention to learn Mandarin

1. To the extent possible the book should be written in Mandarin first. 
This helps to keep the cultural appropriateness, phrasing, and natural langaugae flow. As my wife, who is a native Colombian can attest, English books translated to Spanish just don't read as well to a native speaker as one written in native Spanish. I assume this is true for other languages.

2. As Mandarin is a language of characters rather than an alphabet, the explanation of characters should be brokendown to the most simple level. 
This is because an English speaking child will have the experience of an alphabet creating a word rather than a character holding the meaning of a concept. Also, the child will see the same character again potentially used elsewhere so it is helpful for clarity. One example is to not use the English word "Yes" as there is no equivalent in Mandarin but rather simply repeate the verb as it the Mandarin custom. Another example is the concepts of here and there require two characters in Mandarin which correlate to "this" and "that" combined with a Mandarin word that implies a location (this location or that location). The issue is "this" and "that" are characters used elsewhere for those meanings so it is confusing to be taught that they mean "here" and "there". It is easier to explan "this location" and "that location" which carry the same conotation. There are many examples of this and this is an issue when translating from any language to another.

3. Color the character with its tone.
Mandarin is a lagunage to tones. These are often difficult to remember when first learning so one option is to use font color as an assist to the learning to remind them of the tone. The color should be able to be turned off (toggled) and possibly customzied to the users preference. Note that the tone for a word can change depending where it is in relation to other words so the tone designation can't simply be hard coded to a character. 

4. Make elements able to hide/show.
At first there is a desire to show the character, pinyin, meaning, and English translation at the same time. As English speaking children are accoustom to an alphabet, they adapt quickly to pinyin and tend to focus on the pinyin. This is helpful for awhile but at some point, the child needs to start relying on the character. The digital solution is to consider ways to alter the pinyin to force the child to look at the character. The easy way is to simply hide the pinyin but other options include decreasing the opacity over time or other creative approaches. This is an issue with printed books as the pinyin is either there or it isn't. Also, as the child progresses in skill, it should be possible to hide the pinyin of words they are supposed to know, while showing the pinyin of new words.

5. Chinglish is a "thing".
I first heard of this from YoYoChinese and it is simply sticking to the Mandarin word order. However, in a dynamic digital book, it is also possible to mix English and Chinese together to allow more complex stories. For example if you've only learned one Mandarin character, then a story could be totally in English except for that one word which would show up in Mandarin. As the child learns more words, the story would gradually change to show more and more Mandarin characters. These changes could be managed manually or if there is a lesson plan with vocabulary words, those could be loaded up to a story to set the book to a certain level. This could be lesson speciifc or a cummulative set of vocabulary.

6. The opportunity in #5 separates the book content from the lesson content. This will allow teachers to come up with their own lesson plans and still leverage all the stories. So if a teacher wants to start with numbers and colors first, then they book would show those words in Mandarin. However if another teacher wanted to start with conversational content first (My name is ____ , what is your name?) then they could load those lesson plans.

7. Children like to see their own name so one option is to store part of the story as a variable such as the lead character's name and allow the user to enter the child's name and see it reflected across the story. Note that doing this can create issues if any supporting artwork isn't dynamic too.

8. Tracking progress will require some sense of State or storing the users "current page" or something. There are lots of ways to do this and I'm still learning.

9. With various audiences (readers, parents, authors, teachers, admin, etc) there will need to be some solution to user management, profiles, accounts, usernames, passwords, etc. Salted hash's seem adequate for passwords but OAuth options appear useful too.

10. My daughter highly prefers drag and drop .... anything. For learning, the option to incorporate small games or activities in the story may be an option to keep their 30 second attention span while still teaching them something.

11. Audio support for individual characters, words, and whole sentences. 

12. Text highlighting as the audio is played.

13. Ability to change the book from simplified to traditional characters

14. Change size of font or even the font type

15. Show a list of all the characters/words in a story and be able to set their default display (character, pinyin, english)

16. Come up with a way to handle words like "sibling" which would take up a considerable amount of space if you translate character by character.


I'll continue to add ideas and pipeline features. I look forward to seeing what the community comes up with and what features other langauge might need.

