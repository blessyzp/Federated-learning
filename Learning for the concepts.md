# why we have the need for fedarated learning

**1.the privacy**
In many applications, dataset may conclude some sensitive information. Such as self information and self-medical information.

**2.the policy**
Transformation for cross-border may be constricted by policies.

**3.the effiency**
To deal with big datasets, it may be not a good option to collect them up in one server. Since calculate locally can save up resources and time.

# classes of fedarated learning

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

**