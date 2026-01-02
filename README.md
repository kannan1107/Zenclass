#  MongoDB Task  (Design database for Zen class programme)

Design database for Zen class programme
users
codekata
attendance
topics
tasks
company_drives
mentors

## Create the collection

- create the user collection => db.createCollection ("user")
- codekata collection    =>  db.createCollection ("codekata")
- attendance collection    =>  db.createCollection ("attendance")
- topics collection    =>  db.createCollection ("topics")
- tasks collection    =>  db.createCollection ("tasks")
- company_drives collection    =>  db.createCollection ("company_drives")
- mentors collection =>   db.createCollection ("mentors")


##  ("user")  user insert commend    db.users.insertMany([

-  {

    // User 1

    _id: ObjectId(),

    name: "kannan",

    email: "kannan@example.com",

    batch: "B42WD",

    role: "student",

    created_at: ISODate("2020-09-10")

  },

  {

- User 2

    _id: ObjectId(),

    name: "Priya ",

    email: "priya@example.com",

    batch: "B42WD",

    role: "student",

    created_at: ISODate("2020-09-12")

  },

  {

    // User 3

    _id: ObjectId(),

    name: "kaja",

    email: "kaj@example.com",

    batch: "B42WD",

    role: "student",

    created_at: ISODate("2020-09-15")

  },

  {

    // User 4

    _id: ObjectId(),

    name: "raj",

    email: "raj@example.com",

    batch: "B42WD",

    role: "student",

    created_at: ISODate("2020-09-17")

  },

  {

    // User 5

    _id: ObjectId(),

    name: "selva",

    email: "selva@example.com",

    batch: "B42WD",

    role: "student",

    created_at: ISODate("2020-09-20")

  }

]);

- codekata collection    =>  db.createCollection ("codekata")
- attendance collection    =>  db.createCollection ("attendance")
- topics collection    =>  db.createCollection ("topics")
- tasks collection    =>  db.createCollection ("tasks")
- company_drives collection    =>  db.createCollection ("company_drives")
- mentors collection =>   db.createCollection ("mentors") 
 
## show the All Collection  => show collections
## show the All Database  => show dbs
## current DataBase  =>  db
## show the users collection data => db.users.find().pretty();

## insert the codekata collection data
- db.codekata.insertMany([
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9efd"),
    problems_solved: 150,
    last_solved_date: ISODate("2023-08-01")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9efe"),
    problems_solved: 200,
    last_solved_date: ISODate("2023-08-02")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9eff"),
    problems_solved: 180,
    last_solved_date: ISODate("2023-08-03")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9f00"), 
    problems_solved: 220,
    last_solved_date: ISODate("2023-08-04")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9f02"), // FIXED → 24 chars
    problems_solved: 170,
    last_solved_date: ISODate("2023-08-05")
  }
]);


### insert the attendance collection data
- db.attendance.insertMany([
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9efd"),
    date: ISODate("2023-08-01"),
    status: "present"
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9efe"),
    date: ISODate("2023-08-01"),
    status: "absent"
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9eff"),
    date: ISODate("2023-08-01"),
    status: "present"
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9f00"),
    date: ISODate("2023-08-01"),
    status: "present"
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9f02"), 
    date: ISODate("2023-08-01"),
    status: "absent"
  }
]);


## show the users collection data => db.attendance.find().pretty();
## show the users collection data => db.codekata.find().pretty();
## insert the topics collection data
- db.topics.insertMany([
  {
    _id: ObjectId(),
    topic_name: "JavaScript Basics",
    description: "Introduction to JavaScript programming language.",
    created_at: ISODate("2023-07-01")
  },
  {
    _id: ObjectId(),
    topic_name: "Node.js Fundamentals",
    description: "Understanding the basics of Node.js.",
    created_at: ISODate("2023-07-05")
  },
  {
    _id: ObjectId(),
    topic_name: "MongoDB Basics",
    description: "Introduction to MongoDB NoSQL database.",
    created_at: ISODate("2023-07-10")
  },
  {
    _id: ObjectId(),
    topic_name: "Express.js Overview",
    description: "Getting started with Express.js framework.",
    created_at: ISODate("2023-07-15")
  },
  {
    _id: ObjectId(),
    topic_name: "RESTful APIs",
    description: "Designing and building RESTful APIs.",
    created_at: ISODate("2023-07-20")
  }
]);


