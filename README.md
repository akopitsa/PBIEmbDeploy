# PBIEmbDeploy
This Powershell script xplat allow you to :
* Install the Azure CLI and PowerBI CLI on your machine
* Deploy a new Power BI Embedded resource on your Azure Subscription
* Create a Workspace in the PBI Collection
* Import a PBIX file (Only One for now)

All in one command, the deploy.ps1 file.

## Usage

1. Clone the repo : `git clone https://github.com/julienstroheker/PBIEmbDeploy`
2. Copy your .PBIX file in the myReport folder
3. Run the ./deploy.ps1 file : `powershell ./deploy.ps1 -ResourceGroupName <MyResourceGroup> -Location <Location> -PrefixName <CONTOSO> -PrefixNameEnv <DEV>`

> Note : The *PrefixName* and *PrefixNameEnv* will add a prefix at the PowerBI resource created on Azure. Ex : CONTOSO-TEST-PBI

Example :

`./deploy.ps1 -ResourceGroupName "PowerBITest" -Location "West US" -PrefixName "CONTOSO" -PrefixNameEnv "TEST"`

![](./media/OutputExample.png)

> Note : you can use two optional parameters (boolean) when you call the script : Prerequisites and Authentication

## Prerequisites

You need to have installed on your machine :
* NPM (NodeJS)
* Azure-CLI
* PowerBI-CLI

> Note : You can run `./deploy.ps1 -Prerequisites 1` to install the Azure-CLI and PowerBI-CLI packages on your machine.