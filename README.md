# icspa-public-data
game/data/ for icspa



# Download the data

1) Install Git LFS: https://git-lfs.github.com

2) Execute `git clone https://github.com/ics-nju-wl/icspa-public-data.git`

3) `cp -r icspa-public-data/data <your_icspa_folder>/game/`



# Create your own BGM

To create your own background music for credits (assuming you have a .mp3 file):

> sox credits_bgm.mp3 -r 16k -b 16 -c 1 temp.wav

> dd if=temp.wav bs=1 skip=44 of=credits_bgm.wav

find out the size of the `credits_bgm.wav`

modify `file_table` in `kernel/src/fs/fs.c`, and replace the second value for the entry `credits_bgm.wav` to the proper size