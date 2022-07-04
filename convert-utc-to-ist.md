## Convert Server Time from UTC to IST

1. Search for the available timezones using the following command
  
   ```sh
   timedatectl list-timezones | grep -i Asia
   ```
2. Unlink the current timezone

   ```sh
   sudo unlink /etc/localtime
   ```
3. Set the new timezone. The syntax for setting the new time zone is as below
   ```sh
   sudo ln -s /usr/share/zoneinfo/[zone/timezone] /etc/localtime
   ```
   
   For example
   ```sh
   sudo ln -s /usr/share/zoneinfo/Asia/Kolkata /etc/localtime
   ```
4. Verify the updated time
   ```sh
   date
   ```
