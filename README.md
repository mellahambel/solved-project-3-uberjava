Download Link: https://assignmentchef.com/product/solved-project-3-uberjava
<br>
<strong>PURPOSE: Learn more designing multiple classes, packages, accessing a Web site, parsing Strings, creating your own Exception, and being an UberJava driver. </strong>Do all your work in the Github repository available via the link <strong><u>https://classroom.</u></strong><strong>g<u>ithub.com/a/0TtDL9YT</u></strong><strong><u> (https://classroom.</u></strong><strong>g<u>ithub.com/a/0TtDL9YT)</u></strong>

(There is one package location that you’ll need from there)

In this assignment, you are to pretend that you, James Naismith and Prateek are all Uber Drivers!  Each of you get fares and drive people to their destination (all around California). You must keep track of all the trips that you take, how much money that you make, and your rating.

Here is how UberJavaDriver works:

<ol>

 <li>You instantiate all three Drivers – you, James Naismith, and Prateek – each with their name and a Car</li>

</ol>

Note: We’ll talk about in class how you access a Web page – it is pretty much like reading a file.

Sometimes Surge Pricing and sometimes Double Surge Pricing is in effect.  In those cases, you get bigger fares. The above fare line will be followed with a line that looks like this:

<strong>SURGE PRICING IN EFFECT: Fare is $236.26</strong>

OR

<strong>DOUBLE SURGE PRICING IN EFFECT: Fare is $254.55</strong>

<ol start="5">

 <li>In order to figure out your costs you should get the information that is available at the provided link.</li>

</ol>

https://www.cs.usfca.edu/~dhalperin/uberdistance.cgi?rideNumber=&lt;rideNumber&gt; where the rideNumber is what was provided in the nextFare request.

For example, for ride number 1502587145, the return is

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/12/612.png?w=980&amp;ssl=1" class="alignleft lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="alignleft" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/12/612.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>
















TO ALSO get the miles and distance from your current location, add the following to the end of the request: <em>&amp;start=</em>

<em>&lt;startLocationName&gt;</em> , <em>Make sure to replace any space in the location name with a “+”</em> so for instance,

<strong><u>https://www.cs.usfca.edu/~dhalperin/distance.c</u></strong><strong>g<u>i?rideNumber=1502587145&amp;start=Los+An</u>g<u>eles </u></strong><strong><u>(https://www.cs.usfca.edu/~dhalperin/distance.c</u></strong><strong>g<u>i?rideNumber=1502587145&amp;start=Los+An</u>g<u>eles)</u></strong>

This will return at the end of the reply with a line like

<strong><em>Note: From Los Angeles to San Francisco will be 209 miles and take 378 minutes</em></strong>

There you get the distance, time it takes (Note that because of a special deal with the California Highway Patrol, Uberjava drivers are not assessed tolls when driving from their start location to the beginning of a fare).  This information is also in fixed format.

If you enter a bad location the reply will be simply

<strong>ERROR: Invalid start location</strong>

Note: You cannot specify the start location IF it is the same as the fare from location. You’ll get an error return: <strong>ERROR: Start location cannot be specified if same as from location</strong>

<ol start="6">

 <li>All drivers must accept all fares that they are able to get to (depending on their current location) within <u>300 </u>minutes or less. If a fare is not accepted, then you must make the call to UberJava</li>

</ol>

<strong><u>https://www.cs.usfca.edu/~dhalperin/re</u></strong><strong>j<u>ect.c</u>g<u>i?rideNumber=&lt;rideNumber&gt;</u></strong>

