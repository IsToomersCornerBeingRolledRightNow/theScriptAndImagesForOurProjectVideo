# Competition Video

*description of image*

narration

## Script

*0) Map of Auburn*

This is Math Dept. Team Alpha, checking in from the Loveliest Village on
the Plains: Auburn, AL.

*1) Toomer's Corner being rolled*

Here at Auburn, we love our traditions. And one of our most unique traditions,
is the rolling of Toomer's Corner.

*2) Toomer's Drugs exterior*

According to AuburnTigers.com,
the tradition of rolling Toomer's Corner is said to have begun when Toomer's
Drugs had the only telegraph in the city.

*3) Toomer's Drugs interior*

After Auburn University would win a football
game on the road, employees of our local drug store would throw the ticker
tape from the telegraph onto the power lines. At some point down the line,
Auburn fans joined in by throwing toilet paper, and the rest is history.

*4) Toomer's Corner feed website*

Teams at the Auburn, AL Hackathon competition were prompted with several
suggestions, one of which was to take advantage of the live feed of
Toomer's Corner provided by the City of Auburn. What started as a joke
amongst our team of mathematicians quickly turned serious: using a little
bit of calculus, we can programmatically identify when Auburn's famous
corner is littered with celebratory TP.

*5) Level curves and gradient vectors*

A quick Cal 3 refresher: given a function of two variables, the gradient
vector field aways points in the direction of greatest change. As a result,
a gradient vector will always be perpendicular to the corresponding
level curve of the function.

*6) Edge-detected Toomer's Corner, no paper*

The function we wish to consider is simple: using the well-known
Canny edge detection algorithm, we may isolate the edges found in a photo
of Toomer's corner.

*7) Edge-detected Toomer's Corner, no paper, with gradient vectors*

In this image, the corner has not been rolled yet, so the edges and normal
gradient vectors are not oriented in a common direction.

*8) Edge-detected Toomer's Corner, with paper*

However, once Auburn fans get to rolling the corner...

*9) Edge-detected Toomer's Corner, with paper, with gradient vectors*

... due to gravity, the vertical strips of toilet paper introduce
numerous vertial edges,
and therefore horizontal gradient vectors. By summing up the number of
almost-horizontal gradient vectors, our application can say with a high
degree of confidence that Toomer's Corner is being rolled. Our application
does the obvious thing: it sends out a tweet to @IsToomersRolled,
and updates our website IsToomersCornerBeingRolledRightNow.com.

*10) Product page screenshot*

Despite the silliness of our concept,
our application was met with a high level of excitement from the Auburn
community, including the judges of our regional competition and local
press. Following our selection to move on to the global competition,
we put the app into production using Amazon Web Service's EC2 cloud servers,
where it watches the Toomers Corner webcam 24/7 for that next
rolling. We look forward to serving the Auburn community this fall as
football begins, but we're also excited to celebrate non-football victories
which result in the Auburn Family rolling Toomer's Corner as well.

*11) Toomer's Corner feed website*

Of course, as this tradition is certainly unique to the Auburn community,
we struggled to figure out how to generalize our application for global
use. While there certainly are some other specific applications, we came
to ask ourselves: "Is there another mathematical tool we can use to
recognize *arbitrary* unusual activity from a video feed?"

*12) Line of least squares regression*

Another quick math lesson. Given a collection of datapoints in a
two-dimensional space, the line of least squares regression may be used
to identify where further typical data points are expected to be
positioned.

*13) Principle Component Analysis*

This technique may be generalized to three dimensions, and higher,
known as principle component analysis, or PCA.
And that's a good thing, because a 400-by-300 pixel photograph is essentially
a 120,000-dimensional vector. By using footage of a typical day at
Toomer's corner, we
may use this technique to identify a hyperplane of least squares regression,
capturing what you could call "average" states of the web cam feed.

<!-- *14) "Average" image of Toomer's Corner*

This is what our algorithm considers to be one typical
image of Toomer's corner, but keep in mind that it also considers typical
photos in all kinds of weather and times of day. -->

*15) Photoshopped image of Toomer's Corner with dinosaurs*

Using this hyperplane,
we're able to identify any... not-so-typical scenes, by simply computing the
Euclidean distance of a photo from the hyperplane of typical photos.

*16) Photoshopped image of Toomer's Corner with police cars and barricades*

PCA is used in facial recognition techniques, but we see it being used
in reverse here: by registering when a photo of an intersection does *not*
look familar to the algorithm,
drivers could be alerted to find an alternate route to avoid
the unusual activity being observed. While this application is
still a prototype, our team is excited as this approach can recognize
arbitrary strange activity for any video feed, rather than the specific
criteria we search for in our production Toomer's Corner analysis.

*17) Picture of team or website*

Thanks for considering our project for the Smart City Hackathon! We're
honored to have had this opporunity to use mathematics and technology
to improve our local and global communities. Be sure to check out our
project READMEs on GitHub to learn more about each component of our
applications. And to our Auburn Family: Waar Eagle, Hey!






