# Connection with Supabase 
(
## LOGIN TO SUPABASE>

  ### STEP 1
  Open the supabase website
  login using your gmail account
  click new project
  enter your project name
  click to create project>

  ## DATABASE SCHEMA>

  ### STEP 2
  after creating the supabase project
  open sql editor from the left sidebar
  paste your sql code
  click run
  the required table will be created in supabase database
  for example>
   ``sql
   create table department (
        department_id   INT PRIMARY KEY,
        department_name  null
        location         Varchar(100)
   )
   ``
   then we run this if it has error or anything wrong it immediately show in the bottom>

## VISUAL STUDIO CODE>

### STEP 3
open visual studio code
open new terminal
all the next.js commands will run in the VS CODE

## CREATE THE NEXT.JS PROJECT>

### STEP 4
in the VS CODE
open command prompt
write cd desktop
then create the next.js project
npx create-next-app@latest nimra-sup
it will ask some questions like do you want to work in typescript or more after you 
answer it will create the project 
after the project is created
cd nimra-sup

## INSTALL SUPABASE>

### STEP 5 
install the supabase app
npm install @supabase - supabase-js
npm run dev
this allow the supabase to connect with VS CODE
open the project in supabase
open the folder
nimra-sup
all the work will appear there
package.js
data
page.js
env.local

## STEP 6
open the supabase
when you work on sql editor on the top there is a small button
connect through which we can connect our work from supabase to VS CODE
create a page in VS CODE naming env.local
when we click the connect button
copy the code written there and add them to the page env.local
for example
``javascript

NEXT_PUBLIC_SUPABASE_URL=https://aslmyrbhwewnrjngndgf.supabase.co
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=sb_publishable_20cYjzKpWfY_IYxEGRyEzw_ZqRx8XIx

``

this will appear after you click the connect button >

## Lib.folder>

### STEP 7
in VS CODE create a folder 
name it lib
inside the lib folder create a new file 
supabase.js
lib\supabase.js
connect next.js with supabase
write the code here
for example
const supabase url=process.env NEXT PUBLIC SUPABASE URL,
this code connects next.js application to supabase>

## Department.folder>
### STEP 8
write in sql editor

``sql 
create table department(
department_id  INT PRIMARY KEY,
department_name  VARCHAR(100) NOT NULL,
location    NOT NULL
);

``
## insert 

insert row level security so no one can miss use it 
create a table in sql

``sql
enable row level security
for example
Create policy "Allow anon read" on department
for select to anon using (true);

create policy "Allow anon insert " on department
for insert to anon with check (true);
enable this privacy>

)