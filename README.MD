# Dissect technology add-on for Splunk

Provides sourcetyping for ingestion and processing of dissect records. 

## Prerequisites and dependencies
When ingested Dissect output contains Evtx records they are correctly interpreted according to CIM if the Splunk Windows TA is installed. 
To achieve this, the XmlWinEventLog of the Windows TA is altered to perform KV_MODE field extractions. 
Therefor, be carefull to use this app in a production monitoring environment.

App dependencies:
- Splunk Windows TA

## Usage
Most basic usage is to create a tcp input in Splunk and configure it with the wanted dissect sourcetype.
You can now use rdump from the Dissect suite to push data to the Splunk server tcp port. See Dissect documentation on how to use rdump.
(https://docs.dissect.tools/en/stable/tools/rdump.html)

In short this boils down to:

```bash target-query <source> -f evtx | rdump -w splunk://<splunk server ip>:<configure tcp-input port> ```


## Author
Released as open source by Fox-IT (https://www.fox-it.com) part of NCC Group Plc (https://www.nccgroup.com).

Developed by the Dissect Team (dissect@fox-it.com) and made available at https://github.com/fox-it/........ [FIX URL]
contact: Github [github link] or dissect@fox-it.com

## License
License terms: AGPL3 (https://www.gnu.org/licenses/agpl-3.0.html).