<strong><u>(https://www.cs.usfca.edu/~dhalperin/re</u></strong><strong>j<u>ect.c</u>g<u>i?rideNumber=&lt;rideNumber&gt;) </u></strong>to let the “dispatcher” know

The reply will look something like this:

<h1>UBERJAVA REJECT ACKNOWLEDGEMENT</h1>

RideNumber: 1502587145

Reject acknowledged

<ol start="7">

 <li>When you complete the ride, let UberJava know (so that you can be paid); AND so you can learn what your rating is. Do this by going to the site:</li>

</ol>

https://www.cs.usfca.edu/~dhalperin/rating.cgi?rideNumber=&lt;rideNumber&gt; where the rideNumber is what was provided in the nextFare request.

There in graphical format you get your rating for the ride from 1 to 5 stars. For example,

<strong><img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/12/438.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/12/438.png?w=980&amp;ssl=1" data-recalc-dims="1">

  </noscript></strong>

<strong>Note:  All riders are famous USF graduates, so please treat them with respect when they ride in your car!  Plus, that way you’ll get a good rating!</strong>

<em>Note: As famous USF graduates, they can magically take multiple rides at the same time and they can randomly appear in locations instantaneously.</em>

<u>Locations:</u> The only locations for starting OR that rides on UberJava are as follows:

Death Valley

Fresno

Los Angeles

Redding

Sacramento

San Bernadino

San Diego

San Francisco

San Jose Yosemite

<strong>All drivers <u>must</u> start in San Francisco.</strong>

<u>Types of Drivers: </u>Drivers may or may not be UberJavaX Premium Drivers.  However, only James Naismith and Prateek are UberJavaX Premium drivers, everyone else is a regular Driver.  As Premium Drivers, James and Prateek drive more expensive cars that use more gas and they have to pay for extra amenities that they give their riders – like water &amp; snacks. They get paid a higher fare than Regular UberJava drivers. The cost of their amenities is listed on the distance.cgi page, as follows:

<strong>Amenities (Water, snacks, etc.): $27.57</strong>

<u>Cars</u>: Your car can be any make and year and get between 15 and 50 miles per gallon. Every car has operating cost (maintenance plus insurance) per year equal to 20% of the initial price of the car (So a car that costs $62,000 will have an operating cost of $169.86 per 24-hour period) The Premium drivers have the following cars:

Prateek drives a 2019 Tesla Roadster that cost $219,800.

James drives a 2018 Porsche 911 Turbo S Cabriole that cost $200,400

Prateek gets 102 miles per gallon (in equivalent electrical cost); James gets 11.5 miles per gallon.

Your car can be any make and year and gets between 15 and 50 miles per gallon and costs at least $40,000 (we’re a high-end operation here at UberJava! Note your car – even if electric – cannot get more than 50 miles per gallon otherwise you cannot drive for UberJava!

<u>Costs</u>:

Every UberJava Driver has the following costs

Cost of vehicle ownership – assume that each car was got on a 3-year loan at 7% per year for the entire purchase cost. Look on <strong><u>https://www.creditkarma.com/calculators/loan</u></strong>

<strong><u>(https://www.creditkarma.com/calculators/loan) </u></strong>off-line to see what the monthly cost of the loan divide that by (30 * 24) and use that as the value of the cost for an hour of use. Use this to compute the ownership cost for the time of use in UberJava.

Operating costs for your vehicle for the time of use in UberJava

Tolls – if any

Cost per mile for gasoline

Amenities (for UberJavaX Premium Drivers)

<strong>Operation:</strong>

<ol>

 <li>You should write a main driver class called UberJavaMain in which you instantiate the three drivers (you, Prateek and James Naismith); and then have them accept and handle fares</li>

 <li>All Drivers (with their Cars) start in San Francisco AND they must keep driving for a “Session” of at least 24 hours (of recorded driving time) <u>AND</u> until their last fare ends in San Francisco. Note this may entail driving for significantly more than 24 hours.</li>

 <li>When your last Driver ends, the main method should print for each driver the following information:</li>

</ol>

Driver name and whether they are UberJavaX Premium Number of fares they had

Total fares, total miles driven, and total hours/minutes word Total amount the driver earned.

Total cost of operation (with a breakdown by type of cost)

Average Rider Rating

Effective Hourly Earnings after all costs are deducted.

<ol start="4">

 <li>Also, at the end, print the record for each Rider as follows:</li>

</ol>

Total number of fares they had in total and per Driver

Total amount they paid UberJava

Total minutes that they spent on UberJava rides

<strong>Details:</strong>

<ol>

 <li>You can practice any of the calls to UberJava in an ordinary browser by just typing in the request in the address bar. Try it now! <strong><u>https://www.cs.usfca.edu/~dhalperin/nextFare.c</u></strong><strong>g<u>i?driver=Abner+Doubleda</u>y </strong></li>

</ol>

<strong><u>(https://www.cs.usfca.edu/~dhalperin/nextFare.c</u></strong><strong>g<u>i?driver=Abner+Doubleday) </u></strong>(Note Abner Doubleday is widely considered the inventer of baseball)

<ol start="2">

 <li>All your drivers and interaction with the UberJava web pages should be in a package called uberjava.</li>

 <li>Drivers may or may not be UberJavaX Premium (only James Naismith and Prateek are the latter). This should be set when you instantiate a Driver.</li>

 <li>The Driver class should support the following methods int startSession() throws IllegalStateException – this will start a new UberJava session. Statistics should be kept for a session in an UberStatistics class object.  This call returns a sessionNumber particular to the driver. This will throw an IllegalStateException if there is already a started session that has not yet ended.</li>

</ol>

int endSession() throws IllegalStateException – this will end the current session; returns the ended session’s sessionNumber. This throws IllegalStateException if there is no current session.

UberStatistics getSessionStatistics(int sessionNumber) returns the statistics for the specified session or null if session does not exist

UberStatistics getSessionStatistics() returns the statistics for the current session (if it exists) or last session that ended else null

Location getCurrentLocation() returns the current location of the Driver

Int getSessionMinutes() throws IllegalStateException returns the total minutes since the start of the currentSession; throws IllegalStateException if there is no current session.

<ol start="5">

 <li>The Car class should extend from Vehicle. Both Car and Vehicle should be in a package called vehicle.</li>

 <li>Vehicle class:</li>

</ol>

The vehicle class maintains position of a vehicle

Should be declared abstract (you can instantiate a Car or other subclasses, but not Vehicle) Should have a currentLocation that indicates where the vehicle currently is.

The Constructor of Vehicle should be passed a start location.

boolean driveTo(Location newLocation) method should take a Location object as a parameter. (This is how a Vehicle moves). The method returns true if the Vehicle (Car) is moved false otherwise.

<ol start="7">

 <li>The Car class (which extends from Vehicle) should also include the following:</li>

</ol>

Include two Constructors

<ol>

 <li>Car(String name, int year, String make) – sets Location to San Francisco</li>

 <li>Car(String name, int year, String make, Location location) – sets Location to specified Location name (for instance, “Prateek’s Car”) instance variable getName() call parked boolean indicating whether or not the car is parked.</li>

</ol>

boolean isParked() to indicate if car is parked void park() to park the car the vehicle driveTo call should be overridden to first set parked to false before calling the super method. Keep track of all the cars that are created

static Car[] getCars – static method to get an array of all the cars

Keep track of operating cost of the car by including the following:

<ol>

 <li>purchaseCost – the amount spent to initially buy the Car. Set to a null value in the Constructor and add a setter and getter for this. The getter should throw a ValueUndefinedException (see below) if called before the value has been set.</li>

 <li>milesPerGallon – how many miles the Car can travel on a gallon of gas. Again, set to a null value in the Constructor, and add a setter and getter for this. The getter should throw a ValueUndefinedException (see below) if called before the value has been set.</li>

</ol>

<ol start="8">

 <li>After driving somewhere, you must park the Car before driving it again. (driveTo should return false IF the car is not parked when the method is called otherwise it works just like the vehicle driveTo method).</li>

 <li>A package called location <u>is provided for </u>y<u>ou</u> (because it includes “latitude” and “longitude” that can be used to hook this into a graphical user interface). It has one class called Location, that has a private constructor and statically creates an array of all ten locations that are available. Do not alter this class. Location include a getName() method that returns the Location name (e.g., “San Francisco”) and overrides toString. It also Includes the following static methods:</li>

</ol>

Location getByName(String name) – returns the Location with that name or null

Location[] getLocations() – returns an array of all available locations

<ol start="10">

 <li>Create a package called exception. Include at least one class called ValueNotSetException that extends RuntimeException. Make sure to include at least one Constructor that is passed a message parameter. 11. <u>Make all instance variables private; provide </u>g<u>etters and setters where appropriate </u> Make sure to override toString for almost every class that you create.</li>

 <li>Remember you have to drive from where ever you are to where your next Rider is and THAT takes time (included in your 24 hour++ session) and has gas and operating costs.</li>

 <li>Values returned in Web calls to UberJava: rideNumber is 10 characters long and consists of numbers and capital letters “[A-Z0-9]” Fares are in dollars and cents</li>

</ol>

Distance is in integer miles

Toll is integer dollars

Minutes are an integer

For the rating there are up to five stars – either “golden-star.jpg” or “blank-star.png” – count the goldenstar occurrences for the rating.

<strong>Submittal</strong>

<strong><em>After you have  pushed to github, please submit here on Canvas a statement that you have made your commit (This is how we’ll know it’s done!)  INCLUDE YOUR github user name in that statement.</em></strong>

<strong><em>Academic Honesty </em></strong>

<strong><em>Please do all your work individually unless otherwise specified. Do not look at anybody else’s code or solutions. You may discuss high level concepts and seek help from the TA or professor. Any outside sources used for help must be noted.</em></strong>

<strong>Grading:</strong>

Create exception class ValueUndefinedException (or ValueNotSetException) and throw it from getInitialCost and getMilesPerGallon  – 10 points

Implement a method that gets pages from the Web – 10 points

Implement a “parser” for each of the three calls – nextFare, distance, rating – 5 points each * 3 = 15 points

Implement Car &amp; Vehicle classes 10 points each * 2 = 20 points

Implement Driver class – 15 points

Instantiate 3 different drivers (James Naismith, Prateek, and themselves) – 5 points

Run a session (&gt;= 24 hours ending in San Francisco) for all 3 Drivers; maintain statistics for rides; demonstrated with a printout or clear within code – 15 points

Implemented sequence of events for a ride (Steps 4-7 under the explanation of how UberJava works: get nextFare; get  distance info; (optionally reject if too far); driveTo from wherever you are to the start of the ride (if necessary);  driveTo to the “to” location of the Ride; get rating  – 10 points

<strong>Total    100 points</strong>

<strong>Bonus Points Available</strong>

Maintain encapsulation by making instance variables private and implementing getters and setters throughout classes – 5 points

Created additional main methods in Driver and other classes in order to test code – 5 points