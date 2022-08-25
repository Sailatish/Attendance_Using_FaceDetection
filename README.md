# Attendance_Using_FaceDetection

## ABSTRACT:

Face Recognition is a computer application that is capable of `detecting, tracking, identifying or verifying` human faces from an image or video captured using a digital camera.
## Packages Used

- Face-Recognition
- cv2
- numpy
## Face Recognition — Step by Step
- Step 1: Finding all the Faces
- Step 2: Posing and Projecting Faces
- Step 3: Encoding Faces
- Step 4: Finding the person’s name from the encoding
## Recording Attendance to CSV File
```
with open('Attendance.csv','r+') as f:
        myDataList = f.readlines()
        nameList = []
        for line in myDataList:
            entry = line.split(',')
            nameList.append(entry[0])
        if name not in nameList:
            now = datetime.now()
            dtString = now.strftime('%H:%M')
            today = date.today()
            d1 = today.strftime("%d/%m/%Y")
            f.writelines(f'\n{name},{dtString},{d1}')
```
## Screenshort
<picture>
  <img src="Screenshot (29).png">
</picture>
