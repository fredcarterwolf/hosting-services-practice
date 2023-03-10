<br />

<div align="center">
  <h1>Backend</h1>
  <p><h3 align="center">Ready-to-run APIs π</h3></p>
  <a href="https://expressjs.com/">Express</a>
  <span>&nbsp;&nbsp;β’&nbsp;&nbsp;</span>
  <a href="https://www.prisma.io/">Prisma</a>
  <span>&nbsp;&nbsp;β’&nbsp;&nbsp;</span>
  <a href="https://planetscale.com/">Planetscale</a>
  <span>&nbsp;&nbsp;β’&nbsp;&nbsp;</span>
  <a href="https://dash.cloudflare.com/">Cloudflare</a>
</div>
<hr>
<br />

```
get("/detail/:email")
    description: get all the detail record of user by providing its email behind the endpoint

post("/detail")
    description: create the detail record
    body: email, temperature, blood_pressure, pulse_rate, hemoglobin, hematocrit, white_cell, platelet

put("/detail/:id")
    description: update the detail record
    body: temperature, blood_pressure, pulse_rate, hemoglobin, hematocrit, white_cell, platelet

get("/news")
    description: get all the news record from the news table

post("/news")
    description: create a news record in the database
    body: title, text

put("/news/:id")
    description: update the news record by providing the news id behind the endpoint
    body: title, text

post("/task")
    description: create a task record in the task table
    body: name, description

get("/task")
    description: get all the task from the task table

get("/task/:id")
    description: get specific task by providing the task id behind the endpoint

put("/task/:id")
    description: update a task record
    body: name, description

get("/user/:email")
    description: get the all the detail of the user

post("/user/signup")
    description: signup the user
    body: email, password

post("/user/login")
    description: login user
    body: email, password
```

<hr>

```
src
β   index.ts - Main server file
β
ββββapi
β   β
β   ββββcontrollers
β   β       Detail.controller.ts
β   β       News.controller.ts
β   β       Task.controller.ts
β   β       User.controller.ts
β   β
β   ββββmiddlewares
β   β       cors.ts
β   β       jwt.ts
β   β       rate_limit.ts
β   β       index.ts
β   β
β   ββββroutes (CRUD operation with database)
β       - Set "Content-Type": "application/json"
β       - Set "Authorization": "Bearer ${token}" | token retreive from user login
β
β           Detail.ts
β               get("/detail/:email")
β                   description: get all the detail record of user by providing its email behind the endpoint
β
β               post("/detail")
β                   description: create the detail record
β                   body: email, temperature, blood_pressure, pulse_rate, hemoglobin, hematocrit, white_cell, platelet
β
β               put("/detail/:id")
β                   description: update the detail record
β                   body: temperature, blood_pressure, pulse_rate, hemoglobin, hematocrit, white_cell, platelet
β
β           News.ts
β               get("/news")
β                   description: get all the news record from the news table
β
β               post("/news")
β                   description: create a news record in the database
β                   body: title, text
β
β               put("/news/:id")
β                   description: update the news record by providing the news id behind the endpoint
β                   body: title, text
β
β           Task.ts
β               post("/task")
β                   description: create a task record in the task table
β                   body: name, description
β
β               get("/task")
β                   description: get all the task from the task table
β
β               get("/task/:id")
β                   description: get specific task by providing the task id behind the endpoint
β
β               put("/task/:id")
β                   description: update a task record
β                   body: name, description
β
β           User.ts
β               get("/user/:email")
β                   description: get the all the detail of the user
β
β               post("/user/signup")
β                   description: signup the user
β                   body: email, password
β
β               post("/user/login")
β                   description: login user
β                   body: email, password
β
β           index.ts
β
ββββlib
β       jwt.ts
β       prisma.ts
β
ββββtest
```
