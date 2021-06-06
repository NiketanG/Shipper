## Shipper

Traffic Management and Navigation System for Coastal Regions.
Developed for **ASEAN-India Hackathon** 2021 - PS7 by Team 51 and received **Encouragement Award**. 

### Demo

[Shipper-Web](https://shipper-web.netlify.app) - Shipper Dashboard

[Shipper-ML](http://nikketan.pythonanywhere.com/) - Object Detection API for Ship Detection using Satellite Imagery


### What is Shipper ?

Shipper is a Traffic Management and Navigation System designed for Coastal Regions. This includes but not limited to docks, and regions surrounding sea shores.


### How it works

![How it works](Process.png)

The [Server](https://github.com/NiketanG/shipper-server) acts as an AIS Station for the demo. The [Dashboard](https://github.com/NiketanG/shipper-web) utilizes the AIS Sensor & Radar on the deck for positioning. As the Coastal AIS Station transmits data, the dashboard shows and updates positions of other ships nearby.

When other ships are in close proximity, the dashboard switches to Radar for better accuracy. 

As the ships move far from coast, the connection to AIS Station is lost, the Dashboard automatically switches to Satellite Imagery for Ship Identification using [Shipper-ML](https://github.com/NiketanG/shipper-ml). It takes the satellite imagery, then identifies and marks the ships in it, and returns the new image.

Based on locations of other ships, appropriate warnings are displayed along with Navigational Guides in case of collisions. 

A report system for unidentified ships is also implemented using the same AIS Server, and this data is transmitted to all ships in the vicinity. 

The implementation, requires no internet connectivity once connected to the AIS on Deck, as it can be converted into a standalone app running on standalone server.  


The [Pitch Presentation](Shipper_Team51_PS7.pdf) is included in the repo. 

---
### Local Development
##### IMPORTANT

> For Cloning, the usual `git clone` command wont work as the repo contains submodules. Use the command below.
```
git clone --recurse-submodules https://github.com/NiketanG/shipper
```

The Repo contains three modules - [`shipper-web`](https://github.com/NiketanG/shipper-web), [`shipper-server`](https://github.com/NiketanG/shipper-server) & [`shipper-ml`](https://github.com/NiketanG/shipper-ml)

- Shipper-web 
    
    Web Application to be used on the Client


- Shipper-server
    
    Mock Server used for Demo Purposes  


- Shipper-ml
    
    Object Detection ML API for Detecting Ships using Satellite Imagery


### Installation
##### Instructions for installation of each module are given in respective directories  ([`shipper-web`](https://github.com/NiketanG/shipper-web), [`shipper-server`](https://github.com/NiketanG/shipper-server) & [`shipper-ml`](https://github.com/NiketanG/shipper-ml)). 


##### Shipper-Server
- Install Dependencies
- Configure Environment Variables
- Create Database Migrations
- Start the Shipper-server.

##### Shipper-Server
- Install Dependencies
- Configure the Mapbox Tokens and API_URL environment variables for Shipper-web. 
- Start Shipper-Web.
- Open [http://localhost:3000](http://localhost:3000) in your browser to view the dashboard. 

##### Shipper-ML
- Install dependencies for Shipper-ML.
- Download the Pre-trained model.
- Start the server and open [http://localhost:5000](http://localhost:5000) in your browser.



### Tech Stack
#### Open source projects used:

##### Backend:
[Nodejs](https://nodejs.org/en/)
[Expressjs](http://expressjs.com/)
[Socket.io](http://socket.io/)
[Postgresql](https://www.postgresql.org/)

##### Frontend:

[Reactjs](https://reactjs.org/)
[Tailwindcss](https://tailwindcss.com/)
[Mapbox](https://www.mapbox.com/)


##### Object Detection API
[Flask](https://flask.palletsprojects.com/en/2.0.x/)
[OpenCV](https://docs.opencv.org/master/d6/d00/tutorial_py_root.html)
[Numpy](https://numpy.org/)
[Pillow](https://pillow.readthedocs.io/)



---

## Team

- Niketan Gulekar
- Joselyn Bernabe
- Kim Vathanak
- [Edwin Ong](https://www.linkedin.com/in/edwin-ong-b43227142/)
- [Sinatrio Bimo Wahyudi](https://github.com/sinatriiobimo)


## LICENSE
[Eclipse Public License (EPL)](https://www.eclipse.org/legal/epl-2.0/)

You are free to modify the code. Redistributions are not allowed without prior request from the original author. You are obligated to include the full **license** and the **copyrights**.