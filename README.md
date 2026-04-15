This application monitors given TWS account in real time and sends a message to given discord-channel (via web-hook) when trade execution occured and position amount changed. 

A local instance of IBKR TWS must be running on the same machine where this application is used.

This application uses TWS in 'read only API' mode and doesn't use any personal account information except position monitoring.

All communication between Publisher and TWS occurs locally.

Publisher does not execute any transations on given account ('read only').


Prerequisities for using:

   1)  .NET8 Framework installed on local machine, please take ".NET Desktop Runtime" option: download from here: https://dotnet.microsoft.com/en-us/download/dotnet/8.0

   2)  Existing discord's channel web-hook, example: https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks


For deploying as user (not developer) please download the existing 2 files to your local windows folder and start the executable:
TwsPublisher.exe and TwsPublisher.dll.config (which is a text file)

Published source code is only for transparency purpose, to show that no other actions except read only account's position monitoring and WebHook request to Discord are made with this software. 


TWS must be configured for using API:

   1)  In TWS go to “Global Configuration”, API, settings and check "enable activex and socket clients" and also check "read-only API"

   2)  Note the Socket port configured. I.e 7496 and take this value into corresponding TwsPublisher.exe field

TWS Paper-Trading is also supported.
