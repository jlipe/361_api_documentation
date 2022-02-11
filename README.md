# Headline Service API Reference
## Base URL
`https://s9goa8paxj.execute-api.us-east-1.amazonaws.com`

### Headlines Endpoint
`GET /headlines`

#### NOTE: There must be a query string with sources in it. So `/headlines` must be followed with a `?sources=`

| Paramater | Description | Optional |
| ------ | ------ | ------ |
| Sources | Comma seperated list of sources | No
| Limit | Per source article limit | Yes (defaults to 5)

#### NOTE: The sources must be capatlized and spelled exactly as described in the possible sources below
#### The comma seperated format would look like sources=DailyFX,NY+Times,Mother+Jones
#### Spaces in the source name are replaced with a plus sign

#### Possible Sources
| Source |
| ------ |
| Fox News |
| CNN | 
| Breitbart |
| Mother Jones | 
| NY Times |
| DailyFX | 
| CNBC |
| Financial Times |
| Crypto News |

#### Response
[
    {"headline": "Investigators Find Gaps in White House Logs of Trump’s Jan. 6 Calls",
    "source": "NY Times",
    "time", "2022-02-10T21:45:14.105727"},
    {...},
    {...}
]


#### Example Request
`GET https://s9goa8paxj.execute-api.us-east-1.amazonaws.com/headlines?sources=DailyFX&limit=3`

#### Example Response
[
    {
    headline: "Nasdaq 100 Dives as 40-Year High Inflation Boosts Case for Aggressive Rate Hikes",
    source: "DailyFX",
    time: "2022-02-10T22:00:20.320921"
    },
    {
    headline: "Gold Price Stages Five-Day Rally for First Time Since November",
    source: "DailyFX",
    time: "2022-02-10T21:30:16.976095"
    },
    {
    headline: "Australian Dollar Technical Analysis: Failure at Significant Resistance - Setups in AUD/JPY, AUD/USD",
    source: "DailyFX",
    time: "2022-02-10T20:00:16.168286"
    }
]