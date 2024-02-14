<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
<h1>Object-Detection-for-ML-Engineering</h1>
<p>This Repo contains a Box Detection Application capable of identifying box containers in conveyor belt pictures.</p>

<h2>Project Detations</h2>

<ol>
  <li><strong>Data Science</strong>
    <ul>
      <li><b>Yolo8_Model_Creation.ipynb</b> downloads the dataset from Roboflow, followed by training Yolov8 on train set using transfer learning, validation and test result display. Finally, the model is saved as <i>best.pt</i></li>
    </ul>
  </li>

  <li><strong>Machine Learning </strong>
    <ul>
      <li>I created a FastAPI web application to serve the saved model to customers. Home page is a basic I/O based UI that lets a user upload a conveyor belt image, and when a button is clicked, the application uses the previously saved Yolo8 model to detect box containers and return the image with labels in a new page. Alternatively, I also created an API functionality that can programmatically accept a conveyor belt image as input to return as output the image with labels saved in local system. </li>
      <li>Finally, I deployed this FastAPI based Yolov8 application as a Docker Image, which runs this application in a containerized manner, and uploaded it to Docker Hub. This means all end users can avoid the hassle of installing multiple packages needed to run the application on their system. All they need to is to simply install Docker Desktop, pull the image from the hub, run it as a Docker container and finally access the webpage as localhost:8000</li>
    </ul>
  </li>
</ol>
  
  

<h2>End User Instructions</h2>
In order to use this object detection web application, please follow below instructions
<ol>
  <li><strong>Install Docker</strong>
    <ul>
      <li>Make sure Docker is installed on your system. You can download and install Docker Desktop from the official Docker website.</li>
    </ul>
  </li>

  <li><strong>Pull the Docker Image</strong>
    <ul>
      <li>Open a terminal or command prompt in your system and run:
        <pre><code>docker pull agpsuai23/box_detection_image</code></pre>
      </li>
      <li>This command will download the Docker image named <code>agpsuai23/box_detection_image</code> to your local machine.</li>
    </ul>
  </li>

  <li><strong>Run the Docker Container</strong>
    <ul>
      <li>Once the image is pulled, execute the following command:
        <pre><code>docker run -p 8000:8000 agpsuai23/box_detection_image</code></pre>
      </li>
      <li>This command starts the container and maps port 8000 of the host to port 8000 of the container, allowing access to the application.</li>
    </ul>
  </li>

  <li><strong>Access the Application</strong>
    <ul>
      <li>Open a web browser and go to: <a href="http://localhost:8000/" target="_blank">http://localhost:8000/</a></li>
      <li>You can now interact with the Box Detection Application through the browser interface.</li>
    </ul>
  </li>
</ol>

</body>
</html>
