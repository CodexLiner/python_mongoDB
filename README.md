
**Q. What is openCV ?**

[OpenCV](https://opencv.org/)  ‘Open Source Computer Vision Library’ is an open-source library that includes several hundreds of computer vision algorithms. Using OpenCV, you could pretty much do every Computer Vision task that could ever be imagined !

**According to Wikipedia**

Computer vision is an [interdisciplinary scientific field](https://en.wikipedia.org/wiki/Interdisciplinarity) that deals with how computers can be made to gain high-level understanding from [digital images](https://en.wikipedia.org/wiki/Digital_image) or [videos](https://en.wikipedia.org/wiki/Video). From the perspective of [engineering](https://en.wikipedia.org/wiki/Engineering), it seeks to automate tasks that the [human visual system](https://en.wikipedia.org/wiki/Human_visual_system) can do.

In Simple words Computer vision is a field of deep learning that allows the machine to identify, process images just like humans do. In terms of parsing images humans perform extremely well but when it comes to machines detecting objects involves multiple and complex steps, including feature extraction (edges detection, shapes, etc), feature classification, etc.

**More about open CV**

OpenCV contains implementations of more than 2500 algorithms! It is freely available for commercial as well as academic purposes. The library has interfaces for multiple languages, including Python, Java, and C++.

Applications:

**OpenCV’s** application areas include:

2D and 3D feature toolkits

Egomotion estimation

Facial recognition system

Gesture recognition

Human–computer interaction (HCI)

Mobile robotics

Motion understanding

And Many More

OpenCV gives access to more than 2,500 state-of-the-art and classic algorithms. By using this library, users can perform various tasks like removing red eyes, extracting 3D models of objects, following eye movements, etc.

**Q. What is Pandas ?**

Pandas is an open-source library that is built on top of NumPy library. It is a Python package that offers various data structures and operations for manipulating numerical data and time series. It is mainly popular for importing and analyzing data much easier. Pandas is fast and it has high-performance & productivity for users.
##### Adavantage of Pandas
- Fast and efficient for manipulating and analyzing data.
- Data from different file objects can be loaded.
- Easy handling of missing data (represented as NaN) in floating point as well as non-floating point data.
- Size mutability: columns can be inserted and deleted from Data Frame and higher dimensional objects.
- Data set merging and joining.
- Flexible reshaping and pivoting of data sets.
- Provides time-series functionality.
- Powerful group by functionality for performing split-apply-combine operations on data sets.

**Q. Write a Code to add Establish Connection with MongoDB ?**

```python
# PyMongo is a Python distribution containing tools for working with MongoDB
from pymongo import MongoClient

# creating database if doesnt exist
def getDatabase():
    cluster = MongoClient(
        "mongodb+srv://root:root@cluster0.o8ehzeq.mongodb.net/?retryWrites=true&w=majority")
    db = cluster["my_database"]
    return db

# inserting single value on collection
def insert_user(data, collection):
    collection.insert_one(data)
    print("Congrats User Succesfully inserted " , data)

# deleting single value on collection
def delete_user(query, collection):
    collection.delete_one(query)
    print("Congrats User Succesfully deleted " , query )

# updating single value n the collection
def update_user(query, collection, data_to_update):
    collection.update_one(query, data_to_update)
    print("Congrats User Succesfully updated " , query , "To" , data_to_update )


# main function 
def main():
    database = getDatabase()
    collection = database["user_collection"]
    # insert_user(data= {"_id": 100, "user_name": "Sushil"} , collection=collection)
    # delete_user(query = {"_id": 100} , collection=collection)
    # update_user(query={"_id": 100}, collection=collection , data_to_update= {"$set" : {"user_name" : "Gopal Meena"}} )

# calling main function
if __name__ == "__main__":
    main()

```

