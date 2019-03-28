# A Virtual Tour of Stonehenge 

![alt text](https://raw.githubusercontent.com/UBC-GEOB472-Spring2019/dminney-web/master/Geographic%20Visualization/Stonehenge-sample.png)

[Experience Stonehenge in VR!](https://a-frame-assignment.glitch.me/)

## Discussion of Process
My idea to create a 'virtual reality tour' stemmed from the idea of the Stanley Park VR Experience, where the user could walk around either using VR controls, their phone, or their computer, and explore somewhere they could physically not visit. I knew that the limitations with A-frame and WEBVR would prevent any complex VR experience from being possible, so I adapted this idea to present a virtual tour of Stonehenge in Salisbury, England. This 3D experience sets itself apart from a typical 2D experience, because the grand size and mystery of Stonehenge is very present through the 3D, as I experienced when visiting the historic site a few years ago. Pictures and maps of the site would not do it justice, which is why I thought bringing it into a 3D realm would be a good idea. The signs around the site are also similar to the ones at the actual location, providing short tidbits of information for the user to gain a greater understanding of the mystery that still surrounds Stonehenge today.

### Sources
The models for stonehenge and the signs used were found on Sketchfab.

[Stonehenge Model](https://sketchfab.com/3d-models/stonehenge-dji-mavic-jaymie-james-0947e454c8ad491593ce867f3d29169e)

[Sign Model](https://sketchfab.com/3d-models/sign-592ba375a7194290affed512a06c562a)


### Difficulties
There were however some problems, as the models used were highly detailed and although usable in A-Frame, they would create a laggy and un-pleasant expereince. To solve this, the model was downloaded in OBJ form and opened up in Meshlab. Then, the polygons were reduced using the following: 
**Filters → Remeshing, Simplification and Reconstruction → Simplification: Quadric Edge Collapse Decimation (with texture)** 

After reducing the amount of faces by a significant amount, the file was saved as OBJ. The next problem was converting OBJ to GLTF for use in A-frame. Although there were some websites that provide an online conversion tool, none of them were able to retain the textures. I was able to convert the file using [obj2gltf](https://github.com/AnalyticalGraphicsInc/obj2gltf) which is programmed using Node.js. After reducing the amount of polygons, the reduction in lag was noticeable, without loosing too much detail and texture of the model itself. 

### Room for Improvement
Due to my own personal limitaitons and the limitations of A-frame, this project could be improved greatly. The detail of the model if preserved would provide a greater sense of reality, as well as the ability to create a realistic and high quality photosphere or extension of the model. However, i was able to work around this by adding fog which gives the illusion that there is a landscape beyond the fog that just cannot be seen, similar to the placement of mirrors in a small space to give the illusion of an extension of space. 

