Buy me a coffee via paypal 
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=U6D8YB3PEWTVW&item_name=Buy+me+a+coffee&currency_code=USD&source=url)

```
Buy me Coffee with XLM GDQP2KPQGKIHYJGXNUIYOMHARUARCA7DJT5FO2FFOOKY3B2WSQHG4W37
```
```
Buy me Coffee with BitCoin 36fD957SDWHJYYzuH2xmceJ6T2qE9vNiV4
```
```
Buy me Coffee with XRP rw2ciyaNshpHe7bCHo4bRWq6pqqynnWKQg
``` 

```
Buy me Coffee with BAT 0xb9f4845dbEd1FB1Dae90D8e203037B5623B66666
``` 


# Script to add YouTube Ads DNS to Pi-hole black list

# You can add this link to your gravity list by going to 
http://piholeIPAddress/admin/groups-adlists.php  </br>
```https://raw.githubusercontent.com/kboghdady/youTube_ads_4_pi-hole/master/youtubelist.txt```

Also, add script to update the gravity list containing these lines : 
``` pihole -g ```
``` sudo pihole restartdns ```

# How the script works
- It will get the black.list from my github which is updated daily or every two days 
- It will update both the black.list and blacklist.txt files where the blocking of pihole happens
- It will remove any dupiclates 

it will be more effective if you add it the crontab </br>

Steps: </br></br>
1- Download the script from github using this command : </br>
```
git clone https://github.com/kboghdady/youTube_ads_4_pi-hole.git
```

```
cd youTube_ads_4_pi-hole
```
```
sudo chmod a+x youtube.sh
```
2- Create a scheduled task to run the script: </br>
```
sudo crontab -e 
```
Add this line to make it runs every 1 hour, but you can change it to whatever you like</br>
```
0 */1 * * * sudo /home/pi/youTube_ads_4_pi-hole/youtube.sh >/dev/null 
```
Where the script location is /home/pi/youTube_ads_4_pi-hole/youtube.sh </br>
more information about crontab https://crontab.guru </br>

## the List of DNS get updated daily
