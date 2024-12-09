# [Endpoint Security] Are you sure that’s an invoice? 
Based on the initial findings, we discovered how the malicious attachment compromised Julianne's workstation:

    A PowerShell command was executed.
    Decoding the payload reveals the starting point of endpoint activities. 

## Investigation Guide
With the following discoveries, we should now proceed with analysing the PowerShell logs to uncover the potential impact of the attack:

    Using the previous findings, we can start our analysis by searching the execution of the initial payload in the PowerShell logs.
    Since the given data is JSON, we can parse it in CLI using the jq command.
    Note that some logs are redundant and do not contain any critical information; hence can be ignored.

## JQ Cheatsheet
jq is a lightweight and flexible command-line JSON processor. This tool can be used in conjunction with other text-processing commands. 

You may use the following table as a guide in parsing the logs in this task.

Note: You must be familiar with the existing fields in a single log.

<div>
<img src="https://github.com/Modern-Wizard/-Endpoint-Security-Are-you-sure-that-s-an-invoice-/blob/main/ss5.png" />
</div>


