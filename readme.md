[comment]: # "Auto-generated SOAR connector documentation"
# ShadowDragon SocialNet

Publisher: ShadowDragon  
Connector Version: 1\.2\.0  
Product Vendor: ShadowDragon  
Product Name: SocialNet  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.0\.1068  

This app supports investigative actions on the SocialNet cloud investigation API

# phantom-socialnet

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a SocialNet asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**api\_key** |  required  | password | API key for SocialNet
**verify\_server\_cert** |  required  | boolean | Verify remote server certificate

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[hunt alias](#action-hunt-alias) - Hunt for an alias in SocialNet  
[hunt email](#action-hunt-email) - Hunt for an email address in SocialNet  
[hunt phone](#action-hunt-phone) - Hunt for a phone number in SocialNet  
[hunt name](#action-hunt-name) - Hunt for a person's name in SocialNet  
[hunt phrase](#action-hunt-phrase) - Hunt for a phrase in SocialNet  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'hunt alias'
Hunt for an alias in SocialNet

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**alias** |  required  | Alias to hunt for social network accounts | string |  `user name`  `alias` 
**limit** |  optional  | Number of query results to return \(max 10000\) | numeric | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.alias | string |  `user name`  `alias` 
action\_result\.parameter\.limit | numeric | 
action\_result\.data\.\*\.avatar\_url | string |  `url` 
action\_result\.data\.\*\.id | string | 
action\_result\.data\.\*\.name | string | 
action\_result\.data\.\*\.social\_site\_name | string | 
action\_result\.data\.\*\.type | string | 
action\_result\.data\.\*\.url | string |  `url` 
action\_result\.summary\.total\_results | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'hunt email'
Hunt for an email address in SocialNet

Type: **investigate**  
Read only: **True**

Limit is the maximum boundary for the results returned for each socialnet site and not the total results cumulative of all the sites\. Maximum results \(limit\) for each socialnet site are 10000\.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**email** |  required  | Email address to hunt for social network accounts | string |  `email` 
**limit** |  optional  | Number of query results to return \(max 10000\) | numeric | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.email | string |  `email` 
action\_result\.parameter\.limit | numeric | 
action\_result\.data\.\*\.avatar\_url | string |  `url` 
action\_result\.data\.\*\.bits | numeric | 
action\_result\.data\.\*\.created\_at | string | 
action\_result\.data\.\*\.id | string | 
action\_result\.data\.\*\.is\_disabled | boolean | 
action\_result\.data\.\*\.is\_expired | boolean | 
action\_result\.data\.\*\.is\_revoked | boolean | 
action\_result\.data\.\*\.name | string | 
action\_result\.data\.\*\.public\_key\_algorithm | numeric | 
action\_result\.data\.\*\.social\_site\_name | string | 
action\_result\.data\.\*\.type | string | 
action\_result\.data\.\*\.url | string |  `url` 
action\_result\.data\.\*\.user\_ids\.\*\.created\_at | string | 
action\_result\.data\.\*\.user\_ids\.\*\.email | string |  `email` 
action\_result\.data\.\*\.user\_ids\.\*\.id | string | 
action\_result\.data\.\*\.user\_ids\.\*\.is\_disabled | boolean | 
action\_result\.data\.\*\.user\_ids\.\*\.is\_expired | boolean | 
action\_result\.data\.\*\.user\_ids\.\*\.is\_revoked | boolean | 
action\_result\.data\.\*\.user\_ids\.\*\.name | string | 
action\_result\.data\.\*\.username | string |  `user name` 
action\_result\.summary\.total\_results | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'hunt phone'
Hunt for a phone number in SocialNet

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**phone** |  required  | Phone number to hunt for social network accounts | string |  `phone` 
**limit** |  optional  | Number of query results to return \(max 10000\) | numeric | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.limit | numeric | 
action\_result\.parameter\.phone | string |  `phone` 
action\_result\.data\.\*\.avatar\_url | string |  `url` 
action\_result\.data\.\*\.id | string | 
action\_result\.data\.\*\.name | string | 
action\_result\.data\.\*\.social\_site\_name | string | 
action\_result\.data\.\*\.type | string | 
action\_result\.data\.\*\.url | string |  `url` 
action\_result\.summary\.total\_results | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'hunt name'
Hunt for a person's name in SocialNet

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**name** |  required  | Name to hunt for social network accounts | string |  `name` 
**limit** |  optional  | Number of query results to return \(max 10000\) | numeric | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.limit | numeric | 
action\_result\.parameter\.name | string |  `name` 
action\_result\.data\.\*\.avatar\_url | string |  `url` 
action\_result\.data\.\*\.bits | numeric | 
action\_result\.data\.\*\.created\_at | string | 
action\_result\.data\.\*\.expires\_at | string | 
action\_result\.data\.\*\.id | string | 
action\_result\.data\.\*\.is\_disabled | boolean | 
action\_result\.data\.\*\.is\_expired | boolean | 
action\_result\.data\.\*\.is\_revoked | boolean | 
action\_result\.data\.\*\.name | string | 
action\_result\.data\.\*\.public\_key\_algorithm | numeric | 
action\_result\.data\.\*\.social\_site\_name | string | 
action\_result\.data\.\*\.text | string | 
action\_result\.data\.\*\.title | string | 
action\_result\.data\.\*\.type | string | 
action\_result\.data\.\*\.url | string |  `url` 
action\_result\.data\.\*\.user\_ids\.\*\.created\_at | string | 
action\_result\.data\.\*\.user\_ids\.\*\.email | string |  `email` 
action\_result\.data\.\*\.user\_ids\.\*\.id | string | 
action\_result\.data\.\*\.user\_ids\.\*\.is\_disabled | boolean | 
action\_result\.data\.\*\.user\_ids\.\*\.is\_expired | boolean | 
action\_result\.data\.\*\.user\_ids\.\*\.is\_revoked | boolean | 
action\_result\.data\.\*\.user\_ids\.\*\.name | string | 
action\_result\.data\.\*\.username | string |  `user name` 
action\_result\.summary\.total\_results | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric |   

## action: 'hunt phrase'
Hunt for a phrase in SocialNet

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**phrase** |  required  | Phrase to hunt for social network accounts | string |  `phrase` 
**limit** |  optional  | Number of query results to return \(max 10000\) | numeric | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.parameter\.limit | numeric | 
action\_result\.parameter\.phrase | string |  `phrase` 
action\_result\.data\.\*\.avatar\_url | string |  `url` 
action\_result\.data\.\*\.id | string | 
action\_result\.data\.\*\.name | string | 
action\_result\.data\.\*\.social\_site\_name | string | 
action\_result\.data\.\*\.text | string | 
action\_result\.data\.\*\.title | string | 
action\_result\.data\.\*\.type | string | 
action\_result\.data\.\*\.url | string |  `url` 
action\_result\.summary\.total\_results | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 