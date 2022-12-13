# Traffic-light-management-using-AI
Despite the fact that computer vision is today a highly developed field, capabilities for recognition and classification are not frequently used in day-to-day activities. Therefore, in this project we will make use of the current traffic infrastructure with some additional requirements, to create and demonstrate an advanced traffic light management
# Abstract
Increasing traffic congestion at signalized junctions is a matter of great concern for creating and maintaining sustainable cities. Traffic jams in addition to adding to drivers' delays and stress levels, traffic bottlenecks significantly increase fuel usage and pollution. The main reason behind this is the way of controlling traffic at such junctions. Semi-automated and conventional traffic management has reached it’s saturation point and can no longer handle the high density of traffic flow with complex patterns. In this paper, we discuss and draw comparisons of previous research and works done to solve this problem. Our focus would be on techniques using Machine Learning, such as Computer Vision and Deep Neural Networks.
# Introduction
Numerous road networks are experiencing issues due to the decline in road capacity and the accompanying Level of Service as a result of the rise in automobiles in metropolitan areas. The bottleneck for these high vehicular flow are the conventional traffic management system used in these cities. There are two ways to tackle traffic flow currently in implementation : semi-automatic traffic lights with fixed timings or traffic police stationed at junctions to control the flow manually. The problem with use of traffic lights is that they use a fixed time for each side of the cross road, irrespective of the density of vehicles on those roads.

![image](https://user-images.githubusercontent.com/75363378/207390161-76e0fa64-9982-49e7-8f3c-874404b94fe5.png)
![image](https://user-images.githubusercontent.com/75363378/207390225-02272ba4-38c9-48a2-b05b-3e329a4a6589.png)

Ideally, the road with higher density of vehicles should be given extra time to pass the junction, as that will lead to lower waiting time on average for all of the vehicles. Depending on manual control of traffic at junctions with manpower is inefficient, as a human cannot process all of the information at live with great accuracy for a longer time. Despite the fact that computer vision is today a highly developed field, capabilities for recognition and classification are not frequently used in day-to-day activities. Therefore, in this project we will be using Machine Vision to improve the current state of traffic. We would also come across some new methodology and techniques in analysis and decision making for traffic lights using live cameras installed at junctions.
# Problem Statement
To build a self adaptive traffic light control system based on YOLO. Disproportionate and diverse traffic in different lanes leads to inefficient utilization of same time slot for each of them characterized by slower speeds, longer trip times, and increased vehicular queuing.To create a system which enable the traffic management system to take time allocation decisions for a particular lane according to the traffic density on other different lanes with the help of cameras, image processing modules.
# Methodology
The solution can be explained in four simple steps:
1.	Get a real time image of each lane.
2.	Scan and determine traffic density.
3.	Input this data to the Time Allocation module.
4.	The output will be the time slots for each lane, accordingly.

 <img src="https://user-images.githubusercontent.com/75363378/207391460-a103d439-ec6b-460f-a7b7-acddeb8c42a2.png" height="500">  <img src="https://user-images.githubusercontent.com/75363378/207391504-bf55def6-0644-4673-99ba-233f63f3c63b.png" width="500" height="500">

# Results and Discussions
The result for the project could be divided in two divisions : 

1.	Evaluation of Vehicle Detection Model
		The vehicle detection module was tested with a variety of test images containing varying amounts of vehicles, and the accuracy of detection was found to be in the  		range of 75-80%. Some test results are shown above in Fig. 3. This is satisfactory, but not optimum. The primary reason for low  accuracy is the lack of a proper 		dataset. To improve upon this, real-life footage from traffic cameras can be used to train the model, so that accuracy of the system can be improved.
		We have used the images from the live feed camera installed at the traffic junctions or at normal traffic spots around the city or on the outskirts. These videos 		or live feeds were  used to feed the model based on YOLO and OpenCV, where we detected the vehicle and there movement as in downwards or upwards, i.e., towards the 		traffic signal or away from it. We were also successful in defining what type of vehicle is it.
		
    <img src="https://user-images.githubusercontent.com/75363378/207393722-8678178d-4ca3-41d3-a8ab-ffc61a123f9a.png" width="800" height="550">
    <img src="https://user-images.githubusercontent.com/75363378/207393802-b3c7df30-5a11-48f0-baf0-838395017fe3.png" width="800" height="550">

    We were also succesfull in implementing the derived traffic density from the detection module to the model for finding the optimum timings for each traffic lane to 		pass the vehicles. This was done on the principle of giving more priority or giving more time to the lane with higher traffic density and lesser to the ones with 		relatively uncrowded lane, while not creating bottlenecks or congestion in any one lane. For the same purpose,  we created a simple simulation using PyGame.
		
    <img src="https://user-images.githubusercontent.com/75363378/207395269-acc46692-6cd3-4391-b262-17749ada0868.png" width="800" height="550">

		
2.	Evaluation of the Proposed Adaptive System
		For the pupose of evaluation of the system, the traffic movement simulation for both the system was run for 5 minutes a total of 15 times, using which the total 			number of vehicles that were able to pass through this junction were calculated.
		
    <img src="https://user-images.githubusercontent.com/75363378/207395478-a0ceec2b-21e0-4954-aa3d-732d7bd51bd4.png" width="500">
		
# References
[1] <a href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9358334&isnumber=9358272">M. M. Gandhi, D. S. Solanki, R. S. Daptardar and N. S. Baloorkar, "Smart Control of Traffic Light Using Artificial Intelligence," 2020 5th IEEE International Conference on Recent Advances and Innovations in Engineering (ICRAIE), 2020, pp. 1-6, doi: 10.1109/ICRAIE51050.2020.9358334.</a>

[2] <a href="https://www.researchgate.net/publication/229029935_Intelligent_Traffic_Lights_Control_By_Fuzzy_Logic">Khiang, Kok & Khalid, Marzuki & Yusof, Rubiyah. (1997). Intelligent Traffic Lights Control By Fuzzy Logic. Malaysian Journal of Computer Science. 9. 29-35.</a>

[3] <a href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6137134&isnumber=6137119">M. H. Malhi, M. H. Aslam, F. Saeed, O. Javed and M. Fraz, "Vision Based Intelligent Traffic Management System," 2011 Frontiers of Information Technology, 2011, pp. 137-141, doi: 10.1109/FIT.2011.33.</a>

[4] <a href="https://www.researchgate.net/publication/328987822_Improving_Traffic_Light_Control_by_Means_of_Fuzzy_Logic">A. Vogel, I. Oremović, R. Šimić and E. Ivanjko, "Improving Traffic Light Control by Means of Fuzzy Logic," 2018 International Symposium ELMAR, 2018, pp. 51-56, doi: 10.23919/ELMAR.2018.8534692.</a>

[5] <a href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7868350&isnumber=7868337">T. Osman, S. S. Psyche, J. M. Shafi Ferdous and H. U. Zaman, "Intelligent traffic management system for cross section of roads using computer vision," 2017 IEEE 7th Annual Computing and Communication Workshop and Conference (CCWC), 2017, pp. 1-7, doi: 10.1109/CCWC.2017.7868350.</a>
