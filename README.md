#Global Expansion of Rugby Union

##Summary
This visualization tells the story of how rugby has been around for a long time
(since the early 1800's) and for most of its existence has been popular in mainly
a few countries, mostly within the Commonwealth.  However, with the advent of the
Rugby World Cup and the professional era, the game is enjoying quick gains in 
global popularity.  This is shown in three charts:
  1. Increasing global TV audience for the World Cups
  2. Increasing participation for the World Cups
  3. Closer games in the World Cups as Tier 2 nations become as compentent as
     Tier 1 teams.

##Design
I wanted to be able to tell a full story not only of how rugby is increasing in 
popularity very recently but also to put that into context of how rugby's 
popularity was stagnant for many decades.  This would take a bit more than a 
few words in a caption, but I also didn't want to write a full article as that
was a bit out of scope of the project.  I was inspired by the excellent viz at
 http://drones.pitchinteractive.com/ and decided that might be the best way to go.
 
I broke up the visualization into three graphs to show three aspects of the growing
popularity: spectatorship, official participation by nations, and comptitiveness.
The first two are self-explanatory, the third is somewhat important for rugby
as Tier 1 teams (the traditional powerhouses) historically have routed the Tier 2
teams in competition, and there are arguments to keep the WC small because of this.

As there was a lot of information for the user, I wanted to try to simplify the 
component parts as much as possible and keep it all on one page.

**Timeline:**
	*Initial*: Though the viz focuses on how rugby has expanded in the WC era, I also
	wanted to convey how the expansion has accelerated significantly over the previous
	150 years by juxtaposing these timeframes in one timeline.  So the timeline will
	show the full history of rugby with the WC era comprising only the last 30 years.
	Once the timeline runs through, the timeline will focus on the WC events only to
	allow the user to review each event individually with updates to the following charts.
	*Feedback*: Users reported wanting more control to view the full timeline.  A 'pause' or
	'next' button was suggested, but thought these might be too cumbersome and preferred 
	a hands-off experience.  To address concerns I decided to allow the user to toggle
	back to the full timeline view with a click of a button.  Additional feedback indicated
	confusion between what event was shown in the timeline and what was on the map (e.g. 
	a pre-WC event was selected but the map was still showing WC data).  To help 
	clarify, I added a "World Cup Era" indicator on the timeline, which actually helps
	my initial decision to show how the World Cup era is a small portion of the full
	history of rugby.

**Audience chart**: 
	*Initial*: I decided to use a single-axis bubble chart with bubble size
	indicating viewership as this was a simple way to show how generally how viewership
	has gotten much greater.  Initially I planned to align the time axis to the goal 
	differential time axis (perhaps sharing it) so the user didn't have to process 
	two separate elements showing the same thing (passage of time), but eventually 
	decided to merge this with the timeline as I could re-use the timeline space to 
	convey this additional information (so, instead of timeline being 8 rect. buttons 
	left to right it would be the 8 bubbles with the additional size information).
	Colors are used for interactivity purposes, not to distinguish data.  "Red" was
	selected for the "active" year as most users would associate red with an "active"
	element.
	*Feedback*: Initially I thought to put no legend or labels to keep a streamlined
	view as the general message was still clear ('viewership is increasing').  However,
	the users thought this distracting, so I put floating labels on each point.
	
**Map**:
	*Initial*: I wanted to use a map to show the expansion of teams competing the WC
	for two reasons:
		1. A map is more visceral for users, if I can use that term.  Actually seeing
			participation spread across the globe will have more impact and remain in 
			the users mind longer rather than providing quantitative data only.
		2. The world map is a well understood representation for any viewer, so the 
			information can be processed more quickly and the viewer can make their own
			connections.  Saying that 16 teams competed in the first WC is one thing, 
			but when a viewer can see that a quarter of those were from the British 
			Isles alone that adds another dimension to the story.
		Regarding colors and breakdown of the categories, I wanted to focus on total
		participation only.  Results and performance are secondary to the story so 
		the presentation doesn't focus on this, but there is some information there 
		as it would be interesting to the viewer.  As such, I decided to make 
		"competing" different shades of the same color (blue) and "did not compete"
		countries gray (most users already identifying gray as generally indicating 
		'not active', 'no data', etc....).  The different shades of blue also make 
		the map viewable by colorblind persons.
	*Feedback*: In the legend I originally did not include an indicator for "did not
	compete".  There was some confusion as to which countries were competing and which
	were not, so I updated the legend to indicate "Competing, [RESULT]" for all 
	competing countries and "Did Not Compete" for the non-competing countries.
	Additionally, after adding the full timeline view, when a viewer selected a 
	non-WC event the map was still showing the best all-time WC performance which 
	was confusing.  I changed the map to show no countries competing and indicating
	that it was before the WC era.
	
**Points Difference Chart**:
	*Initial*: The main goal of this chart was to show points differential of games 
	decreasing over time.  I chose a scatterplot to show the points difference value
	decreasing (y-axis) as time goes on (x-axis).  This is a common chart type, so 
	it will be easily understood by viewers. 
	I wanted to show both individual games and average differences for the World Cup.  
	The individual games would show some of the outliers for how much blowouts were 
	a factor in some WCs (and it's generally interesting to see specific games/results).  
	The average shows the meat of the chart which is that the points differences are 
	going down on average: the World Cup is getting more competitive.  
	As I wanted to show a trend I added a line to connect the avg. points to make 
	it easier for the viewer to see.  I used two different colors to distinguish 
	between the two types of data, selectingthe same two colors as the rest of the 
	charts for continuity.
	*Feedback*: There was a technical issue with the scale not updating after the 
	introduction of the "full timeline" view, so that was corrected.

Two main points of feedback I received initially covered the following concerns:

  1. **Timeline speed and behaviour**:  In the initial draft, the timeline started 
	   automatically and the viewer usually wasn't preparted for it.  Additionally
		 the events went by too fast so the reader could not see this.
		 
		 To address this, I added a "start" button to the timeline and slowed it down
		 in general.  Additionally, I made the World Cup events stay up longer to 
		 account for the additional information that was shown in these.  Finally
		 I gave some functionality to allow the user to go back to see earlier events.
		 
	2. **No directions on use**:  Some users did not realize that there were
		interactive elements to the viz.  To address this, I added some explicit 
		wording on how to use the chart as well as some "mouseover" events to 
		highlight interactive elements.
		 

##Feedback
Viewer #1:  Points noted as viewer watched and commented on visualization:
							1. Modify timeline notes to include dates
							2. Add explanation/conclusion of charts
							3. Change map colors for readability (esp. light and medium blue)

Viewer #2:	"Right off the bat, I felt it was moving too fast.  I had to start the
						slideshow over as I didnt know it was going to begin moving through 
						different texts.  Maybe a flashing notification that 'slideshow begins 
						now' would help, or a button to allow viewer to 'begin slideshow'?  
						Even after I knew what to expect, I thought it moved very quickly, 
						especially when you introduced graphics to where my eye wanted to drift 
						down to the graphics, but then I knew I would miss out on the text.  
						At this point I had to restart it again.  Is it possible the viewer 
						could have control over the slideshow and have 'next' buttons?  or at 
						least control the speed or both.

						As for the graphs, they are a good representation of the data I believe.  

						In the beginning where you are chronologically moving through the years, 
						with each year it would be nice if you could add a picture or some 
						graphic to accompany it?  Capitalization of 'Rugby Union' - should it 
						always be capitalized or not? whatever the case, make sure you're 
						consistent throughout.  I found myself asking what is 'Rugby Union' 
						versus regular Rugby?  Are they the same thing?  I saw the little part
						about the schism but still was wanting a little more clarification 
						after the fact".

Viewer #3:	"I will exactly agree with Viewer #2's point about the speed, you 
						should explain that people can click on the time bar points to
						manually control. Even then, you should slow the auto movement down. 

						As a sales person I would recommend starting with an easier to read 
						entrance(perhaps it was just the quick start that made me miss the 
						point) with more info that tells me why The Story of Rugby is 
						important or maybe why the way you are presenting it is unique and 
						worth watching.  The data is great, but a person watching should 
						know why this data is great and interesting. More specifically, what
						does this tell me about the future of Rugby (I am always thinking of
						predictive when it comes to analytics)? Thore's suggestion on 
						graphics is good too. In general, I just needed a better way to 
						connect with the presentation.

						The last note is that I didnt know that there was additional 
						information below the time bar area at the end that was showing 
						additional data. Not sure if that was my screen resolution, but I 
						nearly didnt even know there was a line chart there on the bottom as 
						well."

Viewer #4: "I guess there's not much left for me to provide....  I would 
						definitely agree with Viewers 2 and 3.  It's a bit fast and I feel 
						like need to pause or have some sort of control.  There needs to be 
						some preparatory intro page (or at least more so than the current),
						which could be helped with some visuals."

##Resources 

		**Wikipedia**: General rugby information
			www.wikipedia.com
			
		**ESPN Statsguru**: World Cup fixture data (points differentials)
			http://stats.espnscrum.com/statsguru/rugby/stats/index.html

		**Pitch Interactive - Out of Sight, Out of Mind**: Visualization structure inspiration
			http://drones.pitchinteractive.com/
			
		**New York Times - Various Charts**: Visualization style inspiration
			http://www.nytimes.com

		**D3 API Reference**: Reference for D3 modules
			https://github.com/d3/d3/blob/master/API.md
			
		**Stackoverflow**: Issue resolution (D3, general js, HTML, CSS)
			http://stackoverflow.com/
			
		**Mike Bostock’s Blocks**: Reference for samples of specific D3 features
			https://bl.ocks.org/mbostock
