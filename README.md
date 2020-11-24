# machine-learning-challenge

The Kepler mission monitored and cataloged data to support classic exoplanet identification
techniques of transit time, radial velocity, microlensing, and direct imaging.

 Radial velocity measures the shift of a star as from the gravitational pull of its orbiting planets. 
The measurement of radial velocity is correlated to the mass and the orbital period of a planet.Increases in mass and orbital speed result in increases in radial velocity [2].

Microlensing is an indirect method of planet detection [2]. It measures the bending of light as energy from astar passes a planet [2]. Microlensing offers the ability to detect the smallest and most distant planets.

The descriptions of radial velocity,microlensing, and direct imaging are intentionally brief as this work focuses primarily on transit time and cumulative data. 

Transit time was briefly discussed in the previous section and was an area of concentration
for this study. Planetary transits can yield information which can lead to an estimate of the object of interest’s size, speed of orbit, period of orbit, mass, and density of its star [2].Amazingly, a transit can also provide clues to an object of interest’s atmospheric composition as different elements absorb and reflect light differently [2].

transit time diagram - As a planet crosses between a star and the field of view of the observation tool, the light curve is altered. The transiting planet absorbs, reflects, or redirects a portion of the energy detected by the observer. The speed of transit and magnitude of the light curve change provide several insights into the object

Kepler’s transit data has become the leading source of data and
method for identifying exoplanets. Traditional direct imaging and radial velocity techniques
are biased towards the detection of large exoplanets. In contrast, Kepler’s transit time dataallows for the detection of smaller Earth-sized exoplanets—opening a whole new window of
planets to be discovered [4].

Another exoplanet dataset used for classifying candidate objects of interest is the Cumulative Kepler Object of Interest (KOI) table 13. The KOI table contains aggregate level datadescribing unique object of interest identifiers, exoplanet archive attributes, project disposition columns, summarized transit properties, threshold-crossing events, stellar parameters, and pixel-based KOI vetting statistics14; and considering the subject matter and vast distances of which the data was collected, the data quality of this table is good given the subject matter. 

Fortunately, the Cumulative KOI table has each observation labeled with a disposition of
“FALSE POSITIVE”, “CONFIRMED”, OR “CANDIDATE” in the “koi_disposition”. This enables the creation of a training data set with observations with a dispositionof “FALSE POSITIVE” OR “CONFIRMED”. “FALSE POSITIVE” is used to describe allobjects of interest tracked by Kepler which were determined not to be exoplanets.“CONFIRMED” describes objects of interest which have been confirmed to be exoplanets.“CANDIDATES” have not yet been formally classified25.The “CANDIDATE” observationscreate the test dataset used to make the final classification of exoplanet or not. For the train dataset, the disposition is encoded to a binary numeric column as required by the SVM classifier in Python (0 = “FALSE POSITIVE”, 1 = “CONFIRMED”)26
. This variable is then split intoits own dataframe and dropped from the primary dataset. The disposition dataframe is the response variable for the SVM classifier. 
 