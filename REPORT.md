# Discord Hack Report

## Summary
In the last couple weeks there has been a large surge in hacks across the Discord platform.  
These hacks use a different approach to target their victims. It has been seen before that 
hackers would obtain Discord account  
credentials via a fraudulent link pertaining to Discord Nitro, but this approach undermines the trust between users to test a 'simple  
game' not only grabbing Discord tokens, but installing malware on the victims computer.

<br>
<br>

## WARNING
These hackers are serious and will try to [extort you for money](/HackingScreenshots/SellingPrice/price.png). They are stealing valuable Discord accounts to sell them for profits. They are also [spending money](/HackingScreenshots/ProofOfHack/transaction-history.png) linked to these accounts. To see what the might be doing look at [this image](/HackingScreenshots/SellingPrice/reasoning.png).  
These hackers are also threatening to [delete accounts](/HackingScreenshots/MoriFakeEmailer/email-threat.png) for not complying. As seen from a emailer claiming to work at discord.  
They also may make subtle threats such as [this one](/HackingScreenshots/Threat/possible-threat.png).  

<br>
<br>

## How this affects the Mori community
The community for the [Mori](https://www.youtube.com/c/Mori) channel has been deeply affected by these hacks. Mori's Discord server has been comprimised and is most likely beyond the point of recovery. Many supportive community members came together over Mori's Discord server, but have now lost that privilage and lost the ability to trust other members.

### How did this happen?
I am a member of the Mori community, I've been following the channel for a long time. Over this time I've developed a minor mutual friendship with Mori as he is engaged with comminicating with his community. As an active Discord user and developer, I have many friends over Discord, including one I made in a programming related Discord server.  

<br>

On `February 21, 2022` at `4:37pm PST` I am contacted by this old friend from a programming server. They ask me if I could do them a 'favor' and test out their 'simple game' named [Pintflight](/HackingScreenshots/MalwareAnalysis/analysis.png). I was suspicious of their intent, but knowing I had talked to them before and shared a common developer interest, I mistakenly trusted them. I ran their 'Unity Game' under a basic security scan but nothing came up. So I ran the program. After I ran the program, and noticed the 'game' had not started within a couple seconds, I was immediately concerned, I now knew what they were up to. I recieved [several emails](/HackingScreenshots/ProofOfHack/emails.png) from Discord that my email and password was changed and a new account was created using my email. Then on both my desktop and mobile device, was logged out of discord. I have just lost access to my account.  

The following day, `February 22, 2022` at approximately `2:45pm PST`, I recieved word from a tweet from Mori (though the original tweet was deleted) that his Discord has been hacked by a viewer of his. I instantly [replied](https://twitter.com/BraedenSowinski/status/1496256413672550401) to his tweet explaining:
```
Damn, if this is the result of my account getting hacked I am so sorry
```
The next following couple minutes Mori and I conversed, I explained how it was not me and my Discord account was hacked the night prior. The hacker noticed the messages between Mori and I over Discord, and used that to his advantage. Mori knew that I was a developer, what he didn't know was that I was locked out of my account, and I was not the one messaging him. The hacker asked mori the same thing, to do them a 'favor' and to test their 'simple game'. Unknowingly Mori trusted my name, and ran the program. Mori has now lost access to his Discord account.

The following days not much happened, I tried to bargain with the hacker via my alternative account. But on `Februarry 24, 2022` at `5:08pm PST` the hackers started to abuse their power, I called out Mori's account for being hacked on the Discord server. I was then [banned](/HackingScreenshots/HackAbuse/ban.png) for 'lying' when I was trying to warn everyone of the fictitious account. They handed out permissions to their fellow hacker friends in the Discord server, and banned several others. The hacker on Mori's account purged the chats and tried to suppress anyone who called them out on it. All of the hackers abuse on the Mori Discord server can be seen in the [HackAbuse](/HackingScreenshots/HackAbuse/) folder.

<br>
<br>


## Investigation on the Malware
As a tech savvy person who is into Software and Cyber Security, I reached out to a Cyber Security specialist on YouTube who does reverse engineering / malware analysis. He [responded with interest](/HackingScreenshots/MalwareAnalysis/check.png) and I await to hear back with his in depth report. He provided a [link to a breif overview of the malware](https://app.any.run/tasks/f350328b-df2d-4eb3-84cc-6dc1c114da54) on [ANY.RUN](https://app.any.run/).

Looking into the ANY.RUN analysis, we are able to determine several suspicious acitivies and factors. One important activity that flags it as suspicious is the large sudden drop of files into a `/.nexe_natives/` folder as well as deleting several files from `C:/ProgramData/` [seen here](/HackingScreenshots/MalwareAnalysis/files.png).

This analysis also includes a [brief review](/HackingScreenshots/MalwareAnalysis/any.run.png) of what the program is attempting. This can be shown with the [processes](/HackingScreenshots/MalwareAnalysis/processes.png) that are seen to be run.

Another suspicious factor that is vital to finding more information is the [connections](/HackingScreenshots/MalwareAnalysis/connections.png). We can see it calls out to https://ipconfig.io/ to gather information from our IP address, as well as three connections to a `superfuniestindianparty.rip`. We too can run the IP address of that domain to find out some more information. We find out the [ipconfig](/HackingScreenshots/MalwareAnalysis/ipconfig.png) shows that it is based in Turkey. More proof to associate the hackers and malware from Turkey is seen in the [FromTurkeyProof](/HackingScreenshots/FromTurkeyProof/) folder. 

### Persistant Malware
The malware is persistant, after the brief investigation into the malware, I thought removing the `/.nexe_natives/` would be enough to disrupt the malware and prevent anything further. I did several overviews of my Task Manager and stopped and non-essential programs. I double checked all StartUp related folders to make sure anything that shouldn't be there wasn't there. I thought my computer was in the clear.

`February 25, 2022` at `11:01am PST` I recieved an email from Discord that my email has been added back to my account, and my password needed to be reset. I have successfully gained back my Discord account. I started trying to get things back to normal, have my friends unblock my account and let everyone know I was in the clear.  One thing to know is that I ran `Windows 11 Insider Preview` so updates for my computer were almost daily occurances. I required a restart for an un update, nothing out of the ordinary, a couple minutes go by and my computer updates.  
I log in and start continuing my day on my computer. When I recieve yet another email from Discord claiming my accounts email to be changed, I look at my account settings and see my account email, has been changed. I attempt to change it back, but my password was changed as well. I was hacked again, at `1:08pm PST`.

Through their persistant malware they also managed to [hack an alternative account](/HackingScreenshots/ProofOfHack/myemails.png) of mine, and are trying to delete it. This is an important detail as my alternative account was signed in on a entirely different browser as my main. This goes to show the malware is capable of surveying multiple browser types for stored Discord Tokens.

<br>

To see a full in depth analysis you can view it [on github here](https://github.com/kem0x/Discord-Trojan-Research)

<br>
<br>

## Hacker Abuse of Power
The hackers, after obtaining Mori's Discord account and full control over his Discord server, they started to abuse their power. The hacker invited his friends and gave them [admin privilages](/HackingScreenshots/HackAbuse/hack-abuse.png). This can be seen in depth in Mori's Discord servers [audit log](/HackingScreenshots/ServerAuditLog/).

### Leaked Hacker chats
During the abuse of power, several screenshots exposing the hackers chats have been collected, one of them depicts the hacker on Mori's account messaging his friend about [getting admin powers](/HackingScreenshots/LeakedHackerChats/hacked-leaked.png). As well as his friend telling the Hacked Mori account to ["grab all his friends / then sell"](/HackingScreenshots/LeakedHackerChats/hacker-chat.png). Finally, we know there was at least 3 hackers proven in [this image](/HackingScreenshots/LeakedHackerChats/proof-of-group.png).

### Who to avoid?
Majority of the hackers accounts have been exposed so you know when they get involved in any situation.

1. `wax#1337`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Discord ID: `213553482513252352`
2. `Krii$ 4L#1337`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Discord ID: `913486395438428171`
3. `45qk#2345` aka `Hire#0002` Discord ID: `117035637411938312`

You can view all their associated accounts in the [hacker profiles](/HackingScreenshots/HackerProfiles/) folder.
