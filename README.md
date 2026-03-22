## Voyage Line City Transit
_________________________________________________________________________________________
<img width="908" height="508" alt="1 Landing page" src="https://github.com/user-attachments/assets/c56d0cf5-07ae-4f67-8767-690dfcb8abc6" />
## LANDING PAGE
1️⃣   **Landing Page Dashboard– Branding & Navigation Layer** 

What This Page Represents

This is not an analytical dashboard — it is the executive entry point into the transit analytics ecosystem.

It establishes:

•	Brand identity: Voyage Line City Transit

•	Visual theme: modern, urban mobility

•	**Navigation structure:**

o	Landing Page (active)

o	Details

o	Metrics

•	Filter capability preview: Filter by Route Name

**Business Story**

This page communicates that:

•	The organization is customer-centric and mobility-focused.

•	The analytics solution is structured and role-based.

•	Users can drill into operational and performance views.

Strategic Purpose

This page:

•	Reduces cognitive overload

•	Creates a professional BI experience

•	Encourages guided data exploration

•	Aligns stakeholders around one unified analytics system

Think of this as the BI portal front door.

_____________________________________________________________________________________________________________
## DASHBOARD 2
<img width="901" height="506" alt="2 Details Dashboard" src="https://github.com/user-attachments/assets/1c7b0440-93d3-48db-9021-04e4e843c6e4" />

2️⃣   **Operations & Performance Overview Dashboard : Details** 

(High-Level Executive Summary)

This is the KPI command center.

**Core KPIs**

**Metric	Value	Interpretation**

Total Rider-- 6,587	Moderate overall demand

Avg Riders per Trip-- 32.94	Decent seat occupancy

Total Trips-- 200	Operational scale

Total Revenue-- 183K	Revenue-generating efficiency

**Story:**

The transit system is operating consistently with moderate utilization and solid revenue generation.
__________________________________________________________________________________________________________________
**Trip Time Trend**

The time-series chart shows:

•	Significant volatility during operational hours

•	Peaks around morning and evening windows

•	Clear rush-hour movement pattern

**Operational Insight:**

Demand is commuter-driven and predictable in structure but fluctuates within peak bands.
_______________________________________________________________________________________________________________
**Peak & Down Hours**

•	Peak Hour: 8:57 PM (80 passengers)

•	Down Hour: 7:50 PM (15 passengers)

Story:

Evening usage is dominant. There is a strong late-day commuter or event-driven demand pattern.
____________________________________________________________________________________________________________________
**Time Range Distribution**

Highest ridership blocks:

•	9:00 AM – 11:59 AM → 1.4K
•	12:00 PM – 2:59 PM → 1.3K
•	9:00 PM – 11:59 PM → 1.1K

**Insight:**

Mid-morning and late evening windows drive traffic.

This suggests:

•	Office commuters

•	Students

•	Possibly airport routes
______________________________________________________________________________________________________________
**Route Performance**

Busiest Route:   East-West Express

Least Busy: South Line

Story:

Route demand is uneven.

Capacity rebalancing opportunity exists.
________________________________________________________________________________________________________________
**Weekly Distribution**

•	Highest: Sunday & Monday

•	Average: 941 riders

**Insight:**

Weekend demand is strong — not purely corporate commuter traffic.

Likely mixed-use transit network.
________________________________________________________________________________________________________________
**Bus Utilization**

•	Properly Utilized: 3.0K

•	Overutilized: 2.8K

•	Underutilized: 0.8K

**Operational Conclusion:**

Fleet allocation needs optimization.

Overutilization risk → service degradation.

Underutilization → revenue inefficiency.
___________________________________________________________________________________________________________________________
**Yearly Distribution**

YoY Change: -83.50%

This is critical.

Story:

Either:
•	Major disruption occurred

•	Data coverage difference between years

•	Policy or external factor impact

This is an executive red flag.
________________________________________________________________________________________________________________________

This dashboard tells a story of:

A transit system that is operationally active and revenue-generating, but facing uneven route performance and significant year-over-year decline.

It supports:

•	Executive review

•	Fleet allocation decisions

•	Capacity planning

•	Revenue optimization strategy
_______________________________________________________________________________________________________________________
## DASHBOARD 3
<img width="902" height="503" alt="3 Metrics Dashboard" src="https://github.com/user-attachments/assets/56c4b439-4492-4f30-ba22-e818386ff10c" />

3️⃣**Rider Demographics & Route Analysis: Metrics**
(Operational Intelligence Page)
This is a segmentation and optimization dashboard.
________________________________________________________________________________________________________________________
**Top-Level Metrics**

•	Total Riders: 6,587

•	Avg Rider per Trip: 32.94

•	Total Trips: 200

•	Revenue: 183K

This ensures KPI continuity across pages.
_______________________________________________________________________________________________
**Route Distribution for Riders**

