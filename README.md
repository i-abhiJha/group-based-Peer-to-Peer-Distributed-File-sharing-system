# group-based-Peer-to-Peer-Distributed-File-sharing-system
The goal is to build a group based file sharing system where users can share, download files from the group they belong to. Download should be parallel with multiple pieces from multiple peers with support for fallback multi-tracker system, parallel downloading and custom piece selection algorithm.


### Functionalities added till now:
  * multiple client can connect to the tracker
  * User should create an account and register with tracker
  * Login using user credentials.
  * Logout
  * only one user can login at a time from a certain port

### How to Run :
  * ##### Step 1: Running Tracker
      * ./tracker tracker_info.txt tracker_no
            [Assumption: Only one tracker is implemented, backup tracker not implemented yet. Therefore, tracker_no is only 1]
  
  * ##### Step 2: Running a client
      * ./tracker tracker_info.txt tracker_no
      * ###### Accessing Functionalites:
          * **creating accout:** create_user <user_id> <passwd>
          * **Login into accout:** login <user_id> <passwd>
          * **Logout from account:** logout
