# Project Proposal
James Li

### Project title

Esports Tracker

### What and why?

For people who desire to get notified about their favorite teams within Esports, and those that want to learn more about the field and keep track of their favorite teams. 

### For whom?

This project is for anyone that is interested in Esports across multiple different titles (Counter-Strike, League of Legends, Overwatch, etc.) and will allow for both casual and hardcore enjoyers of the discipline to keep tabs on their favorite teams.

### How?

1. Utilizing the free API provided by [PandaScore](https://pandascore.co/), users will be able to enter some form of contact information (probably email), and have a notification sent to them based off of that contact information about the events that have transpired with the teams that they have requested to follow. As this will utilize a cron, this will probably be sent either daily, weekly, or monthly.

2. The free API endpoint only allows for 1k requests hourly. As a result, we will probably need to store a `.env` somewhere that has a memo of multiple keys and how many requests were sent to each key, and if one key is met to the requirement, the program will use the next available key. This should reset once an hour programatically.

3. User information like emails and usernames can be stored somewhere for personalization utilities, alongside utilizing anti-spam measures like reCAPTCHA/Cloudflare Turnstile and verification emails to ensure that only valid emails are being sent. Additionally, to conserve on API calls, there should be some automatic checking in place on the backend to see which accounts are inactive (not clicking the link to view their personalized inputs) and automatically unsubscribe those emails from the service.

### Scope

This project has a decent scope that requires many different technologies to be utilized/learned and learning about how to work around different constraints like conserving API calls, utilizing scheduling programs like crons, CAPTCHA verification, verification emails, and working with other people's APIs, alongside more that are most likely not touched on here.

  [PandaScore](https://pandascore.co/)'s API offers many games and their statistics, including but not limited to: `CS2, LoL, DOTA2, OW2, R6S, VALORANT, WoW, SC2, and more`. Due to the size of the information, decisions must be made as to which games are offered, what information we should offer, how that information is found (fuzzy search/matching queries?), and how it's displayed. 

  Thus, the frontend must be very concise, clean, easy-to-use, and navigable. Using things like JWT for authentication can be helpful, but those decisions must be made before approaching the subject.

**TL:DR;** The scope on the project is significantly larger than first glance, as there are many constraints we need to work around. Thus, it would be best to thorougly plan everything through and ensure all members are on the same page as to requirements, what new tech to learn, and allocation of work before proceeding with any development. 