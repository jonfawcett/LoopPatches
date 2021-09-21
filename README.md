# Loop Patches

Using the patch command in git allows you to apply code from other developers, pull requests, or even saved customizations you regularly make. If you are applying code from other developers, please ensure that you look through the code and understand what the code changes are before incorporating it. It is your responsibility to understand and implement your Loop system and you do this at your own risk.

# Automatic Dose Strategy Switching

In my experience Automatic Bolus works great to combat highs, but can be too aggressive overnight or when dealing with lows. This automatic switcher allows you to set a BG threshold for switching between temp basal and automatic bolus. For instance if set at 130 mg/dl, Loop will automatically use temp basals under 130 mg/dl and switch to automatic boluses over 130 mg/dl. This has greatly solved the issue of needing to have AB aggressive enough to combat high BG while needing it less aggressive in lower range.

# Nightscout Profile Upload

Typically Loop uploads a new profile everytime any setting is changed. This includes starting/stopping an override as well as when the dosing strategy is changed. This can generates thousands of extra profile saves to Nightscout each month which can cause other issues. The patch limits Loop to only upload a new profile if Basal, Carb Ratio, ISF, target range, or an override setting is changed.


# Combined Patch

This patch incorporates the Strategy Switch er and Nightscout profile uploader fix together. Both are needed in order to ensure you do not overload your NS database profile table while using the switcher patch.

Please watch my YouTube video for directions on installation. Update to video: The NS patch now handles uploading override modifications correctly.
https://www.youtube.com/watch?v=m6Cy4nlkaNQ&t=4s

Before installing, always make sure you understand when this was last tested and updated by me by reviewing the commits on my fork to see the last date I merged from Loopkit's main repository.
https://github.com/jonfawcett/Loop/commits
