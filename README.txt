This implements the Gcal_Events module in a simple manner. 

The current calendar it uses is that of gcalevents@gmail.com, which was made for demonstration purposes. 

*Notes*

Line 609 in gcal_events.module was changed from:

foreach (split("[ \n]", $calendar_ids) as $calendar_id) {

to

foreach (preg_split("[ \n]", $calendar_ids) as $calendar_id) {

to prevent an error, which is noted here: http://drupal.org/node/1809520. 