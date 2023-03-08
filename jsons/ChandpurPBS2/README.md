# JSON Guidline

# Menu JSON

``` js
  {
    "version": 1.00, // double value- if person list is updated then you must increment this version in order to sync updated data in the app
    "home_notification": [ 
    // notification to show in home activity of the app
    // there could be multiple notification at a time based on view_type
      {
        "type": "marquee", // marquee- scrolling bottom text notification & popup- popup notification using dialog
        "title": "ডিজিটাল উদ্ভাবনী মেলা ২০২২", // title is mendatory for popup but optional for marquee (btw always recommended to add a title)
        "title_color": "#AA4A44", // marquee text body color code
        "image_url": "", // for popup notification only - for marquee it should keep empty
        "body": "", // notification message (to show a notification on home page then you must put something in body tag)
        "link": "", // for popup notification only - for marquee it should keep empty
        "date": "18/11/2022", // for popup notification only - for marquee it is not mandatory
        "view_type": 1 // int value - case 1 = everybody will see the notificaiton & case 2 = consumer won't see the notification (officials only)
      }
    ],
    
    "home_menu_offices":[
      // home page grid view item is listed here
      {
			  "order_no": 4,
			  "id": 4,
			  "title": "সমিতি বোর্ড",
			  "icon": "https://raw.githubusercontent.com/shhridoy/MY-API-SERVER/master/images/chandpurpbs2/Icon4.png",
			  "sub_menu": [],
			  "sub_menu_1": [],
			  "details_link": ""
		  }
    ]
  }


