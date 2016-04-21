# MyChat
A modified version of chatty project using private_hub and Thin.   (Added group chat based on private chat for now) 

#Start version References
  https://github.com/Joseph-N/chatty


#To get this working
  Go ahead and do git clone
  Do bundle
  
     bundle
  
  Next
  
     rake db:drop db:create db:migrate db:reset
  
 Then change Assert_path for emoji in initializer/emoji_picker.rb to be your host url
    
     Emoji.asset_host = 'https://natasha-yujhuang.c9.io/'
     
 Finally, run your server
 
     rails s -p $PORT -b $IP
     
#Reminder

 For Thin server, it should be running on new terminal. It is only for 'real time' functionality of the chatting app which uses faye/faye.js (does not work for now and need refresh page everytime send messages)
     Run this command for chat server in a different terminal
     
     rackup private_pub.ru -s thin -E production
     
  PS: the chat thing is kinda working anyway even the thin server is not running, but not in real time. You have to refresh to see the upcomming messages in the chat box. The reason is that the browsers are blocking insecure script. However, if set up a new host for chat server and works for production host. It will work real time.
     
     
     
     
     
     
 
