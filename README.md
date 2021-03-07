#!/bin/bash


# menu
clear
echo -e "\033[1;93m============================================="
echo -e "\033[1;90m[\033[1;96m•\033[1;90m] \033[1;95mAuthor  \033[1;91m :  \033[1;96mRandiansyah"
echo -e "\033[1;90m[\033[1;96m•\033[1;90m] \033[1;95mFacebook \033[1;91m: \033[1;96mRendi Saputra"
echo -e "\033[1;90m[\033[1;96m•\033[1;90m] \033[1;95mYoutube \033[1;91m: \033[1;96mRendi Noober"
echo -e "\033[1;93m============================================="
echo -e "\033[1;90m[\033[1;92mA\033[1;90m] \033[1;96mInstall Bahan"
echo -e "\033[1;90m[\033[1;95m1\033[1;90m] \033[1;93mDark Fb"
echo -e "\033[1;90m[\033[1;95m2\033[1;90m] \033[1;93mTombol Kiri-Kanan"
echo -e "\033[1;90m[\033[1;95m0\033[1;90m] \033[1;93mKeluar/Exit"
read -p "pilih sesuai input ~> " pil;
if [ $pil == "A" ]
then
    cd $HOME
    pkg update && pkg upgrade -y
    pkg install git -y
    pkg install python python2 ruby bash php clang nano figlet -y
    pkg install toilet ifconfig fish wget -y
    pip install --upgrade pip
    pip install requests
    pip install mechanize
    pip2 install requests
    pip2 install mechanize
elif [ $pil == "1" ]
then
    cd $HOME
    git clone https://github.com/Rendi-ID/DarkFb
    cd DarkFb
    python2 darkfb.py
elif [ $pil == "2" ]
then
    cd $HOME
    git clone https://github.com/karjok/terkey
elif [ $pil == "0" ]
then
    echo -e "terima kasih sudah menggunakan tools ini"
    sleep 2
    echo -e "jgn lupa subscribe channel admin :)"
    xdg-open https://www.youtube.com/channel/UClOfbjKzNtNdnAkv6uUoMNw
    sleep 5
else
    echo "salah, masukan nomor input dengan benar!"
    bash belajar.sh
fi
