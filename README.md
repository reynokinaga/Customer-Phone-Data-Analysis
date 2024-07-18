# Project 1: Ex-Mobile Report

# Summary

 You are hired by Ex-Mobile to be their new business analyst. Ex-Mobile is a very small company and is looking to expand so they want you to run some analysis on their customer database and figure out marketing recommendations and some other important analytical questions.


# Deliverables

The way you will do this is by following the instructions below. Your deliverables will be a combination of answered questions and copied tables in Excel and a .sql file with the queries you wrote to find the answer, divided up by the question numbers.
** You will not get credit for questions answered in Excel without corresponding SQL queries **
** The SQL queries should deliver ONLY the data requested (unless noted)**

Remember: Deliverables are two files: Excel and SQL File.
Excel: You copy the table from here and then create visualization(s) and provide an answer to the question.
SQL File: There are 16 queries necessary at minimum. You can use multiple queries for #3.

# Database Information

There are some terms you need to understand in order to use this DB:

    MIN: Mobile Identification Number: unique number assigned by the wireless service provider. (account #)
    MDN: The phone number
    IMEI: International Mobile Equipment Identity: unique number for identifying a device on a mobile network. (like your vehicles VIN)

There are 6 tables in the sample of Ex-Mobile's DB.

    Subscriber: Subscriber information including address, MDN and MIN.
    Device: information about the devices used at Ex-Mobile and has IMEI
    DirNums: identifys the city and state of each MDN and connects it with an IMEI
    MPlan: table of the plans used at Ex-Mobile. Has data, throttle and cost
    Bill: table of the current bills for each MIN, includes bill costs
    LastMonthUsage: table of the last month of usage for each MIN, includes minutes, data in MB and texts


# Visualizations in Excel

When creating visualizations for these summary tables, please be sure they make sense. You may find that creating one visualization for each table doesn't make sense because some of it may be unreadable. It is your job to determine if the visualization makes sense and if not, split it into multiple visualizations. Include a few comments
about the visualization such as "City A has the highest average texts" or something of that nature. This is the creative part of the assignment where you are expected to spend a little time creating a professional and creative solution.

 
# The Report Questions (with Visualizations)

Each question number will have their tables pasted to a different Excel sheet. Be sure all copied tables are OFFICIAL Excel tables and have headings.

    Our first goal is to get an idea of some summary data. Please get us the following summary tables and show a visualization for each:
    (A) Show us the first and last names of our customers along with their minute usage, data usage, text usage and total bill. Order them by their full name.
    (B) Show us the average of the minutes, data, texts and total bills by city.
    (C) Show us the sum of the minutes, data, texts and total bills by city.
    (D) Show us the average of the minutes, data, texts and total bills by mobile plan.
    (E) Show us the sum of the minutes, data, texts and total bills by mobile plan.


# The Report Questions (without Visualizations)

For the following questions, you do not need to create visualizations but rather it will be about answering questions based on the query results. Please copy the table into the sheet for the question section (so 1 is one sheet. 2 is another sheet with A, B and C on it). To the right of the table, do analysis on the table and answer the question posed by the question. The answer may be obvious and you are encouraged to analyze it anyway, providing recommendations on how to use the data. Be creative! You still need to have these SQL queries in the SQL file. This must be done in Excel. You are not required to include analysis in the SQL file comments, only in the Excel file.

1. Marketing asked where we should be focusing our new marketing at. We have decided that we want to put our efforts increasing our customer base in cities we currently have customers in instead of marketing in cities we have no customers in. Let's figure out which three cities we should point our markets to. (Hint: we should  be marketing to cities we have the least number of customers in. Be careful and keep this in mind when answering the three queries below.)
    (A) First though, I want to know which two cities we have the most customers in.
    (B) Then show me which cities we should increase our marketing in.
    (C) Finally, show us which plan (only one) we should market the most based on the number of people who have them (infer if they are marketing to least or most customer using common sense and the paragraph intro to this question for what they want to market to cities based on).

 2. Next we want some information on the actual devices our customers use.
    (A) Show us the count of cell phone types with count among our customers. What type do most of our customers use?
    (B) Show us which customers (first and last name) use the phone type that is least used by our customers so we can send them a promotion for their friends and family.  You can use the answer from 2A in this query.
    (C) Finally, show us our customers and the year of their phones who have phones released before 2018?

3. Now we are trying to figure out if our customers are using our data plans efficiently. We have Unlimited plans that throttle the data at specific limits and then there are plans for caps on data usage. We want to know ultimately if there is a city that uses a lot of data (within the top 3 data using cities) but none of our customers in that city are using the Unlimited Plans. If there is a city like that, which one is it? 

4. Our financial department has requested a few items of information.
    (A) They wish to know the first and last name of the customer who has the most expensive bill last month.
    (B) They also want to know which mobile plan delivered the highest total bill last month.

5. Finally, we want to get some information on minutes usage.
    (A) Please tell us which area code (only the area code) uses the most minutes, return the minutes also.
    (B) Lastly, Which cities do we see the biggest difference in terms of minutes usage? In other words, which cities have the biggest difference between the customers who use smallest amount of minutes to customers that use the largest. Use the difference of customers who use less than 200 and customers who use more than 700 minutes.
