# ChatBot-API-WebScraper

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
Dependencies
Nightbot: Used for bot integration with Twitch. The script appears to rely on Nightbot's variable system (e.g., $(user), $(channel), $(eval ...), etc.).
Valorant MMR History API: An external API that provides MMR history for a given Valorant player.
Important Notes
Ensure the external API URL (https://api.henrikdev.xyz/valorant/v1/mmr-history/na/draxick/000) is up-to-date and that the API structure hasn't changed.
The script assumes a specific JSON data structure from the external API. If the API changes, the script may break.
Consider handling rate limits or potential outages for the external API for a smoother user experience.
This README provides an overview of the script's purpose, functionality, and dependencies. Make sure to adjust it to your needs, especially if there are additional details or specific nuances about the script's operation that weren't provided in the initial description.




