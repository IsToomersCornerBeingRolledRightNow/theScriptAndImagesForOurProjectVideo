# Competition Video

*description of image*

narration

## Script

*Map of Auburn*

This is Math Dept. Team Alpha, checking in from the Loveliest Village on
the Plains: Auburn, AL.

*Toomer's Corner being rolled*

Here at Auburn, we love our traditions. And one of our most unique traditions,
is the rolling of Toomer's Corner.

*Toomer's Drugs*

According to AuburnTigers.com,
the tradition of rolling Toomer's Corner is said to have begun when Toomer's
Drugs had the only telegraph in the city. After Auburn University
would win a football
game on the road, employees of our local drug store would throw the ticker
tape from the telegraph onto the power lines. At some point down the line,
Auburn fans joined in by throwing toilet paper, and the rest is history.

*Toomer's Corner feed website*

Teams at the Auburn, AL Hackathon competition were prompted with several
suggestions, one of which was to take advantage of the live feed of
Toomer's Corner provided by the City of Auburn. What started as a joke
amongst our team of mathematicians quickly turned serious: using a little
bit of calculus, we could programmatically identify when Auburn's famous
corner is littered with celebratory TP.

*Level curves and gradient vectors*

A quick Cal 3 refresher: given a function of two variables, the gradient
vector field aways points in the direction of greatest change. As a result,
a gradient vector will be perpendicular to the level curves of the function.

*Edge-detected Toomer's Corner, no paper*

The function we wish to consider is simple: using the well-known
Canny edge detection algorithm, we may isolate the edges found in a photo
of Toomer's corner.

*Edge-detected Toomer's Corner, no paper, with gradient vectors*

In this image, the corner hasn't been rolled, so the edges and normal
gradient vectors are not in a common direction.

*Edge-detected Toomer's Corner, with paper*

However, once Auburn fans get to rolling the corner...

*Edge-detected Toomer's Corner, with paper, with gradient vectors*

... the vertical strips of toilet paper introduce numerous vertial edges,
and therefore horizontal gradient vectors. By summing up the number of
almost-horizontal gradient vectors, our application can say with a high
degree of confidence that Toomer's Corner is being rolled. Our application
does the obvious thing: it sends out a tweet to @IsToomersRolled,
and updates our website IsToomersCornerBeingRolledRightNow.com.

*Product page screenshot*

The application was met with a high level of excitement from the Auburn
community, including the judges of our regional competition and local
press. Following our selection to move on to the global competition,
we put the app into production using Amazon Web Service's EC2 cloud servers,
where it watches the Toomers Corner webcam 24/7 for that next
rolling. We look forward to serving the Auburn community this fall as
football begins, but we're also excited to celebrate non-football victories
which result in the Auburn Family rolling Toomer's Corner as well.

*Toomer's Corner feed website*

Of course, as this tradition is certainly unique to the Auburn community,
we struggled to figure out how to generalize our application for global
use. While there certainly are some other specific applications, we came
to ask ourselves: "Is there another mathematical tool we can use to
recognize *arbitrary* unusual activity from a video feed?"

*Line of least squares regression*

Another quick math lesson. Given a collection of datapoints in a
two-dimensional space, the line of least squares regression may be used
to identify where further typical data points are expected to be
positioned.

*Plane of least cubes regression*
<!-- change slide title to "Principle Component Analysis" ~Daniel  -->

This technique may be generalized to three dimensions, and higher.
And that's a good thing, because a 400-by-300 pixel photograph is essentially
a 120,000-dimensional vector. By using footage of a typical day at
Toomer's corner, we
may use this technique to identify a hyperplane of least squares regression,
capturing what you could call "average" states of the web cam feed.

*"Average" image of Toomer's Corner*

This is an average image of Toomer's corner generated from our algorithm,
at least for a certain time of day. It's computationally difficult to
generate these; however, we only need to do this every so often.
<!-- This whole slide is redundant, you already state in the above slide that PCA generates a hyperplane of "typical" or "average" images. You might mention that our new image analysis algorithm measures the distance of an image from a (pregenerated) hyperplane of typical images. It might be notable that PCA is already used in computer facial-recognition algorithms ~Daniel -->


*Photoshopped image of Toomer's Corner with dinosaurs*

Using this hyperplane storing average days at Toomer's Corner, we're able
to identify any... not-so-average scenes.
<!-- the hyperplane doesn't store average days, it characterizes images as being "typical" or not ~Daniel -->

*Photoshopped image of Toomer's Corner with police cars and barricades*

We believe this technique has applications in analyzing roads and traffic,
as drivers could be alerted to find an alternate route when an intersection
is likely obstracted with unusual activity. While this application is
still a prototype, our team is excited as this approach can recognize
arbitrary strange activity for any video feed.
<!-- good point, the algorithm detects arbitrary "non-typical" images -->

*Picture of team or website*

Thanks for considering our project for the Smart City Hackathon! We're
honored to have had this opporunity to use mathematics and technology
to improve our local and global communities.







