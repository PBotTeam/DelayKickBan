KickBanFix - By fall3n


DESCRIPTION

Since 0.3x release, functions - Kick, Ban or BanEx functions are called quickly when processed. So any functions which 
would get or set player's data will fail as it would lose the connection. There had been some fix for this by 
delaying the Kick/Ban function and I've also been using it before. But then I realized that it's not completely efficient 
because in case if a player is spamming and an auto-kick is kept, the server would still receive data until the player's
connection is actually lost. This is a bad practice and would create a mess if the scripter hasn't denied 
the data of the player after kick/ban is processed.

This include ensures that most of the player's update won't be synced to the server, including chat, commands,
dialog responses, vehicle updates and death information. This include is compatible with both 0.3x version and
0.3z version.

Also, this include provides an OPTIONAL parameter called "delay_ms" which is actually the time(in milli-seconds) to be delayed over Kick, Ban or BanEx functions. 

native Kick(playerid, delay_ms=150); //If used as Kick(playerid); delay_ms will be set as 150 (default value)
native Ban(playerid, delay_ms=150);
native BanEx(playerid, const reason[], delay_ms=150);
native IsKickBanProcessed(playerid); //Returns : 1 if kick/ban is being processed, 0 if not.



INSTALLATION

Place "KickBanFix.inc" on /pawno/include/ directory.


CREDITS

- fall3n for the complete include.
- SA-MP Team for SA-MP.

LICENSE

      This Source Code Form is subject to the
      terms of the Mozilla Public License, v.
      2.0. If a copy of the MPL was not
      distributed with this file, You can
      obtain one at
      http://mozilla.org/MPL/2.0/.


CONTACT

	Github : https://github.com/falle3n/
	
	
Thank you for using KickBanFix.inc

