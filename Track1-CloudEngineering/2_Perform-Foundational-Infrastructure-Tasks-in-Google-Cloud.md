## Perform Foundational Infrastructure Tasks in Google Cloud

*lab Link* (GSP3150): https://google.qwiklabs.com/focuses/10379?parent=catalog

```
There is no CLI instruction for this lab, you have to just use the (GCP UI) for completing this lab.
```

**Task 1: Create a bucket**
```yaml
1. Navigation menu > STORAGE > Storage > Create Bucket
2. Name your bucket > [ Enter your Project ID ] > Continue
3. Choose where to store your data > Region: us-east1 4. Continue
5. Use default values for the remaining
6. Click Create
```

**Task 2: Create a Pub/Sub topic**

```yaml
1. Navigation menu > BIG DATA > Pub/Sub
2. Create Topic > Name: Jooli > Create Topic 
```
> Make sure you remember the topic name, which will be used in Task 3.

**Task 3: Create the Cloud Function**
```yaml
1. In the console, click the Navigation menu > Compute > Cloud Functions
2. Click Create function
```
|    Field    |     Values                          |
|  ---------  |    --------                         |
| Name        | thumbnail                           |
| Region      | us-east1                            | 
| Trigger     | Cloud Storage                       |
| Event type  | Finalize/Create                     |
| Bucket      | BROWSE > Select the qwiklabs bucket |
 
 ```yaml
 3. Keep all default >Click Next
 4. Select Runtime: Node.js 10
    Entry point: thumbnail 
5. Copy the given in index.js and package.json to the dialog. [Code can be found at (Qwiklab_Page)]
```
 [Qwiklab Page](https://google.qwiklabs.com/focuses/10379?parent=catalog#:~:text=const%20topicName%20%3D%20%22MyTopic%22%3B-,index.js%3A,-/*%20globals%20exports%2C%20require)
 > Make sure you replace the text **REPLACE_WITH_YOUR_TOPIC** with the topic you created in task 2, in line 16 of index.js

 ```yaml
 6. Download the below image 
 ```
 ![](https://storage.googleapis.com/cloud-training/gsp315/map.jpg)

```yaml
7. Navigation menu > STORAGE > Storage > Select your bucket > Upload files
8. Refresh bucket
```

**Task 4: Remove the previous cloud engineer**

```yaml
1. Navigation menu > IAM & Admin
2. Search for the "USERNAME 2" > Edit > Delete Role
```