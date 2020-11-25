# Bullet journal templates for the reMarkable
Screen estate optimised bullet journal templates for the reMarkable (2) paper tablet

These are basic bullet journaling grids with 32 squares vertically. I created them so that one can easily copy/paste things between monthly, regular and quarter pages while taking advantage of the full screen estate of the reMarkable devices and have day numbers with indicated weekends.

## Install

If you don’t have any of the fancy third party tools, you can just use `scp` and if needed `ssh` and `vim`.  
These come with few to **no guard rails**. You can **brick your device** if you run the wrong commands so be careful 😱  
If you have not used these tools before or feel insecure it is a good idea to read an introduction to them or to ask a friend for help or supervision. You’ll learn the most if they don’t touch your keyboard 😊

1. Clone or download the repo and navigate into it.
1. Copy the `*.png` files to `/usr/share/remarkable/templates/` on your remarkable using something like  
`scp *.png root@reMarkable:/usr/share/remarkable/templates/.` so that the templates will be on your device.   
Depending on your wifi router you might have to replace `reMarkable` with your reMarkable’s IP. You find it on the device under `Menu->Settings->Help->About->Copyright and licenses` on the first page in the last line on the screen. Two lines further up you’ll also find the `ssh` **password**.
1. Either copy the `templates.json` from this repo to your remarkable or edit your existing `templates.json` on your device so that your device becomes aware of the new templates. If you already have added custom templates, you will have to edit. Otherwise just copying should be okay with firmware version 2.4.1.30. It is safer to make a backup now using `scp root@reMarkable:/usr/share/remarkable/templates/templates.json backuppath/.` and it only takes seconds. After making the backup
**either**
    * Copy the `templates.json` from this repo `scp templates.json root@reMarkable:/usr/share/remarkable/templates/.`  
**or**  
    * Edit your existing file by using `ssh root@reMarkable` and `vim /usr/share/remarkable/templates/templates.json` to merge the content of `32_58.json` from this repo.  
1. Restart the reMarkable `Menu->Settings->General->Restart` and enjoy the templates.

## 😱 My reMarkable can’t load templates after the reboot 😱

Don’t panic. Usually that means the reMarkable could not parse the `templates.json` 😖. Look into it and maybe use a [JSON validator](https://duckduckgo.com/q=json+validator&ia=answer) to figure out what is wrong. Usually it is a comma. It happens to everyone once in a while. Bon courage! 🤗

## Credits

The basic dot pattern was created using Austin Andrews’ [Remarkable Template Builder](https://github.com/Templarian/Remarkable).
