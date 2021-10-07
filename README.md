# Statistical Data Analysis Project

This project focuses on using some exploratory data analysis as well as null hypothesis testing to compare different datasets.

We have information on aproximately 500 fake users that have two different types of cell phone plans: a _surf_ plan and an _ultimate_ plan. We have information about where they're from, which plan they use, and the number of calls, text messages, and time spent on the internet in a single year. In this project, the plan is to analyze clients' behavior and determine which prepaid plan brings in more revenue.

## What to know about this project:

**The Aim** - The goal of this project is to prepare the data as if it were to be used in a model later on. Garbage in equals garbage out, so we will want to preprocess the data as best we can. Strategies include:
- Identify and fill in missing values
- Optimize data types
- Delete duplicate data
- Categorize the data

**The Data** - The data files below is where our input for the project comes from, and it can be found in this project folder. The files contain different non-identifying information on people associated with their plans, their calls, their messages, their internet usage, . The following characteristics are in the file:

The `calls` table - `megaline_calls.csv`  
The `internet` table - `megaline_internet.csv`  
The `messages` table - `megaline_messages.csv`  
The `plans` table - `megaline_plans.csv`  
The `users` table - `megaline_users.csv`  



The `users` table (data on users):  
`user_id`: unique user identifier  
`first_name`: user's name  
`last_name`: user's last name  
`age`: user's age (years)  
`reg_date`: subscription date (dd, mm, yy)  
`churn_date`: the date the user stopped using the service (if the value is missing, the calling plan was being used when this database was extracted)  
`city`: user's city of residence  
`plan`: calling plan name

The `calls` table (data on calls):  
`id`: unique call identifier  
`call_date`: call date  
`duration`: call duration (in minutes)  
`user_id`: the identifier of the user making the call  

The `messages` table (data on texts):  
`id`: unique text message identifier  
`message_date`: text message date  
`user_id`: the identifier of the user sending the text  

The `internet` table (data on web sessions):  
`id`: unique session identifier  
`mb_used`: the volume of data spent during the session (in megabytes)  
`session_date`: web session date  
`user_id`: user identifier  

The `plans` table (data on the plans):  
`plan_name`: calling plan name  
`usd_monthly_fee`: monthly charge in US dollars  
`minutes_included`: monthly minute allowance  
`messages_included`: monthly text allowance  
`mb_per_month_included`: data volume allowance (in megabytes)  
`usd_per_minute`: price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)  
`usd_per_message`: price per text after exceeding the package limits  
`usd_per_gb`: price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)  

**The Surf Plan**:  
- Monthly charge: $20
- 500 monthly minutes, 50 texts, and 15 GB of data
- After exceeding the package limits:
  - 1 minute: 3 cents
  - 1 text message: 3 cents
  - 1 GB of data: $10

**The Ultimate Plan**:  
  - Monthly charge: $70
  - 3000 monthly minutes, 1000 texts, and 30 GB of data
  - After exceeding the package limits:
    - 1 minute: 1 cents
    - 1 text message: 1 cents
    - 1 GB of data: $7

**Questions to Solve** - During this process, we will try to answer these questions:
- What are some initial observations on the consumers' behaviors?
- Hypothesize that the average revenue from users of Ultimate and Surf calling plans differs.
- Hypothesize that the average revenue from users in NY-NJ area is different from that of the users from other regions.