## show the users collection data => db.topics.find().pretty();
## insert the tasks collection data 
- db.tasks.insertMany([
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9efd"),
    task_name: "Build a To-Do App",
    status: "completed",
    due_date: ISODate("2023-08-10")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9efe"),
    task_name: "Create a RESTful API",
    status: "in-progress",
    due_date: ISODate("2023-08-15")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9eff"),
    task_name: "Design a Database Schema",
    status: "pending",
    due_date: ISODate("2023-08-20")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9f00"),
    task_name: "Implement Authentication",
    status: "completed",
    due_date: ISODate("2023-08-12")
  },
  {
    _id: ObjectId(),
    user_id: ObjectId("6929bff4c4e80b31e74e9f02"), 
    task_name: "Deploy to Cloud",
    status: "in-progress",
    due_date: ISODate("2023-08-18")
  }
]); 


## show the users collection data => db.tasks.find().pretty();
## insert the company_drives collection data
- db.company_drives.insertMany([
  {
    _id: ObjectId(),
    company_name: "TechCorp",
    drive_date: ISODate("2023-09-01"),
    participants: [
      ObjectId("6929bff4c4e80b31e74e9efd"),
      ObjectId("6929bff4c4e80b31e74e9efe")
    ]
  },
  {
    _id: ObjectId(),
    company_name: "InnovateX",
    drive_date: ISODate("2023-09-10"),
    participants: [
      ObjectId("6929bff4c4e80b31e74e9eff"),
      ObjectId("6929bff4c4e80b31e74e9f00")
    ]
  },
  {
    _id: ObjectId(),
    company_name: "CodeWorks",
    drive_date: ISODate("2023-09-15"),
    participants: [
      ObjectId("6929bff4c4e80b31e74e9f02") 
    ]
  }
]);

## show the users collection data => db.company_drives.find().pretty();
## insert the mentors collection data
- db.mentors.insertMany([
  {
    _id: ObjectId(),
    name: "kannan",
    email: "kannan@example.com",
    expertise: ["JavaScript", "Node.js"],
    assigned_batches: ["B42WD"]
    },
    {
    _id: ObjectId(),
    name: "Priya",
    email: "priya@example.com",
    expertise: ["MongoDB", "Express.js"],
    assigned_batches: ["B42WD"]
    },
    {
    _id: ObjectId(),
    name: "kaja",
    email: "kaja@example.com",
    expertise: ["HTML", "CSS"],
    assigned_batches: ["B42WD"]
    },
    {
    _id: ObjectId(),
    name: "raj",
    email: "raj@example.com",
    expertise: ["React", "Redux"],
    assigned_batches: ["B42WD"]
    },
    {
    _id: ObjectId(),
    name: "selva",
    email: "selva@example.com",
    expertise: ["Python", "Django"],
    assigned_batches: ["B42WD"]
    }
    ]);
## show the users collection data => db.mentors.find().pretty();


## Find all the topics and tasks which are thought in the month of October
- db.topics.find({ created_at: { $gte: ISODate("2023-10-01"), $lt: ISODate("2023-11-01") } }).pretty();


- db.tasks.find({ due_date: { $gte: ISODate("2023-10-01"), $lt: ISODate("2023-11-01") } }).pretty();

