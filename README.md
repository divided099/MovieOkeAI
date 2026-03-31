# MovieOkeAI (now depracated)

![moviebot](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/246d6543-a1bb-49dd-990e-a56025b48927)

MovieOkeAI is a revival project for MovieBot, which allowed you to transform text to a full-on 3D animation and contained other features as well and was extremely easy to use. 

# What happend to it?

![image](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/8d7144b5-1d14-44c4-a2d9-ad99fb0b4638)

The project was shut down due to lack of developers and profit; it was very un-sustainable as it was free at first and tried implementing a paid plan, but it was already too late.

Some of the owners of the project tried their best to find investors and worked hard to keep the app working and going. MovieBot had a very engaged community but just couldn't keep up, and i remember discovering MovieBot once, and it was just the month before shutdown, sadly, so i thought... "could i save it...?" so then i tried reverse engineering the APK file for it and took a look at the code, and of course some files were corrupted, but most weren't, so i got to take a good look at it, which gave me a good understanding of how it worked. i then used MitMProxy to sniff network logs with my phone to MovieBot, which is where I discovered even more on how it worked!

# How MovieBot Works

![MovieBotBanner](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/ac1c3b25-f0cd-4cc8-ba68-5b00b6cd1e57)

MovieBot highly depends on OpenAI; it uses the moderation API to make sure sissy people don't try to generate sissy things.

Ok, now for the fun stuff!

To generate stories, it uses ChatGPT; the code in MovieBot randomises models to use if the user doesn't pick one and then sends this request to ChatGPT. 

"content": "You are a creative writer who will author lines of dialogue between two characters that are witty, surprising, and laugh-out-loud funny.",
"role": "system"

Through this request it generates the story and then makes this following request:

"content": "Generate 3 lines of hilarious dialogue between \"{Model1}\" and \"{Model2}\" about: \"{GeneratedStory}\"",
"role": "system"
}

Then it makes a request to a custom API URL created by MovieBot through its own website, which no longer exists or works.

The code creates a log of user-specified settings for the animation and OpenAI-generated content and then sends it all over to here: https://static.movieoke.app/app/features.json
It generates the animation and sends it to the user, who can then preview, save, and edit it.

We assume the MovieBot API randomises model movement and may use AI to determine where to move them.

Also note that it would only allow you to use two models, but it was possible to add your own in the editor.

For voices, it used ElevenLabs AI, which was either randomised by the code or selected by the user.

From all this, I built a basic Python library for interacting with MovieBot very near to the shutdown, and it worked for a few days after the shutdown as they disconnected the MovieBot API a few days after making the library de-functional, but some aspects of it still work. The revival project includes functions and classes to assist in its construction, and I plan to have it request the re-created backend. 

![Screenshot 2023-11-15 at 6 46 11 pm](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/e91b6f16-49dc-4132-8e50-a66a947de981)

# Completed Tasks

• Backend re-creation in good progress ✅ 

• Buttons UI ✅ 

• Store Client ✅ 

• 3D/2D store backend ✅ 

• MovieBot reverse engineering ✅

• Basic 3D/2D animation generator ✅ 

• Updates backend ✅ 

• Direct messaging backend ✅ 

# Important Incomplete Tasks

• Completed GUI ❌

• Login/Signup Feature ❌

• Upload Animations ❌

• In-visioned Animation Generatation (similar to the original MovieBot) ❌

# Generated Animation

https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/0e9b35ee-f520-4117-8249-b75080365b1c

# Preview

![Screenshot 2023-11-15 at 6 49 44 pm](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/d638ad79-288e-4af5-b0de-3627100e7c89)

![Screenshot 2023-11-16 at 10 33 31 pm](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/76b20929-6258-456e-80d4-edb394825660)

![Screenshot 2023-11-16 at 10 34 08 pm](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/32180a91-ceca-42c3-8d28-d8de2b381cec)

![Screenshot 2023-11-16 at 10 34 51 pm](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/4bc89963-8ff5-444a-95de-a5cb7e8f9775)

# This is what i want each tab to look like for, 'Generate' 'Studio'

![GenUI](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/68830e03-0bfc-40a7-86a3-34408529eaaf)

![StudioSelect](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/672c625f-e5a8-44fe-b090-395719d8e5ab)
![Studio3D](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/3adf5e7e-efa7-4b4b-8704-6be514c083e4)
![Studio2D](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/15f2526a-c238-4abd-bfd7-026ef6c2df1a)

# Info

If you choose to modify and mess with what has been uploaded to this repo, then you will not have access to a lot of the MovieBot stuff, but you should still be able to make a decent mod for it if you feel like it, but we suggest joining the dev team for more control and more opportunities.

If you are interested in joining us, our dev team and dev chat currently operate on Discord; if you would like to help us out, then please do the following: https://discord.gg/xgmR67M7P2

![wiicode](https://github.com/DividedRanYou/MovieOkeAI/assets/147950850/ca7b046f-bc46-44ef-8c7e-3bf4b9d3fe4b)

# Extra

**Download link to MovieBot APK archives: https://apkpure.com/moviebot-ai/app.teleportal.movieoke/versions**

- CantStopDivided
