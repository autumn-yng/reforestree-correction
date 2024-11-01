# ReforeTree - Correction

Full report: https://docs.google.com/document/d/1jVvjSXZ2SAY1Hvxa1l6deUh6aBIIneTP-i4yoZTA9i0/edit?usp=sharing



Hi! We are Autumn and Sulagna from Mount Holyoke College. Here's our independent project on noticing and fixing mistakes on an already existing paper. We created this repository to store our work for correction of ReforesTree Dataset (https://github.com/gyrrei/ReforesTree/tree/main). 


ReforesTree is a valuable new dataset for the community of Machine Learning and data scientists who want to apply their skills to help the environment, especially through forestry applications. There are shortcomings in the original pipeline and dataset of ReforesTree, however. One of the core problems, discovered by Barenne et al, was that the areas captured by the drone images were bigger than the areas that the ground truth field measurements were taken on. Because ReforesTree authors were benchmarking the AGB estimations of satellite maps based on their drone images, the conclusion in the original ReforesTree paper that the satellite-based maps overestimated forest AGB couldn’t be proven right. To know whether those maps overestimated AGB or not, we would have to crop the drone images so that they capture exactly the same field measured area and recalculate the AGB estimation for comparison. This was what Barenne et al didn’t do, and we set out to do this.

![Screenshot 2024-11-01 at 5 48 01 AM](https://github.com/user-attachments/assets/52780c49-9efc-4c0c-8c68-b4c406b095ce)

In the original paper, the whole area of the drone images has been assumed to correctly fit into the area covered by the field measurements. As we can see in the pictures, that’s far from the truth. There may also be errors in the GPS locations and in the number of trees from the field measurements, as described in Barenne et al. Our aim was to find out how we can make clear, fix, and overcome these mistakes, so that this ReforesTree dataset can still help the machine learning community learn and get accurate results. Here's a step by step image description, how we edited the drone imagery.

![Screenshot 2024-11-01 at 5 49 45 AM](https://github.com/user-attachments/assets/58881689-3310-4fa3-a2c4-9e36c517354e)

Then we overlapped the correct images to get the satellite estimation based on AGBench(https://github.com/gyrrei/AGBench/tree/master/data)code. The overestimation factors changed but it still supported the hypothesis that satellite imageries overestimated the carbon stock. Besides, we noticed some area inconsistencies that we fixed in our calculation.

![Screenshot 2024-11-01 at 5 54 01 AM](https://github.com/user-attachments/assets/cdfe1338-1ccc-4cb9-9b1e-0bc45cfa37c3)