Top Routes:

•	East-West Express (1,322)

•	Central Line (1,271)

•	Airport Express (754)

Bottom:

•	South Line (185)

Story:
Traffic concentration is heavy on 2–3 key routes.

Long-tail routes may need:

•	Marketing

•	Schedule adjustment

•	Possible route redesign
________________________________________

Bottom Performing Buses

Underperformers:
•	Bus 34

•	Bus 13

•	Bus 14

•	Bus 19

•	Bus 26

•	Bus 39

Operational Implication:

This enables:
•	Targeted maintenance review

•	Route reallocation

•	Driver performance evaluation

•	Schedule optimization

This is actionable BI.
________________________________________
**Passenger Gender Distribution**

•	Male: 32%

•	Female: 35%

•	Other: 33%

Insight:

Balanced gender representation.

Transit system is inclusively utilized.
________________________________________
**Age Group Distribution**

Highest Segment:

•	30–39 years (1,474 riders)

Followed by:

•	50–59

•	40–49

Story:

Core users are working professionals.

Less senior citizen penetration.

Youth (10–19) moderate.

Marketing and scheduling can be tailored to working-age commuters.
_________________________________________________________________________________________________________________________
**Occupation Distribution**
Top:

•	Other

•	Professional

•	Self-Employed

Lower:

•	Retired

•	Student

Interpretation:

Strong workforce commuter base.

Transit is economically driven, not student-dominant.
_______________________________________________________________________________________________________________________________
**Peak Hours by Occupation**

Different occupations peak at different times.

Example:

•	Professional peak ~ 11:41 AM

•	Retired ~ 8:50 AM

•	Student ~ 8:57 PM

Insight:

Different behavioral segments.

Advanced opportunity:

•	Demand-based scheduling

•	Occupation-targeted passes
__________________________________________________________________________________________________________________________________

Average Age: 43

Confirms:
Mid-career demographic dominance.
_____________________________________________________________________________________________________________________________
## CONCLUSION
**Strategic Business Story Across All Dashboards:**

When combined, the full story is:

Voyage Line City Transit is a moderately scaled urban transit network with:

•	Concentrated route demand

•	Strong working-age commuter base

•	Evening and mid-morning peak windows

•	Some fleet inefficiency

•	Significant year-over-year decline risk

Opportunities:

1.	Route Rationalization

2.	Fleet Rebalancing

3.	Occupation-Based Pricing

4.	Demand Forecasting Model

5.	Revenue Optimization Strategy

6.	Underutilized Route Marketing Campaign

## DAX
```
Date = 
VAR Maxdate =YEAR(MAX(FactTable_ridership[Date]))
VAR Mindate =YEAR(MIN(FactTable_ridership[Date]))
RETURN
ADDCOLUMNS(
    FILTER(
    CALENDARAUTO(),
    YEAR([Date])>=Mindate &&
    YEAR([Date])<=Maxdate
    ),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date],"mmm"),
    "MonthNum", MONTH([Date]),
    "Day", DAY([Date]),
    "Weekday", FORMAT([Date],"ddd"),
    "Week_num",WEEKDAY([Date]),
    "Quarter","Q-"&QUARTER([Date]),
    "WeekType", IF(WEEKDAY([Date])=1,"Weekend",IF(WEEKDAY([Date])=7,"Weekend","Weekday")),
    "WK of Month",
            VAR FirstDayOfMonth = DATE(YEAR([Date]), MONTH([Date]), 1)
            VAR DaysInMonth = DAY(EOMONTH([Date], 0))
            VAR CurrentDate = [Date]
            VAR DaysFromStart = INT(CurrentDate - FirstDayOfMonth) + 1
            RETURN 
            "Week-"&
                CEILING(DaysFromStart / 7, 1),
                 "Time", FORMAT([Date], "hh:mm AM/PM")
           
)
```

```
Age Group label = 
VAR _AgeGrouppct=DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_demographics[Age Bucket])))
VAR _Yaxis= SELECTEDVALUE(Lookup_demographics[Age Bucket])
VAR _pctvalue= FORMAT(_AgeGrouppct,"0.0%")
RETURN
_Yaxis & " ↕ "& _pctvalue
```
```
AgeGrouppct = DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_demographics[Age Bucket])))
```
```
Average Rider Per trip = DIVIDE([Total Riders(passengers)], COUNTROWS(FactTable_ridership))
```
```
Avg Rider Age = AVERAGE(Lookup_demographics[Age])
```
```
Blank measure = 300
```
```
Blank measure2 = 0
```

