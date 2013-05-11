Bootstrap Calendar
=================
The aim of this plugin is to have a simple calendar to show events using Bootstrap. It is also possible to display different periods on the calendar and to specify their classes (css).

For sure it can be improved, and you are welcome to do it!


Requisites
==========

+ Bootstrap (http://github.com/twitter/bootstrap)
+ jQuery (http://jquery.com/)


Quick start
===========

<pre>
    var evnts = function(){
              return {
                      "event":
                          [
                               {"date":"01/25/2013","title":"your title"}
                              ,{"date":"02/01/2013","title":"your title"}
                          ]
                      }
          };
          
    var periods = function(){
              return {
                      "period":
                          [
                               {"dtstart":"05/10/2013","dtend":"05/25/2013","class":"your-css-class"}
                              ,{"dtstart":"11/26/2013","dtend":"12/04/2013","class":"your-css-class"}
                          ]
                      }
          };

    $('element_to_render_calendar').Calendar({ 'events': evnts, 'periods': periods,
        'weekStart': 1 })
        .on('changeDay', function(event){ alert(event.day.valueOf()); })
        .on('onEvent', function(event){ alert(event.day.valueOf()); })
        .on('onNext', function(event){ alert("Next"); })
        .on('onPrev', function(event){ alert("Prev"); })
        .on('onCurrent', function(event){ alert("Current"); });

<div id="calendar"></div>
</pre>


Parameters
==========

<pre>
weekStart: 1|2|3|4|5|6|7

msg_days: Text for week days. Default: ["Su", "Mo", "Tu", "We", "Th", "Fr", "Sa"]

msg_months: Text for months. Default: ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]

msg_today: Text for 'Today' button. Default: 'Today'

msg_events_header: Text for events header. Default: 'Events Today',

events: Events to show in the calendar. Format: {"event":[{"date":"01/25/2013", "title":"title 1"}]}

periods: Periods to show in the calendar. Format: {"period":[{"dtstart":"05/10/2013","dtend":"05/25/2013","class":"your-css-class"}]}
</pre>
