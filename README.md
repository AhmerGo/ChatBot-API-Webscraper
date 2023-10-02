# ChatBot-API-WebScraper
Sample Output: 

![image](https://github.com/AhmerGo/ChatBot-API-Webscraper/assets/146684126/6f0f9826-df42-4e95-a91b-2a0ce7655044)


Twitch Bot Integration with Valorant MMR History
This script integrates a Twitch bot to fetch and present a streamer's (in this case, "Draxick") recent Matchmaking Rating (MMR) changes in Valorant.

Overview
The bot fetches data from three sources:

Stream Uptime Duration from Twitch ({{uptimeLength}}).
Stream Start Date from Twitch ({{uptimeAt}}).
MMR History for the player "Draxick" on Valorant from an external API (https://api.henrikdev.xyz/valorant/v1/mmr-history/na/draxick/000).
Using this data, the bot evaluates if the streamer is currently live, checks for any errors (like parsing issues or connection problems), and presents the MMR changes in a readable format.

Usage
Trigger the bot in Twitch chat with the appropriate command (e.g., !mmr). The bot will then respond with one of the following messages:

A statement that "Draxick is not live" if the stream is not currently running.
A summary of Draxick's current Ranked Rating (RR), tier, and the MMR change from the last game.
Error messages related to parsing data or connecting to the external server.
Code Structure
The script starts by checking the stream uptime string to determine if the streamer is live.
If live, the start date of the stream is parsed.
The MMR history data is fetched and decoded.
A series of checks and logic determine the appropriate message to display based on the received data.
If any errors occur during these operations (like parsing JSON), the error is captured and displayed in a truncated form for brevity.




