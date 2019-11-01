# Secure-Torrent-System

Just like a torrent system ,our system let's you transfer the files locally between the peers ,with the full nodes(you can say servers) keeping track of all the peers and which peer is having how much percentage of a file. So when a peer requests for a file, the full node returns a list of peers which are currently hosting that particular file. So the file instead of getting serially downloaded from a single peer is now getting downloaded in parts parallelly from multiple peers. Hence more the number of peers seeding the file the less time it takes to receive it.The reason why we call this secure is because our system performs file integrity check once the file is completely downloaded, perform sharing file using encryption and a pass for joining our network.

Currently our system contains 3 full nodes which ae keeping track of all peers and each working in synchronization.

Requirements:Python 3 

If you want to run our project here are the steps

1. Create a virtual environment 
```
virtualenv -p python3 venv
```
2. Install all the necessary libraries 
```
pip3 install -r requirements.txt 
```

Install tkinter in your computer or else it will show an error when you select add torrent option.
tkinter is a python gui library.


3. Start the full nodes on a single laptop
```
./run.sh
```
4. Copy the directory of Peer on the laptop on which you want to start a peer,also create a virtual environment for the                            
   peer and follow the below steps
   
  - First activate the virtual environment
    ```
    source venv/bin/activate
    ```
  - Enter the peer directory.
  - Get the ip address of the laptop which is hosting the full nodes and replace all the the ips of network.json
    file with this ip.Don't worry about the ports,just replace the ips.
  - Run the peer.py file by going to the peer directory
    ```
    python3 peer.py 7000
    ```
    You can put any port number above 6000 
  
  - Now you can start hosting and downloading the files.
  
  
  1. Hosting the torrent File
  * Select the file which you want to host from the browse window which will appear when you select
    'add torrent' option.
    
  2. Downloading the file
  * Just enter the correct file name with extension eg.nature.jpg when you select Download file option.

