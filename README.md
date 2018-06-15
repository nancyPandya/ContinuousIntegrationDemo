# ContinuousIntegrationDemo

Continuous Integration using Xcode Server

Apple introduced it’s own Xcode Server since Xcode 9, which is to be used for continuous integration for our projects.

We need to follow the below steps for implementing CI :-
1.    Open Xcode Project -> Preferences -> Server & Bots; turn on the server to provide CI.
    ⁃    Configure the settings and permissions as needed.
    ⁃    In the Mail tab, fill in all the details, save and it’s done.

2.    Now, in Xcode  Preferences -> Accounts; click on the plus icon to add a server account.
    ⁃    Choose Xcode Server for account type.
    ⁃    Next, choose the server with the name(can be your system’s user name) which you just configured in Server & Bots section.
    
3.    To start the integrations, we first have to create bots, Xcode -> Product -> Create Bot.
    ⁃    Name the bot and choose the server for CI.
    ⁃    Configure the repository/source control for project.
    ⁃    Choose the scheme and configure the settings.
    ⁃    Choose the time and duration you want for integrating the team’s work.
    ⁃    Allow Xcode Server to manage your certificates and profiles, go in the Certificates & Profiles tab to add the necessary certificates and profiles to the server.
    ⁃    Configure the environment variables, only if needed, it’s not necessary.
    ⁃    Add triggers to bot and configure as per your need
        •    Periodic Email Report, to get reports after every integration
        •    New Issue Email, to receive the emails for occurring issues
        ⁃    Create the bot.
        
4.    After creation, bot will start integrating the project and that’ll be your first integration. After that, every integration will take place as you configured it for and on success you’ll get a .ipa file of your project.

5.    Bots can be edited and deleted after creation as needed, you can see the boy activity in the last tab of the right menu in Xcode, also you’ll receive the daily reports via email(Periodic Email Report trigger).

6.    Also, if you setup the server using the name or IP address in a system using same DNS, you can configure, integrate and manage the bots from any system you’d like.