## Find all the company drives which appeared between 15 oct-2020 and 31-oct-2020
- db.company_drives.find({ drive_date: { $gte: ISODate("2020-10-15"), $lte: ISODate("2020-10-31") } }).pretty();
## Find all the company drives and students who are appeared for the placement.
- db.company_drives.aggregate([
  {
    $lookup: {
      from: "users",
      localField: "participants",
      foreignField: "_id",
      as: "student_details"
    }
  }
]).pretty();
## Find the number of problems solved by the user in codekata
- db.codekata.aggregate([
  {
    $lookup: {
      from: "users",
      localField: "user_id",
      foreignField: "_id",
      as: "user_details"
    }
  },
  {
    $unwind: "$user_details"
  },
  {
    $project: {
      _id: 0,
      user_name: "$user_details.name",
      problems_solved: 1
    }
  }
]).pretty();
## Find all the mentors with who has the mentee's count more than 15
- db.mentors.aggregate([
  {
    $lookup: {
      from: "users",
      localField: "assigned_batches",
      foreignField: "batch",
      as: "mentees"
    }
  },
  {
    $addFields: {
      mentee_count: { $size: "$mentees" }
    }
  },
  {
    $match: {
      mentee_count: { $gt: 15 }
    }
  },
  {
    $project: {
      _id: 0,
      name: 1,
      email: 1,
      mentee_count: 1
    }
  }
]).pretty();
## Find the number of users who are absent and present in the month of October
- db.attendance.aggregate([
  {
    $match: {
      date: { $gte: ISODate("2023-10-01"), $lt: ISODate("2023-11-01") }
    }
  },
  {
    $group: {
      _id: "$status",
      count: { $sum: 1 }
    }
  }
]).pretty();
## Find the number of tasks assigned to and completed by each user
- db.tasks.aggregate([
  {
    $lookup: {
      from: "users",
      localField: "user_id",
      foreignField: "_id",
      as: "user_details"
    }
  },
  {
    $unwind: "$user_details"
  },
  {
    $group: {
      _id: "$user_details.name",
      total_tasks: { $sum: 1 },
      completed_tasks: {
        $sum: {
          $cond: [{ $eq: ["$status", "completed"] }, 1, 0]
        }
      }
    }
  },
  {
    $project: {
      _id: 0,
      user_name: "$_id",
      total_tasks: 1,
      completed_tasks: 1
    }
  }
]).pretty();
## Find all the mentors who has the mentee's count more than 10 and sort them in descending order
- db.mentors.aggregate([
  {
    $lookup: {
      from: "users",
      localField: "assigned_batches",
      foreignField: "batch",
      as: "mentees"
    }
  },
  {
    $addFields: {
      mentee_count: { $size: "$mentees" }
    }
  },
  {
    $match: {
      mentee_count: { $gt: 10 }
    }
  },
  {
    $sort: {
      mentee_count: -1
    }
  },
  {
    $project: {
      _id: 0,
      name: 1,
      email: 1,
      mentee_count: 1
    }
  }
]).pretty();
## Find the topics and tasks which are thought in the month of October and sort them by date.
- db.topics.find({ created_at: { $gte: ISODate("2023-10-01"), $lt: ISODate("2023-11-01") } }).sort({ created_at: 1 }).pretty();
- db.tasks.find({ due_date: { $gte: ISODate("2023-10-01"), $lt: ISODate("2023-11-01") } }).sort({ due_date: 1 }).pretty();

## Find all the company drives and students who are appeared for the placement.
- db.company_drives.aggregate([
  {
    $lookup: {
      from: "users",
      localField: "participants",
      foreignField: "_id",
      as: "student_details"
    }
  }
]).pretty();

## Find the number of users who are absent and task is not submitted  between 15 oct-2020 and 31-oct-2020
- db.attendance.aggregate([
  {
    $match: {
      date: { $gte: ISODate("2020-10-15"), $lte: ISODate("2020-10-31") },
      status: "absent"
    }
  },
  {
    $lookup: {
      from: "tasks",
      localField: "user_id",
      foreignField: "user_id",
      as: "user_tasks"
    }
  },
  {
    $unwind: "$user_tasks"
  },
  {
    $match: {
      "user_tasks.status": { $ne: "submitted" }
    }
  },
  {
    $group: {
      _id: null,
      absent_and_not_submitted_count: { $sum: 1 }
    }
  },
  {
    $project: {
      _id: 0,
      absent_and_not_submitted_count: 1
    }
  }
]).pretty();




