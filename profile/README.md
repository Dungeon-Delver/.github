#Dungeon Delver
A game I really enjoy playing is Dungeons and Dragons, but one of the main blocks to playing the game is finding other people to play it with since it takes at least 4 people (ideally 5-6). Thats how I got the idea for Dungeon Delver, to bridge that gap and allow people to focus on what really matters: playing the game!

## Features
Dungeon Delver allows for account creation using Facebook OAuth. The website features persistent sign-on using local storage. Once logged in, users can find parties or create a new one meeting their own specifications. The finding parties algorithm uses a party-ranking method to ensure that users see the parties that meet their specifications. Party searching has pagination and background thread prefetching to reduce wait times for the user. Alternatively, if users already know of a party, they can search for parties by party name. Once a party is found, users can request to join parties. Parties are fully customizable by the party's dungeon master, including Search Parameters that will change the search criteria for the party, status (private/public/closed), custom images, and custom party names.

As the DM, you have full control over your party. Acting essentially as an admin as well as the dungeon master, You can accept/reject users, remove troublesome users, modify party search parameters, upload custom images, or if you have no other choice, delete the party.

All members of a party have access to party chat. Party chat (implemented with Sockets API) theoretically supports an unlimited number of people, but parties are limited to 6 users. Party chat also supports pagination, so users can load more messages on demand and see chat history. Each user has a profile that can be accessed in a variety of ways (clicking on their chat message, clicking on their name in a members list for a party, etc.) Each profile lists the user's public parties. Users of a party can leave at any time; however, the DM cannot leave, only delete the party.

The website also has a live notification system. Notifications are triggered by the following events: party join request, accept party join request, reject party join request, party leave and party deletion. Notifications are fully live and paginated.

## Specifications
The frontend was built in react and the backend is a node/express server. The backend connects to a node/express server and also has a sockets API server for live notifications and chat.