```
BottomN = 
VAR _Ranking =
    RANKX(
        ALL(Lookup_buses[BusNumber]),
        [Total Riders(passengers)],
        ,
        ASC,
        DENSE
    )
RETURN
IF(_Ranking <= 5, [Total Riders(passengers)], BLANK())
```
```
Busiest Route = 
VAR _TotalPassengers_perroute= 
SUMMARIZE(
    Lookup_routes, 
    Lookup_routes[RouteName],
    "Total Passengers", sum(FactTable_ridership[NumberOfRiders])
    )
VAR _TopRoute= TOPN(1,_TotalPassengers_perroute, [Total Passengers], DESC)
RETURN
MAXX(_TopRoute,Lookup_routes[RouteName])
```
```
Caption = 
IF( SELECTEDVALUE('Dynamic TopN'[Dynamic TopN Order])=0, 
"Under Performing Buses are selected",
"Top Performing Buses are selected")

```
```
CF Age Group label = 
VAR _AgeGrouppct=DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_demographics[Age Bucket])))
RETURN
IF(_AgeGrouppct>0.19, "#FO9383","#CCCCCC")

```
```
CF Occupation = 
VAR _Occupationpct=DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_demographics)))
RETURN
IF(_Occupationpct>0.19, "#E1135F","#C7D8ED")
```
```
CF Route = 
VAR _Routepct=DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_routes)))
RETURN
IF(_Routepct>0.19, "#E1135F","#C7D8ED")
```
```
CF Weekday = 
VAR _OverallAvg= CALCULATE(DIVIDE([Total Riders(passengers)], DISTINCTCOUNT('Date'[Weekday])), ALL('Date'))
RETURN
IF([Total Riders(passengers)]>_OverallAvg,1,0)
```
```
CF YoY check = IF([YoY change]<0,"#E91A63","Green")
Down Hour Of Operation = 
VAR _TotalPassengers_perroute= 
SUMMARIZE(
    FactTable_ridership, 
    FactTable_ridership[Time],
    "Total Passengers", sum(FactTable_ridership[NumberOfRiders])
    )
VAR _DownTime= TOPN(1,_TotalPassengers_perroute, [Total Passengers], ASC)
RETURN
MAXX(_DownTime,FactTable_ridership[Time])
```
```
Female Chart = 
VAR _Female= DIVIDE(CALCULATE([Total Riders(passengers)], Lookup_demographics[Gender]="Female"), [Total Riders(passengers)])
VAR _No_of_icons= 10
VAR _No_of_fillicons= _Female*_No_of_icons
VAR _No_of_empty_icons= _No_of_icons- _No_of_fillicons
VAR _filledicons= "●"
VAR _emptyicons= "○"
VAR _bars= REPT(_filledicons,_No_of_fillicons) & REPT(_emptyicons,_No_of_empty_icons)

RETURN
_bars
```
```
Least Busiest Route = 
VAR _TotalPassengers_perroute= 
SUMMARIZE(
    Lookup_routes, 
    Lookup_routes[RouteName],
    "Total Passengers", sum(FactTable_ridership[NumberOfRiders])
    )
VAR _TopRoute= TOPN(1,_TotalPassengers_perroute, [Total Passengers], ASC)
RETURN
MAXX(_TopRoute,Lookup_routes[RouteName])
```
```
Male Chart = 
VAR _Male= DIVIDE(CALCULATE([Total Riders(passengers)], Lookup_demographics[Gender]="Male"), [Total Riders(passengers)])
VAR _No_of_icons= 10
VAR _No_of_fillicons= _Male*_No_of_icons
VAR _No_of_empty_icons= _No_of_icons- _No_of_fillicons
VAR _filledicons= "●"
VAR _emptyicons= "○"
VAR _bars= REPT(_filledicons,_No_of_fillicons) & REPT(_emptyicons,_No_of_empty_icons)

RETURN
_bars
```
```
Occupation label = 
VAR _Occupationpct=DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_demographics[Occupation])))
VAR _Yaxis= SELECTEDVALUE(Lookup_demographics[Occupation])
VAR _indicator= IF(_Occupationpct>0.19,"✔","❌")
VAR _separtor= IF(_Occupationpct>0.19,"|")
VAR _pctvalue= FORMAT(_Occupationpct,"0.0%")
RETURN
_Yaxis & "|" & _pctvalue &_separtor &_indicator 
```
```
Other Chart = 
VAR _Other= DIVIDE(CALCULATE([Total Riders(passengers)], Lookup_demographics[Gender]="Other"), [Total Riders(passengers)])
VAR _No_of_icons= 10
VAR _No_of_fillicons= _Other*_No_of_icons
VAR _No_of_empty_icons= _No_of_icons- _No_of_fillicons
VAR _filledicons= "●"
VAR _emptyicons= "○"
VAR _bars= REPT(_filledicons,_No_of_fillicons) & REPT(_emptyicons,_No_of_empty_icons)

RETURN
_bars
```
```
Pct Female = DIVIDE(CALCULATE([Total Riders(passengers)], Lookup_demographics[Gender]="Female"), [Total Riders(passengers)])
```
```
Pct Male = DIVIDE(CALCULATE([Total Riders(passengers)], Lookup_demographics[Gender]="Male"), [Total Riders(passengers)]) ```
```
```
Pct Other = DIVIDE(CALCULATE([Total Riders(passengers)], Lookup_demographics[Gender]="Other"), [Total Riders(passengers)])
```
```
Peak Hour Of Operation = 
VAR _TotalPassengers_perroute= 
SUMMARIZE(
    FactTable_ridership, 
    FactTable_ridership[Time],
    "Total Passengers", sum(FactTable_ridership[NumberOfRiders])
    )
