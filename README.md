# Loop Patches

Using the patch command in git allows you to apply code from other developers, pull requests, or even saved customizations you regularly make. If you are applying code from other developers, please ensure that you look through the code and understand what the code changes are before incorporating it. It is your responsibility to underwhat and implement your Loop system and you do this at your own risk.

# Automatic Dose Strategy Switching

In my experience Automatic Bolus works great to combat highs, but can be too aggressive overnight or when dealing with lows. This automatic switcher allows you to set a BG threshold for switching between temp basal and automatic bolus. For instance if set at 130 mg/dl, Loop will automatically use temp basals under 130 mg/dl and switch to automatic boluses over 130 mg/dl. This has greatly solved the issue of needing to have AB aggressive enough to combat high BG while needing it less aggressive in lower range.

This patch also incorporates my Nightscout profile uploader fix and is needed in order to ensure you do not overload your NS database profile table. Typically Loop uploads a new profile everytime any setting is changed. This includes starting/stopping an override as well as this new automatic switcher. This generates thousands of extra profile saves to Nightscout each month. The patch limits Loop to only upload a new profile if Basal, Carb Ratio, or ISF is changed. The only item not implemented that needs a profile upload is if you add/edit/delete an override. This is needed because it populates Nightscout's remote override drop down box. If you make changes to your saved overrides, just force an upload by temporarily changing one of the 3 primary settings and then changing it back.

Please watch my YouTube video for directions on installation.
