# P3 project
Implementaiton of a site mockup to select one restaurant and order a menu in this restaurant.
- Main page index.html allows selection of the restaurant.
- Restauranti.html pages allow the selection of the meal in the selected restaurant.

Structure of these pages are detailled below:
# index.html : welcome page
## body                                                            
- header                                                             
- main                                                          
    - location                                                              
    - introduction                                                          
    - operation                                                             
    - restaurants article                                                   
- footer                                                                   
### header
- link to main page is deactivated as already on main page
- website logo. 
### main
- location
    - map icon
    - area name for restaurants list
- introduction : summary of site objective
- operation
    - title
    - operation steps list : 3 not clickable buttons for each step of the process. it's a row flex box w/ wrap.
        - operation step : icon + steps description + number in circle
- restaurants article
    - title
    - restaurants list : 4 clickable restaurant cards. it's it a row flex box w/ wrap
        - restaurant card : main part is a link including restaurant picture and restaurant legend (name + area).  
        The new  banner ("Nouveau") is displayed in :after of card having --is-new class variant.  
The is-favorite heart is obtained using the label of an hidden checkbox. The label includes 2 hearts displayed alternativaly depending on checkbox state. This is done in a form following the anchor (form not authorized as link child). 
- footer  
It's common to all pages and includes 4 links.
	- The 3 first are dummies and move to top page.
	- The 4th one is mailto, and open default mailer to write mail to "contact@ohmyfood"                                                         
- loading spinner  
It's at the end of the page to cover everithing.  
During animation, scrolling is disabled by hidding body overflow.  
Refer to css for annimation explanations.

### Responsiveness
Responsiveness consider 4 breakpoints, separating 5 sizes of screen:

- mobile (and below) : the given mockup is stricktly followed. 
- small-tablet : addition of a max-width to stop the width growth of operation and 
    restaurant list to avoid too much flattening of operation steps and restaurant cards.  
	Footer remains left justified
- tablet : max-width is removed, operations steps are displayed side by side with text on 2 lines, and restaurant cards are displayed in a 2 by 2 table.  
Footer title is centered and links are displayed as 2 by table.
- laptop : same a tablet except that the restaurant cards are all displayed side by side on one row.  
Footer title centered, all linsk a displyed on one line.
- desktop (and above) : same a laptop with reintroduction of max-width too flattened of operaton steps and restaurant cards.  
Footer : not changed.

This behavior is obtained by playing only on the width of the operation steps and restaurant cards with one flex box configuration.                
for small-tablet and desktop, a max-width of small-tablet and desktop breakpoint is used to limit width of operation and restaurant list.

# restauranti.html : restaurant #i menu 
Structure is common for the 4 restaurants, only texts are changed. Only exception is for restaurant2 "La note enchantée" for which a 4th starter is added.      
## body 
- header
- banner
- main
	- restaurant-info
	- menu
 	- launch-command button
- footer                                                               
### header
- link to main page is active to go back to main page
- website logo. 
### banner
Image of the restaurant
### main
- restaurant info
    - restaurant name
    - is favorite heart icon
- menu: it includes 3 chapters starter, main and dessert. It's a flew box w/ wrap. Each menu item, chapter or course card, has it own id for animation. Each chapter includes:
	- a header with title and underline
	- a list of 3 or 4 courses. each course card includes 3 parts in a row:
		- course description with title and subtitle
        - price
        - check-mark  
        it's a row flex box w/o wrap and w/o shrink. At initial stage, there is no space to display check-box.   During annimation, description width is reduced to allow appearence of the check-box.  
		Elipsis is used to avoid text wrap and ... appearance.
- operation
    - title
    - operation steps list : 3 not clickable buttons for each step of the process. it's a row flex box w/ wrap.
        - operation step : icon + steps description + number in circle
- restaurants article
    - title
- launch command button : no specific action performed for this mockup, neverthelesse cursor is "pointer" during hover, to show that it is clickable.
### footer 
Same as index.html.

### Responsiveness
Same 4 breakpoints are considered.

- Mobile follows stricly the given mockup.
- small-tablet : banner height is slightly increased, restaurant name is centered, a max-width is added to stop the growth of menu width to avoid too much flattening of course cards.
- Tablet : the banner height is slightly increased, restaurant name is kept centered, max-width is removed as starter and main chapters are displayed side by side, dessert one is centered below.
- Laptop : same a tablet except that the 3 chapters are displayed side by side.                                                                   
- Destop : same a laptop with re-introduction of max-width to avoid too flattened courses cards.                                                           

For restaurant name (left justified or centered), justify-content is changed from space-around to space-between for mobile only.
For the menu, the behavior is obtained by playing only on the width of menu chapters with one flex box configuration.
A max-width of small-tablet and desktop breakpoint is used to limmit menu width growth.