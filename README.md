# teach-byte
##ABSTRACT
###In spite of technological advancements, the farm productivity of Indian agriculture is still on the
lower side. The underlying reason for poor farm productivity in India is due to the inefficient usage
of agricultural inputs, resulting in low or poor-quality agricultural yields. Water happens to be one
of such imperative agricultural input that has a huge impact on agricultural productivity. Precision
agriculture systems can take care of irrigation requirements by optimally and efficiently using irrigation
water for producing crops having superior quality and quantity. This work proposes a smart irrigation
system that can efficiently manage the water requirements of the crop for its optimal growth. The
irrigation schedules are developed using a feed forward neural network model that can predict the
variation in the soil moisture considering the environmental factors such as temperature, humidity,
atmospheric pressure, and the rain. The results indicate the effectiveness of the developed system in
predicting the soil moisture with mean square error as low as 0.13 and the R value as high as 0.98.
##KEYWORDS
### linear regression , iot, soil moisture, agreeculture, machine learning
<details open>
<summary>introduction</summary>
<br>
  Water happensto be the most vital element forsustaining life on the Earth both for humans and animals.
Studies show that humans can live without food for three weeks but when it comes to water, humans
cannot sustain more than three days at a stretch. The same theory applies to the crops that are grown
in the field; they do require water. The depleting levels of the water table, irregular monsoons, climate
change (Aryal, J.P., et al. 2019), water contaminations are posing as serious hurdles for developing a
sustainable agriculture system (Tripathy S, 2019). In agriculture, even with the irrigated lands with
adequate irrigation sources (S. Latha, 2019), the utilization of water for irrigation is not strategic.
The problem that needs immediate attention is, how water, being a limited and vital resource can be
smartly used for irrigation purpose to produce good quality yields capable of fetching good returns
to the farmers. Precision Agriculture (PA) system would definitely be a suitable solution for most
of the issues arising in the agricultural domain including irrigation. In order to provide efficient
This article, originally published under IGI Global’s copyright on October 1, 2020 will proceed with publication as an Open Access article
starting on February 2, 2021 in the gold Open Access journal, International Journal of Agricultural and Environmental Information Systems
(converted to gold Open Access January 1, 2021), and will be distributed under the terms of the Creative Commons Attribution License
(http://creativecommons.org/licenses/by/4.0/) which permits unrestricted use, distribution, and production in any medium, provided the
author of the original work and original publication source are properly credited.
International Journal of Agricultural and Environmental Information Systems
Volume 11 • Issue 4 • October-December 2020
2
water utilization, the PA system needs to be tailor-made for the farmers especially from developing
countries. The implementation success of the PA system largely relies on the implementation costs,
implementation complexity, deployment time, and ease of maintenance. To ensure cost-effectiveness,
the field sensor-based approach is recommended. PA system using field-based sensor approach for
data collection, IoT for providing remote monitoring of parameters and using intelligence in the form
of ML-based predictive model to provide closed-loop control of field parameters would definitely
transform the traditional agriculture into a sustainable one. The reach of the Internet in every nook and
cranny of the world has created a huge demand for applications involving things rather than peoples.
Currently, there are around 8.3 Billion IoT connected devices worldwide and it is predicted that by
2025, this number will be more than double what it is today (21.5 Billion). IoT has already started
benefitting the users worldwide in all the sectors be it healthcare, industry, education or agriculture.
Though the implemented PA systems have seen the progress and success in the agricultural sector in
countrieslike Australia (Jochinke et al. 2007), Belgium, Canada, and the United Statesto name a few,
still the major chunk of farmers are yet to harnessthe rewarding benefits of it. Going by the literature,
there are many implementations of IoT in the agriculture domain. Agriculture can be thought of as
a complex system, which consists of sub-systems like soil preparation, seed implanting, irrigation,
fertilization, weeding, harvesting, sorting, storing and transportation.
IoT was the main driving force for the development of the agricultural systems providing some
of the outstanding solutions to the problems being faced by the farmers in the agricultural and the
related domains. Also,security remainsthe main concern when IoT isinvolved in providing enterprise
and business solutions to the customers. Limited researches focused on the security part of IoT
implementations in agriculture as in (L. Vidyashree and B. M. Suresha, 2019), where an encryption
method was proposed for securing agriculture data.
The work carried out in this research attempts to design a highly secured agricultural field
monitoring and irrigation scheduling system by using IoT and Artificial Neural Network (ANN)
based predictive model. The IoT part is responsible for data collection, storage, and visualization.
The feed-forward neural network (FFNN) model uses the locally generated datasets from the IoT
cloud-server as model inputs. The performance measurement of the FFNN predictive model was
done based on MSE and R. The model was able to accurately predict the moisture values in the field
with low values of MSE and high values of R, apart from this, the other the salient features of the
proposed system are that the developed system uses of low-cost and easily available sensors, the main
center of attraction of the developed system is the ESP32 DevKit V1 which hosts an ESP32 SoC
MCU (capable of providing high security, ultra-low power requirement with built-in Wi-Fi and dual
Bluetooth modules), open-source hardware/software platforms for prototyping and programming,
open-source ThingSpeak™ IoT platform and API for data storage and visualization which also provides
MATLAB® analytics on the cloud. Finally, an Android App is developed by using the Blynk platform
for providing user-friendly irrigation control and automation in the field along with user notification
in the form of email and SMS.
The rest of the paper is organized as follows. Section 1 provides an in-depth literature review
of similar implementations. Section 2 deals with the Prototype Design Ecosystem, highlighting the
hardware and software requirements, technical specifications along with the platform as a service.
Section 3 uses a block diagram approach that highlights the proposed system with various block
descriptions. Section 4 describesthe in-field experimentalsetup for irrigation control and location of
the setup. In Section 5, the results are tabulated for the proposed ANN model that provides irrigation
control and discussion is carried out justifying the use of sensors, microcontrollers, and the ANN
model. In section 6, a detailed comparison is presented with similar implementations in the area of
interest and highlighting the salient features of the developed system and also the cost analysis is
done and compared with other similar systems. Section 7 concludes the paper by revealing important
findings and indicating the importance of the proposed system in the present context along with some
of the improvements that can be taken up in the future.
</details>
<details open>
<summary>METHODOLOGY</summary>
<br>The random forest regression model is a popular machine learning technique used to predict soil moisture levels based on various environmental factors.In this report, we will use the random forest algorithm to predict soil moisture. The data used for this analysis was collected from a soil moisture sensor in a field over a period of previous 8 months . The dataset contains soil moisture measurements and weather variables such as temperature,pressure,pm3,pm2,pm1,time,luminicity,atmospheric moisture and humidity. We used Python programming language and Scikit-learn library to build the random forest model.
 The methodology for using this model can be broken down into the following steps:

Data Collection: The first step in using the random forest regression model is to collect data on the environmental factors that affect soil moisture levels. This data may include variables such as temperature,pressure,humidity,soil moisture,pm1,pm2,pm3,ttime,luminosity,atmospheric moisture.

Data Preprocessing: Once the data has been collected, it is necessary to preprocess it to ensure that it is in a suitable format for use with the random forest regression model. This may involve steps such as data cleaning, normalization, and feature scaling.

Splitting Data into Training and Testing Sets: After preprocessing, the data is split into two sets: a training set and a testing set.We then split data into training and testing sets, with 80% of the data used for training and 20% for testing. The training set is used to train the random forest regression model, while the testing set is used to evaluate its performance.

Training the Model: The next step is to train the random forest regression model using the training set. The model is built by constructing a large number of decision trees, each of which is trained on a random subset of the training data and a random subset of predictor variables.

Evaluating Model Performance: Once the model has been trained, its performance is evaluated using the testing set. This involves using the model to predict soil moisture levels based on the environmental factors( such as;temperature,humidity) in the testing set, and comparing these predictions to the actual soil moisture levels.model has been trained based on the training data and evaluated its performance on the testing data. Mean squared error (MSE) and R-sqaured (R2) metrics to evaluate the model's performance.

Tuning the Model: If the model's performance is not satisfactory, it may be necessary to tune its parameters. This can be done by adjusting the number of decision trees in the forest, the maximum depth of each tree, or the number of variables used in each split.

Final Model Deployment: Once the model has been trained and tuned to the desired level of performance, it can be deployed to predict soil moisture levels based on new environmental data.

In summary, the methodology for using the random forest regression model to predict soil moisture levels involves collecting and preprocessing data, splitting it into training and testing sets, training the model, evaluating its performance, tuning its parameters if necessary, and deploying the final model
![SCHMATIC REPRESENTATION OF RANDOM FOREST](![schematic representation of random forest](https://user-images.githubusercontent.com/116057588/227758314-5aeea6c4-176a-4b45-843e-1eeed27ba040.jpg)

![general methodology for soil moisture](![A-general-methodology-for-soil-moisture-estimation-through-remote-sensing-using-ML](https://user-images.githubusercontent.com/116057588/227758478-458d74df-4dbb-4923-a28b-57cf4622e183.png)
</deatail>
<details open>
<summary>DATA SHEET</summary>
<br>the data has been collected from previous 8 months in the file new data .csv
</deatail>
<details open>
<summary>RESULTS</summary>
<br>The use of the random forest regression model in predicting soil moisture levels using weather variables has shown promising results. In this study, we applied the random forest algorithm to a dataset containing soil moisture measurements and weather variables such as temperature, atomospheric moisture,pressure,luminosity,pm1,pm2,pm3,ttime,humidity.

The results of the analysis showed that the random forest model achieved high accuracy in predicting soil moisture, with a mean squared error (MSE) of 2.357and an R-squared (R2) score of 0.99 on the testing data. These results indicate that the model is able to accurately predict soil moisture levels using weather variables accuracy score is 0.99

Furthermore, the feature importance analysis revealed that temperature and humidity were the most important variables in predicting soil moisture, humidity. This information can be useful for farmers in making informed decisions about irrigation and crop management.

The use of machine learning algorithms such as the random forest regression model in predicting soil moisture levels can ultimately lead to improved agricultural practices and higher crop yields. By providing accurate predictions of soil moisture levels, farmers can optimize their irrigation practices and minimize water usage, which can lead to cost savings and environmental benefits.
</deatail>
<details open>
<summary>CONCLUSION</summary>
<br>In conclusion, the results of this study demonstrate the potential of machine learning algorithms in predicting soil moisture levels and provide valuable insights for farmers in managing their crops. Further research can explore the use of additional variables and techniques to improve the accuracy of the predictions and optimize crop management practices.

#project by team tech-byte 
1.Samruddhi Hiremath
2.Soubhagya Manohar Muddebihal
3.Srushti Basaragi
4.Vachanashree

