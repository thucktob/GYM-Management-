CREATE TABLE Subscription (
    SubscriptionID INT PRIMARY KEY,
    Type VARCHAR(50),
    StartDate DATE,
    EndDate DATE,
    Amount DECIMAL(10,2)
);

CREATE TABLE Member (
    MemberID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT,
    Gender VARCHAR(10),
    Phone VARCHAR(15),
    JoinDate DATE,
    SubscriptionID INT,
    FOREIGN KEY (SubscriptionID) REFERENCES Subscription(SubscriptionID)
);

CREATE TABLE Attendance (
    AttendanceID INT PRIMARY KEY,
    MemberID INT,
    Date DATE,
    FOREIGN KEY (MemberID) REFERENCES Member(MemberID)
);
![image](https://github.com/user-attachments/assets/f931fa21-078d-4f7f-8c94-7a62ddc6cefb)
