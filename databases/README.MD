* Last Name: Leite
* First Name: Eduardo

# For this assignment I worked with Mamudu and Michelle P
# I also looked up onliine resources, youtube videos, and other Repos
https://www.youtube.com/watch?v=HXV3zeQKqGY


* SQL Challenge 1

SELECT Teacher, COUNT(Attendance) AS TotalCuts
FROM (SELECT s.First AS First, s.Last AS Last, s.StudentID AS StudentID, s.ScanTime AS ScanTime, s.Status AS Status, 
p.Date AS Date, p.CourseSection AS CourseSection, p.Attendance AS Attendance, p.Teacher AS Teacher, p.Period AS Period
FROM scan AS s
INNER JOIN periodAtt AS p
ON s.studentID = p.studentID
AND substr(ScanTime,1,instr(s.scanTime, ' ')-1) = p.Date
WHERE p.Attendance = 'A'
ORDER BY s.Last, s.First ASC) AS allCuts
GROUP BY Teacher
ORDER BY TotalCuts DESC
* Homework

SELECT First, Last, studentID, Grade, Scantime, (Period=1) AS pd1, Date, CourseSection
FROM
(
SELECT s.First, s.Last, s.studentID, s.Grade, s.ScanTime, s.Status, Date, CourseSection, Attendance, Teacher, Period 
FROM scan AS s
INNER JOIN periodAtt AS p
ON s.studentID=p.studentID AND SUBSTR(s.scanTime, 1, 9)=p.date
WHERE Attendance="A"
ORDER BY s.Last ASC) 
AS allCuts



https://colab.research.google.com/drive/1-pivEpm8NUUIQAIP5_qKwfzf17TWzXVR?userstoinvite=mamuduwally%40gmail.com#scrollTo=mKUZzfy95rZP





