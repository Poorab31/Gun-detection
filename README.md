# Gun-detection
This is a code for detecting guns/firearms.
Gun Shape Detection (Python)
This project is a small basic try to detect objects that look like a gun shape by only using simple image processing ideas.
Problem Definition
Many places do not have advanced security tools or trained systems. The problem was to create something simple that can check a camera feed and warn if any shape looks like a gun or a long object.
Requirement Analysis
The program should be able to:
•	open webcam
•	capture video frames
•	convert image to grayscale
•	blur and detect edges
•	find contours of objects
•	check contour area, aspect ratio and solidity
•	show a message CLEAR or ALERT based on detection
•	draw boxes around possible shapes
Top Down Design / Modularization
The full idea is divided into smaller parts so it is more easy:
1.	Capture frame from camera
2.	Resize the frame
3.	Convert to grayscale
4.	Blur the image
5.	Apply Canny edge detection
6.	Find contours
7.	Check contour size and proportions
8.	Mark detected shapes
9.	Show output window




Algorithm Development (Short Explanation)
1.	Start program
2.	Open camera
3.	Read a frame
4.	Preprocess (gray + blur + edges)
5.	Find contours
6.	For each contour, check:
o	Is area big enough?
o	Is aspect ratio inside range?
o	Is solidity above limit?
7.	If yes, mark as possible gun-shape
8.	Update status text
9.	Repeat steps for next frame
10.	Stop when user presses 'q'
Implementation
This project uses:
•	OpenCV (cv2) for camera and image functions
•	imutils for resizing and contour handling
•	Only basic Python loops and conditions
•	Simple drawing functions like rectangle and text
Testing and Refinement
The project was tested with:
•	regular objects
•	long objects like bottle, stick, remote
•	small items
Some false detection happens, which is normal because this is only shape-based and not a trained model. Values like area, aspect ratio or solidity can be adjusted.
Expected Outcome
The program will:
•	show a live video window
•	highlight shapes that match the gun-like rules
•	display CLEAR when no shape found
•	display ALERT if something matches the detection rules
This is a simple, easy-to-understand project for students learning computer vision basics.

