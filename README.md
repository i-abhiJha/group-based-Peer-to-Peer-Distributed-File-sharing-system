# group-based-Peer-to-Peer-Distributed-File-sharing-system
The goal is to build a group based file sharing system where users can share, download files from the group they belong to. Download should be parallel with multiple pieces from multiple peers with support for fallback multi-tracker system, parallel downloading and custom piece selection algorithm.


### Functionalities added till now:
  * multiple client can connect to the tracker
  * User should create an account and register with tracker
  * Login using user credentials.
  * Logout
  * only one user can login at a time from a certain port
  * The clients which create the group, by default should become owner of that group. (If Owner leaves the group, some other group member should become owner of that group).
  * Fetch list of all Groups in server.
  * Request to join a group.
  * Leave Group
  * List/Accept Group join requests(if owner)

### Working:
  1. At Least one tracker will always be online.
  2. Client needs to create an account (user_id and password) in order to be part of the network.
  3. Client can create any number of groups (group_id should be different) and hence will be owner of those groups.
  4. Client needs to be part of the group from which it wants to download the file
  5. Client will send join request to join a group
  6. Owner Client Will Accept/Reject the request.

### How to Run :
  * ##### Step 1: Running Tracker
      * ./tracker tracker_info.txt tracker_no
            [Assumption: Only one tracker is implemented, backup tracker not implemented yet. Therefore, tracker_no is only 1]
  
  * ##### Step 2: Running a client
      * ./tracker tracker_info.txt tracker_no
      * ###### Accessing Functionalites:
          * **creating accout:** create_user <user_id> <passwd>
          * **Login into accout:** login <user_id> <passwd>
          * **Create Group:** create_group <group_id>
          * **Join Group:** join_group <group_id>
          * **Leave Group:** leave_group <group_id>
          * **List pending join:** list_requests <group_id>
          * **Accept Group Joining Request:* accept_request <group_id> <user_id>
          * **List All Group In Network:** list_groups 
          * **Logout from account:** logout
