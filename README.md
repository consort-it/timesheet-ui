# Beets UI (Bee timesheet)
**Beets** app provides simple time tracking, managing and exel export functions for small companies with little traffic. It was develeped in Angular and tailored to the needs of **Consort Center of Excellence**. Every employee can enter the working hours per day and project in the tracking view, display his record history in the managing view and create new customers and projects in the customers view.

---

## How to use

1. First steps
  * [Create new user](#create-new-user)
  * [First login](#first-login)
  * [Choose company from list](#choose-company-from-list)

---

2. Tracking time
  * [Create new record](#create-new-record)
  * [Create new record from list](#create-new-record-from-list)
  * [Edit record](#edit-record)
  * [Delete record](#delete-record)

---

3. Manging Records
  * [Display your own record history](#Display-your-own-record-history)
  * [Display company record history](#Display-company-record-history)
  * [Export excel file](#Export-excel-file)

---

4. Managing customers and projects
  * [Create new customer](#create-new-customer)
  * [Edit customer](#edit-customer)
  * [Delete customer](#delete-customer)
  * [Create new project](#create-new-project)
  * [Edit project](#edit-project)
  * [Delete project](#delete-project)

---

5. Technical overview
  * [Components](#components)

---

## 1. First steps

#### Create new user
To create a new user please login in the AWS Cognito. For further information check out our [how to create new cognito user](#link) tutorial.

#### First login
After the first login to the beets app you'll have to change your temporery password (which you'll find in your email) and fill out some additional information about yourself.

**Please pay attention to the AWS Cognito password policy:**

![first login](/img/first_login.png)

#### Choose company from list
Every time you login you can choose your company from the dropdown menu. To change the company you have to logout first.

**Please note: The right company is necessary for accounting and invoice.**

![company login](/img/company_login.png)

---

## 2. Tracking time

#### Create new record
To create a new record 
 * go to the tracking view by selecting *Tracking* in the upper left burger menu 
 * then click on the *plus icon* in the toolbar bellow the date picker
 * fill out required informations and click on *add*
 
![new record](/img/new_record.png) ![new record_2](/img/new_record_2.png)

#### Create new record from list
This function has to be implemented yet.

#### Edit record
This function has to be implemented yet.

#### Delete record
To delete a record
 * go to the tracking view by selecting *Tracking* in the upper left burger menu
 * select the right date and the record from list by clicking on it
 * click on the *delete icon* which will show up in the upper toolbar after you selected a record

![delete record](/img/delete_record.png)

---

## 3. Manging Records

#### Display your own record history
To display your own record history
 * go to the managing view by selecting *Managing* in the upper left burger menu
 * and click on the *user* tab
 
You can switch the months statistics by clicking on the left and right arrows.
 
![manage user](/img/manage_user.png)

#### Display company record history 
To display company record history
 * go to the managing view by selecting *Managing* in the upper left burger menu
 * and click on the *company* tab.
 
#### Export excel file 
To export an excel file
 * go to the managing view by selecting *Managing* in the upper left burger menu
 * click on the *company* tab
 * scroll down to the buttom of the list
 * and press on the *export excel* button

**Please note: By pressing the export excel button the app will export every entry of the chosen month.**

You can switch the months statistics by clicking on the left and right arrows.
 
![manage user](/img/manage_user.png)

---

## 4. Managing customers & projects

#### Create new customer
To create a new customer
 * go to the customers view by selecting *Customers* in the upper left burger menu
 * then click on the *plus icon* in the toolbar
 * fill out required informations and click on *add*

By creating a new customer you also need to create a new project.

![create customer](/img/create_customer.png) ![create customer 2](/img/create_customer_2.png)

#### Edit customer
This function has to be implemented yet.

#### Delete customer
To delete a customer
 * go to the customers view by selecting *Customers* in the upper left burger menu
 * select the right customer from list by clicking on it
 * click on the *delete icon* which will show up in the upper toolbar after you selected a customer
 
**Please note: By deleting a customer**
1. you also delete all projects for this customer
2. you DO NOT delete it from the database but only from the UI
3. the already created records will NOT be deleted. You stil can find them in your tracking and managing view
4. you stil be able to export already created records in the excel overview
5. you will no longer be able to track new records for this customer or its projects

To restore deleted customers, please contact the administrator.

![delete_customer](/img/delete_customer.png)
 
#### Create new project
To create a new project
 * go to the customers view by selecting *Customers* in the upper left burger menu
 * choose a customer by clicking one the arrow on the right side of each customers row
 * then click on the *plus icon* in the toolbar
 * fill out required informations and click on *add*

![create project](/img/create_project.png) ![create project 2](/img/create_project_2.png) ![create project 3](/img/create_project_3.png)

#### Edit project
This function has to be implemented yet.

#### Delete project
To delete a project
 * go to the customers view by selecting *Customers* in the upper left burger menu
 * choose a customer by clicking one the arrow on the right side of each customers row
 * select the project you want to delete by clicking on it
 * click on the *delete icon* which will show up in the upper toolbar after you selected a project

![delete project](/img/delete_project.png) ![delete project 2](/img/delete_project_2.png)

---

#### 5. Technical overview

#### Components

![componente overview](/img/component_overview.png)
