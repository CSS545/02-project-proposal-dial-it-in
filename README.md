[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8937707&assignment_repo_type=AssignmentRepo)
Hint: [Markup Guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

# Dial it in
*Justin Boyer*

*Version 1#*

## Summary of Project
*This app is an epresso companion app designed to help coffee enthusiasts make better coffee more quickly and reliably.  Users will be able to track common brewing variables in order to quickly see what adjustments can be made in order to improve pulls.  Good cups can be quickly reproduced by accessing saved settings - even if the equipment has been adjusted for different roasts.  This makes trying new coffees or switching between bags a breeze! *

## Project Analysis
### Target Audience
*The target audience is beginning to intermediate coffee enthusiasts who need to make frequent adjustments to their brew processes and decide what they like. This audience could be reached on coffee forums, cafes, and coffee tasting subscriptions (eg trade)*

### Primary Purpose
*The primary purpose is to allow coffee enthusiast to save brew configurations for specific coffee roasts and quickly recreate cups they liked*

### Value Proposition
*Dialing in espresso is a daily process for any professional barista and is an essential part of what makes cafe espresso so consistant.  Home coffee enthusiast have a unique set of problems when trying to dail in their cups at home. First, cafe's typically order in bulk and stick to a handful of roasts leaving settings relatively constant from day to day.  Conversely, in order to brew fresh beans consumer bags are much smaller - often less than a pound.  Additionally, home brewers are more likely to experiement with different roasts and brands. Pulling 3-5 shots to find the right balance is a time consuming process that uses a larger percentage of these smaller bags and every roast is different and may require different settings. This app aims to simplify this process, drawing attention to which settings to change and saving "roast profiles" to help home baristas remember settings when switching between different bags of coffee.*

### Success Criteria
*Success can by the number of weekly users with more than one roast profile saved. This is a better metric than daily users because if the app is working well it should reduce the number of times a user needs to spend time dialing in. This metric should capture users that benefit the most from saving their settings *

### Competitor Analysis
*iBrewCoffee: This app is very detailed and focuses primarily on the coffee itself.  Pros: very flexible allows for nearly any type of equipment, links to roasteries all over the world, freemium service. Cons: All the customization options make it very complicated.  It is very overwhelming.*

### Monetization Model
*Ads for local coffee roasters, coffee equipment, coffee subscriptions, coffee sales*

### Initial Design
*MVP must have 3 essential features:
1) Option to manually input espresso settings including dose, yield, grind size, and brew time.
2) Save roast profile to local storage
3) Retrieve roast profile for viewing
*

### UI/UX Design
* Home menu with two buttons to create new profile or load saved profile.  
On the 'create' page: Large easy to press buttons that allow user input on press. Timer button, add photo option, dose/yeild calculator, save button. It would also be nive to have a rating system/flavor profile (maybe P1 or P2).  The page for save profiles will be a list with the photo on the left and a peek at the most important stats in line on the row. Click to enter into a details page. (see included diagram) *

### Technical Architecture
*Internal storage: Ideally I'd like a non-relational database. I'll try to use firebase, but if it is cost prohibative I'll use Core Data even though it is a suboptimal solution for my use case.

The app will have 4 basic pages with a simple heirarchy structure
      -Create new
Home < 
      -Retreive saved -view details

Using non-local storage will require user verification. I plan to use the integrated firebase options in that case.

Roast profiles will be saved as JSON. I don't plan to implement any features where complex querries will be advantageous.
*

## Challenges and Open Questions
*Camera permissions

 Saving and retrieving photos associated with roast profiles

 User authentication and storage - I'm not sure how firebase works or if it is the right choice here.

 How to help users dial in effectively - ie informitive user inputs for taste.
*

## Mockup & UXflowchart
https://lucid.app/lucidchart/46492874-adab-4e33-91a9-84e6c29cf3b0/edit?viewport_loc=-554%2C-516%2C4096%2C1980%2C0_0&invitationId=inv_58ec09ab-8adc-4293-86ac-94f150b00998
(screenshots incleded on the branch too)

## Happy Path
1) Enter in settings for current brew attempt
2) If you liked the brew, save the settings
3) When you are ready to make coffee look through your saved brews
4) Find the saved settings for you current brand/roast etc

## Success criteria focus
The success criteria focused on users that access their saved brews. 
To facilitate this I designed my interface to show users that value fulfillment from the
homepage and list enough saved vaules to quickly see what you have with the option to click 
for more detail once you find what you are looking for.

## Value
The main value my app provides is the ability to quickly remake cups of coffee that you liked
after carefully dailing in your shot to your liking