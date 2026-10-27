# Synapse Privacy Policy

**Effective date:** 27 October 2026  
**Bot owner/operator:** Nathan  
**Privacy contact:** qXrdf@proton.me  
**Bot support/community:** [SUPPORT SERVER OR CONTACT URL]

This policy explains how the operator of Synapse (the “Bot”) handles information when people use the Bot in Discord servers. Complete the remaining bracketed fields and publish this policy at a stable, publicly accessible URL before submitting it for Discord verification. The policy files are intended for publication in a separate public GitHub repository; the current project repository is private. This template describes the current Bot implementation; update it if the Bot’s features or data practices change.

## Information the Bot processes

The Bot receives information through Discord interactions and, where enabled, server events. Depending on the features a server uses, this can include:

- Discord user, server, channel, role, and message identifiers needed to respond to commands and operate server features.
- Leveling records, including XP, level, prestige, and message-activity timestamps; voice activity is used to award eligible voice XP.
- Virtual economy balances and daily/work reward timestamps.
- Poll questions and options, poll creator and message/channel/server identifiers, and each voter's Discord ID and selected option.
- Moderation warnings, including the warned user’s ID, moderator ID, reason, server ID, and creation time.
- Server configuration such as selected channels and roles, feature settings, and configuration for logging webhooks. Webhook credentials are stored with the Bot’s local database and are treated as operational secrets.
- Music upload consent records associated with a Discord user ID. If a user uploads audio, the Bot stores the audio file and related metadata (track name, uploader ID, server ID, file size, duration, and upload time) for that server’s jukebox.
- Message content is inspected to award message-based XP and to operate the configured honeypot feature. When a honeypot is triggered, the Bot may include up to 500 characters of the message in a security alert sent to the server’s configured log destination.
- If a server uses tickets, moderators can request a transcript. The Bot reads the ticket channel’s available message history, including message text, embeds, and attachment URLs, and sends a transcript file to the configured transcript channel. The Bot does not keep that transcript as a separate local database record.
- A member’s Discord avatar is fetched from Discord when generating a level card.

The Bot also processes command inputs and interaction data to carry out the requested command. Discord may provide message content fields only under the access conditions and exceptions described in Discord’s own documentation and platform terms.

## How information is used

The Bot uses this information only to provide and maintain its features, including leveling, polls, the virtual economy, moderation records, server configuration, music storage and playback, tickets, security alerts, and command responses. Operational logs are used to diagnose errors and reliability issues. The Bot does not currently use this information for advertising, sell it, or use it to train machine-learning models.

## Where information is stored and who receives it

Persistent Bot records are stored in a local SQLite database at the location configured by the operator. Uploaded music files are stored on the Bot host in a server-specific music directory. The operator rents the Bot server from [Fasthosts](https://www.fasthosts.co.uk/); the rented server is located in the United Kingdom. As the infrastructure hosting provider, Fasthosts may process or have access to data stored on or transmitted through that server in providing its hosting services, subject to its own terms and privacy information.

Information is sent to Discord as needed to operate the Bot, including command responses, server messages, moderation actions, configured log messages, and ticket transcripts. Ticket transcripts are posted in the transcript channel selected by that server’s administrators and may be visible to people with access to that channel. Discord processes this information under its own terms and privacy policy. The Bot does not intentionally send its stored data to other analytics, advertising, or AI providers.

The operator’s application logs are written to the host and rotated by size (a current log plus up to three 2 MB backups). Logs may contain technical details and Discord identifiers when needed to diagnose an event. The database and music files are not encrypted by the Bot itself; host-level access controls and backups depend on the operator and hosting provider.

## Retention and deletion

The Bot does not currently apply an automatic expiration schedule to stored warnings, leveling and economy records, poll records and votes, server settings, upload-consent records, or uploaded music. They generally remain in the local database or music directory until the Bot operator removes them or deletes the relevant storage. Discord messages and transcript posts remain subject to Discord and server retention controls.

The Bot does not currently provide a self-service command for exporting or deleting an individual’s stored data. To ask about access, correction, or deletion, contact **qXrdf@proton.me** and include the relevant Discord user ID and server ID, if available. The operator will review the request and explain what can be removed. Some records are associated with a server and may require that server’s administrator or the Bot operator to locate and delete them. Deletion may not remove information already posted to Discord, contained in a host backup, or retained where a legal or security need applies.

## Security

The operator uses a local database and host storage to run the Bot. Access controls, backups, and physical or infrastructure security are managed by the Bot operator and hosting provider. No internet-connected service can be guaranteed completely secure. Do not provide sensitive personal information to the Bot or in tickets unless necessary for support.

## Children

The Bot is not designed to collect information from children in violation of applicable law or Discord’s minimum age requirements. Server administrators are responsible for using the Bot in compliance with applicable age and privacy requirements.

## Changes to this policy

The operator may update this policy when the Bot or its data practices change. The latest version will be published at **https://github.com/xnovos-dev/SynapseINFO/blob/main/PRIVACY_POLICY.md**. Continued use after an update is subject to the revised policy to the extent allowed by applicable law.

## Contact

For privacy questions or requests, contact: **Nathan** at **qXrdf@proton.me**.  
Support/community: **[SUPPORT SERVER OR CONTACT URL]**
