# First Order Inductive Learner (FOIL)

This repository contains a full-stack implementation of FOIL (First Order Inductive Learner).  

You could access the application [here](https://forl-frontend-bf4076558d69.herokuapp.com).

## Prerequisites

**Versions Used:**
- **Java:** 17.0.9
- **Node.js:** 18.12.1
- **npm:** 8.19.2
- **Apache Maven:** 3.9.4

Ensure that you have the above versions of tools installed. If not, you can download them from their official websites:

- [Java](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Node.js & npm](https://nodejs.org/)
- [Apache Maven](https://maven.apache.org/download.cgi)

## Running the Application Locally

   ```bash
  git clone https://github.com/Stevehee/FORL-local.git
  cd FORL-local
  mvn spring-boot:run
  cd src/main/frontend
  npm install 
  npm start 
   ```

Once both backend and frontend are running, access the application at http://localhost:3000.


The core logic of FOIL is inside src/main/java/com/FOIL/services/logic directory:

## Files

- `DataSet.java`: Handles data loading from files and data manipulation.
- `Literal.java`: Represents a predicate with arguments.
- `Predicate.java`: Base class for a predicate.
- `Rule.java`: Represents a rule in the form of a head literal and a body of literals.
- `Tuple.java`: Represents an instance of data as a list of literals.
- `FOIL.java`: The main class that drives the FOIL algorithm.

## Usage

Result for an example run :

Head: isGreater 1 ()  
Body: Marital Status 2 (Married-civ-spouse), Education 2 (Bachelors), Occupation 2 (Exec-managerial), Workclass 2 (Private)

Head: isGreater 1 ()  
Body: Relationship 2 (Husband), Occupation 2 (Prof-specialty), Education 2 (Prof-school), Workclass 2 (Self-emp-inc)

Head: isGreater 1 ()  
Body: Sex 2 (Male), Education 2 (Masters), Native Country 2 (United-States), Workclass 2 (Federal-gov)

Head: isGreater 1 ()  
Body: Relationship 2 (Wife), Workclass 2 (Local-gov), Education 2 (Doctorate)

Head: isGreater 1 ()  
Body: Race 2 (White), Occupation 2 (Sales), Workclass 2 (Self-emp-not-inc), Native Country 2 (Canada)
