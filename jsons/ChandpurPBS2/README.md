# JSON Guidline

## MenuList JSON

This JSON file contains Home Grid items & details, home notifications, drawer items, and Sub menu lists under the grid item.

The app fetch this JSON file every time after launching if there is an active internet connectivity.

``` js
  {
    "version": 1.00, // Double value - if person list is updated then you must increment this version in order to sync updated data in the app.
    "home_notification": [ 
    /* notification to show in home activity of the app
     there could be multiple notification at a time based on view_type */
      {
        "type": "marquee", // marquee- scrolling bottom text notification & popup- popup notification using dialog
        "title": "ডিজিটাল উদ্ভাবনী মেলা ২০২২", // title is mendatory for popup but optional for marquee (btw always recommended to add a title)
        "title_color": "#AA4A44", // marquee text body color code
        "image_url": "", // for popup notification only - for marquee it should keep empty
        "body": "", // notification message (to show a notification on home page then you must put something in body tag)
        "link": "", // for popup notification only - for marquee it should keep empty
        "date": "18/11/2022", // for popup notification only - for marquee it is not mandatory
        "view_type": 1 // integer value - case 1 = everybody will see the notificaiton & case 2 = consumer won't see the notification (officials only)
      }
    ],
    
    "home_menu_offices":[
      // Home page grid view item is listed here
      {
        "order_no": 4, // Integer value grid item order
        "id": 4, // Interger value - grid item id
        "title": "সমিতি বোর্ড", // String title for grid item
        "icon": "https://raw.githubusercontent.com/shhridoy/MY-API-SERVER/master/images/chandpurpbs2/Icon4.png", // Grid item icon url
        "sub_menu": [], /* sub_menu is an Integer type Array List which contains sub menu item ids like [1,2,3,4] etc. 
            ** Officials will see this list. **
                case 1: 
                    "sub_menu": [] (there is no sub menu item under this grid item)
                case 2:
                    "sub_menu": [1,2,3,6,7] (sub_menu_sections item id list)
        */
        "sub_menu_1": [], /* It is similar to sub_menu
            sub_menu_1 is used only for consumer to show sub_menu list differently
            ** Consumers will see this list. **
        */
        "details_link": "" /* 
            contains String text/HTML text/URL
            case 1:
                "details_link": "This is a text"
                ** Text open in internal webview activity
            case 2:
                "details_link": "<h1>This is HTML text header.</h1><br><p>This is body</p>"
                ** HTML text open in internal webview activity
            case 3: 
                "details_link": "https://raw.githubusercontent.com/shhridoy/MY-API-SERVER/master/jsons/ChandpurPBS2/notifications.json" 
                ** Notification URL to open notification activity
            case 4:
                "details_link": ""
                ** If keep empty that means there is a sub menu list or persons list available under this grid item.
        */ 
       
        // If sub_menu array list and details_link keep empty that means there is a direct person list under this grid item.
       
        // Always keep details_link empty when there is a sub_menu/sub_menu_1 item available.
      }
    ]
  }


