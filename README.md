# MDTIARMDeploy
Microsoft Defender Threat Intelligence ARM template.

Deploy this to begin ingesting the threat intelligence indicators of MDTI; official documentation on this can be found here: https://learn.microsoft.com/en-us/azure/templates/microsoft.securityinsights/2023-02-01-preview/dataconnectors?pivots=deployment-language-arm-template
and 
https://learn.microsoft.com/en-us/azure/sentinel/connect-mdti-data-connector

and with a really great video into how this product can be utilised found here: https://www.youtube.com/watch?v=meCjqoWgssg

I've put together a basic arm template which takes following key inputs;

- Location
- 
Which location your environment which you wish to deploy the TI indicators to is based in

- Subscription/Tenant/Workspace Information/Location of Workspace
- 
Basic information about your azure environment

- Base Time - Auto applied in code with utcNow()
- 
If you want to control when the lookback works from this value may be worth while editing. I've left it in as a parameter for this reason.

- lookBackPeriod
- 
Defines how long you wish to ingest indicators for as a convenient drop down(All/30 Days/7 Days)

