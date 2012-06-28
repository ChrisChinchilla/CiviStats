CiviStats v1
This is a proposed API change to allow for easy calling and rendering of creation stats in CiviCRM for display in a website's front end.

This project was started as part of Random Hacks of Kindness 2012

Add 'stats.php' to api/v3/ and you can use the commands listed below.

For the git heads, unless anyone smarter with Git than me can tell me how to make this smoother, add this as a submodule into your civi installation and then move the 'stats.php' up one level…

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