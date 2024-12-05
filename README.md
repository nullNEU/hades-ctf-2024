# hades-ctf-2024
Hades was the first Capture The Flag (CTF) event hosted by nullNEU, Northeastern University's local cybersecurity club.

### What's a CTF?
A **Capture the Flag (CTF) event** is like a treasure hunt for hackers or problem-solvers. Teams solve puzzles, crack codes, or find hidden clues in computer systems to "capture" a digital flag. Each flag earns points, and the team with the most points wins. It's a fun, competitive way to practice hacking or cybersecurity skills!

### Where does "Hades" come into play?
A **security investigation-style Capture the Flag (CTF)** focuses on simulating real-world cybersecurity incidents. Instead of just solving isolated puzzles, participants act like security analysts investigating a cyberattack or breach.

The challenges often mimic real-life scenarios, such as analyzing logs, reverse-engineering malware, or tracking an attacker's activity across compromised systems. Participants must use tools like network sniffers, forensic analysis software, or intrusion detection systems to uncover evidence and piece together the story behind the attack.

The goal is not just to find flags but to simulate the process of incident response and threat hunting, helping participants sharpen their investigative skills in realistic security environments.

The name was coined by [Devesh](https://github.com/DeveshChande), because Greek mythology is cool.

### How do I play?
There are seven stages that have to be solved in order to complete the investigation, with each challenge building on previous ones.

The order of the challenges is:
- getting-groceries
- the setup
- connoisseur
- extraction
- blind-sided
- endgame
- a-familiar-place

This means that you have to solve 'getting-groceries' prior to 'the setup'.

For example, the first challenge involves analyzing a file to identify useful data. It is a text file with Alternate Data Streams, containing the following information:
$URL = `57Gx57G957G957G557G857GD57C457C457G557Gq57G857G957Gu57Gr57Gy57G357C357Gs57G457G257C457G057Ge57Gq57GB57GK57GN57G/57Gw`

$Password = `"y|}-{.~5."}w*y--1),|w#-wn[kerYk'IIa-[kNb[n4NO^.i1}J+/g0M)oOd[pn](|-Oh(K!7`

Equipped with this information, the data is likely to be encoded. As only NTFS filesystems support ADS, the above Alternate Data Streams are provided.

### Additional Details
If you're stuck, refer to the file *solution.md* attached in the repository.

If you're curious about learning how the infrastructure was setup, refer to the file *infrastructure.md* in the repository.

