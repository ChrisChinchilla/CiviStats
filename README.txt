Adds API calls to allow for easy calling and rendering of creation stats in CiviCRM for display in a website's front end.

This project was started as part of Random Hacks of Kindness 2012

So far, here's what you can do:


All contributions and how many
{crmAPI var="StatsS" entity="Stats" action="totalcontributions" sequential="1" }
Amount: {$StatsS.total|crmMoney}
Count: {$StatsS.count}

Yearly contributions and how many
{crmAPI var="StatsS" entity="Stats" action="yearlycontributions" sequential="1" }
Amount: {$StatsS.total|crmMoney}
Count: {$StatsS.count}

Number of members
{crmAPI var="StatsS" entity="Stats" action="current" sequential="1" }
{$StatsS}