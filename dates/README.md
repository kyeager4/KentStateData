# Kent State Semester Dates
This dataset contains the starting and ending dates of the Spring, Summer, Fall, and Winter semesters, beginning at the Fall 2009 semester.

## Codebook
`Semester` - (String) The name of the semester ("Fall", "Spring", "Summer", "Winter").

`StartDate` - (Date, MM/DD/YYYY) The date of the first day of the semester. Always falls on a Monday.

`EndDate` - (Date, MM/DD/YYYY) The day of the last day of the semester. Always falls on a Sunday.

## Data Source
The raw data sources came from information in PDFs on the Kent State University website.
- [University Academic Calendars 2023-2024 to 2027-2028](https://provostdata.kent.edu/roadmapweb/03/academic-calendar-AY2023-AY2027.pdf)
- [University Academic Calendars 2018-2019 to 2022-2023](http://provostdata.kent.edu/roadmapweb/03/academic-calendar-AY2018-AY2022.pdf)
- [University Academic Calendar 2014-2018](https://www.kent.edu/sites/default/files/academic-calendar-2014-2018_0.pdf)
- [University Academic Calendar 2009-2013](http://provostdata.kent.edu/roadmapweb/03/academic-calendar-2009-2013.pdf)
- [Kent State Calendars](http://www.kent.edu/calendars)

In July 2014, I transcribed the starting and ending dates for the academic years 2014 through 2018. In October 2015, I added dates for the academic year 2012-2013.

See also:

- [University Registrar - Registrar Dates by Term](http://www.kent.edu/registrar/registrar-dates-term)

### Transcription Notes
I have entered the data in such a way that the starting date of a semester will always be the Monday of the first week of classes, and the ending date will always be the Sunday at the end of finals week. In the original Kent State files, some of the given semester start dates are on Tuesday; this happens when Martin Luther King Day falls on the Monday of the first week of the semester.

The actual data pulled from the PDF documents was simply the dates corresponding to "Fall Classes Begin", "Fall Fall Final Examinations", "Spring Classes Begin", and "Spring Final Examinations". That is, the starting and ending dates for the winter and summer semesters are simply chosen to be the day after the start or end of the fall or spring semesters. (This way, the semester periods are mutually exclusive and exhaustive. Any date will be able to be classified into exactly one of the periods.)

### Motivation
1. Many of the data collection tools at the library record the date of a given transaction. It is useful to be able to classify those dates into an academic semester after the fact, so that it is easy to count the number of transactions per semester.

2. Many statistical software packages have functions that will determine the "week number" for a given date; they usually return a number between 0 or 1 to 52 or 53. However, each package has slightly different rules about when the start of a week is. For example, Excel's `WEEKNUM()` function allows you to specify what day of the week should be counted as the first day, while SPSS's `XDATE.WEEK()` function uses the weekday that the first of the year fell on (relative to the input date(s)). By having the Kent State semester dates available in a standardized way, I am able to get apples-to-apples comparisons of weekly traffic across years.

## For Future Updates
Ideas for future updates:
- Add semester dates prior to Fall 2012 (Done)
- Add semester dates prior to Fall 2009
- Add semester dates for Summer 2019 and beyond, as they are made available
- Create a complementary file with holiday dates (e.g. Veterans Day, Martin Luther King Day, holiday break, etc.)