VAR _PeakTime= TOPN(1,_TotalPassengers_perroute, [Total Passengers], DESC)
RETURN
MAXX(_PeakTime,FactTable_ridership[Time])
```
```
Peak Hours(Occupation) = 
VAR _professional_PH =
    SUMMARIZE(
        FactTable_ridership,
        FactTable_ridership[Time],
        "Total Passengers",
            CALCULATE(
                [Total Riders(passengers)],
                Lookup_demographics[Occupation] = "Professional"
            )
    )
VAR _TopProfessional =
    TOPN(1, _professional_PH, [Total Passengers], DESC)
VAR _professional =
    MAXX(_TopProfessional, FactTable_ridership[Time])
VAR _student_PH =
    SUMMARIZE(
        FactTable_ridership,
        FactTable_ridership[Time],
        "Total Passengers1",
            CALCULATE(
                [Total Riders(passengers)],
                Lookup_demographics[Occupation] = "Student"
            )
```
```
Route label = 
VAR _Routepct=DIVIDE([Total Riders(passengers)], CALCULATE([Total Riders(passengers)], ALL(Lookup_routes)))
VAR _Yaxis= SELECTEDVALUE(Lookup_routes[RouteName])
VAR _indicator= IF(_Routepct>0.19,"✔","❌")
VAR _separtor= IF(_Routepct>0.19,"|")
VAR _pctvalue= FORMAT(_Routepct,"0.0%")
RETURN
_Yaxis & "|" & _pctvalue &_separtor &_indicator 
```
```
TopN = 
VAR _Ranking =
    RANKX(
        ALL(Lookup_buses[BusNumber]),
        [Total Riders(passengers)],
        ,
        DESC,
        DENSE
    )
RETURN
IF(_Ranking <= 5, [Total Riders(passengers)], BLANK())
```
```
Total bus capacity = sum(Lookup_buses[Capacity])
```
```
Total Buses = DISTINCTCOUNT(FactTable_ridership[BusID])
```
```
Total Revenue = SUMX(FactTable_ridership, RELATED(Lookup_routes[TripFee])*FactTable_ridership[NumberOfRiders])
```
```
Total Riders(passengers) = sum(FactTable_ridership[NumberOfRiders])
```
```
Total Trips = COUNTROWS(FactTable_ridership)
```
```
V Down Hour Of Operation = 
VAR _TotalPassengers_perroute= 
SUMMARIZE(
    FactTable_ridership, 
    FactTable_ridership[Time],
    "Total Passengers", sum(FactTable_ridership[NumberOfRiders])
    )
VAR _DownTime= TOPN(1,_TotalPassengers_perroute, [Total Passengers], ASC)
RETURN
MAXX(_DownTime,[Total Passengers])
```
```
V Peak Hour Of Operation = 
VAR _TotalPassengers_perroute= 
SUMMARIZE(
    FactTable_ridership, 
    FactTable_ridership[Time],
    "Total Passengers", sum(FactTable_ridership[NumberOfRiders])
    )
VAR _PeakTime= TOPN(1,_TotalPassengers_perroute, [Total Passengers], DESC)
RETURN
MAXX(_PeakTime,[Total Passengers])
```
```
YoY change = 
VAR Curryear= 2024
VAR _currentyearrides= CALCULATE([Total Riders(passengers)], YEAR(FactTable_ridership[Date])=Curryear) 
VAR _prevyearrides= CALCULATE([Total Riders(passengers)], YEAR(FactTable_ridership[Date])=Curryear-1) 
VAR _result= 
IF( NOT ISBLANK(_currentyearrides) && NOT ISBLANK(_prevyearrides), DIVIDE(_currentyearrides-_prevyearrides,_prevyearrides,0))

RETURN
IF(_result<>BLANK(),_result,0)
```
```
YoY check = IF([YoY change]<0,"▼","▲")
```

```
Parameter
Dynamic TopN = {
    ("Bottom Buses", NAMEOF('measures (2)'[BottomN]), 0),
    ("Top Buses", NAMEOF('measures (2)'[TopN]), 1)
}
```
