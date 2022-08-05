---
stoplight-id: wr6ko5tozqgd3
---

# Overview

This API detects instances of real-world entities within an image provided as input as a Base64 encoded text. This includes objects like flower, tree, and table; events like wedding, graduation, and birthday party; and concepts like landscape, evening, and nature. For example, you can create an application that alerts you when a person approaches your video doorbell instead of an animal.

For the example if I use the following Base64 encoded data:

[](https://gist.github.com/lbrenman/86bfd4ac91b8ccdaf7c5cf45b2e317fc) 

for the car image shown below:

![](https://i.imgur.com/8XiS1DF.jpg)

I will get the following response:

```javascript
{
    "Labels": [
        {
            "Name": "Car",
            "Confidence": 98.41893005371094,
            "Instances": [
                {
                    "BoundingBox": {
                        "Width": 0.9095886945724487,
                        "Height": 0.4260041415691376,
                        "Left": 0.044332683086395264,
                        "Top": 0.37117668986320496
                    },
                    "Confidence": 98.41893005371094
                }
            ],
            "Parents": [
                {
                    "Name": "Vehicle"
                },
                {
                    "Name": "Transportation"
                }
            ]
        },
        {
            "Name": "Automobile",
            "Confidence": 98.41893005371094,
            "Instances": [],
            "Parents": [
                {
                    "Name": "Vehicle"
                },
                {
                    "Name": "Transportation"
                }
            ]
        },
        .
        .
        .
        {
            "Name": "Jaguar Car",
            "Confidence": 57.534969329833984,
            "Instances": [],
            "Parents": [
                {
                    "Name": "Car"
                },
                {
                    "Name": "Vehicle"
                },
                {
                    "Name": "Transportation"
                }
            ]
        }
    ],
    "LabelModelVersion": "2.0"
}
```
