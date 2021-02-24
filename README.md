# bash_zt_flow
Basic flow rules for self-hosted ZeroTier network controller

I wanted to host my own ZT network controller and ztncui (https://github.com/key-networks/ztncui) is a good project for the main features needed for that purpose. However, it lacks the flow rules interface.

For this to work, you will need to have ZeroTier installed on a Linux system.  A self-hosted ZeroTier network controller can run on any host with ZeroTier installed.  Mine is running on my Chromebook using the Linux VM.

I am using ztncui for managing networks and members.  Then when I need ACLs, I use the ztrules file to create my ruleset and then run:

bash ztrules.bash

in the same directory as the file named "ztrules."

It will prompt for the ZeroTier Network ID and check to be sure it exists and then create the ruleset.

The current iteration of this project has very, very basic rule support based on how I use ZeroTier networks.  The operators "and," "not," and "or" are not yet supported but I will work on it or you are free to contribute code.  I'll also be adding a feature to check the ruleset format before parsing to catch typos.

I created this quickly for a class I'm teaching where I introduced my students to ZeroTier and some wanted to host their network controller.  I recommended ztncui and wanted to give them the ability to work with flow rules besides in the interface and to host their own network controller.

Usage:

edit the file:  ztrules
Read the notes inside the file

Then run:

bash ztrules.bash

enter the network ID you want to add the rules for and hit Enter.  It may take a few seconds as it adds the rules.  If you receive no errors, then be sure to test your rules.
