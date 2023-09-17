# 1.why we have the need for fedarated learning?

**1.the privacy**  
  
  In many applications, dataset may conclude some sensitive information. Such as self information and self-medical information.

**2.the policy**  
  
  Transformation for cross-border may be constricted by policies.

**3.the effiency**  
  
  To deal with big datasets, it may be not a good option to collect them up in one server. Since calculate locally can save up resources and time.

# 2.classes of fedarated learning

## classified by types of data

**1.Horizontal Federated Learning(HFL)**  
  
  Same features but different id.
  For examples, hospitals own lot of similar medical information, belonging to different persons.

**2.Vertical Federated Learning(VFL)**  
  
  Same id but different features.
  For examples, one hospital owns the body information for a person, while school owns his academic information.

**3.Federated Transfer Learning(FTL)**  
  
  By pre-training on a large dataset, we get a fundamental model, which will be sent to several local clients to be trained again.
  To a certain extent, FTL aims to combine federated learning and transfer learning.

## classified by types of experience

**1.cross-device**  
  
Datas locate in different and substantial devices. The number of devices can reach 10 orders of magnitude.

**2.cross-silo**  
  
Datas mainly derive from several data center of enterprise server. Nodes always run more stably.

# 3.the basic procedure of federated learning  

**step1. initialize a global model by the center server**

**step2. send the model to clients joined**

**step3. clients use local datas to train the model, and calculate to update the model.**

**step4. clients sent the new model to server.**

**step5. server collect all the new models and update the global model again.**

**step6.repete those steps until the model converges of satisfied other stopping conditions**

# 4.Other questions  

## 1.how do clients update locally?  

Clients use local datas and received models to train the origin model, then calculate the figures of updating.

## 2.Is there a center server?

In traditional federated learning there does exist a center server.  
But to increase resilience, reduce the risk of a single point of failure or further enhance privacy, non-center methods also appear nowadays.

## 3.What's the functions of server?

The main function of server is to initialize the model, distribute it to clients, collect the updated models, and eventually collect them to renew the global model.

## 4.The content of communication between clients and server.

**4.1 clients to server**  
Local trainings generate changes of weight, which clients upload to the server. It can be an actual change or an increment of the weight.   
For examples, the weight of client A is updated from w=5 to w=6, client will upload this *+1* to server.  

  Besides the weight of model, clients may also update other parameters like learning rate, batches of training. 

**4.2 clinets to clients**
During some non-center fedarated learning, clients may need to communicate with other clients directly to exchange new weights or run collaborative training.


