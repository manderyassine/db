# Gym Management System - Entity-Relationship Model

## Entities and Attributes

### Gymnasium
- Contains all necessary attributes:
  - `Gymnasium_ID` (Primary Key)
  - `Name`
  - `Address`
  - `Phone_Number` ✅

### Member
- Includes required attributes:
  - `Member_ID` (Primary Key)
  - `Last_Name`
  - `First_Name`
  - `Address`
  - `Date_of_Birth`
  - `Gender`
  - `Gymnasium_ID` (Foreign Key) ✅

### Session
- Covers all needed attributes:
  - `Session_ID` (Primary Key)
  - `Sport_Type`
  - `Schedule`
  - `Max_Members`
  - `Gymnasium_ID` (Foreign Key) ✅

### Coach
- Contains essential attributes:
  - `Coach_ID` (Primary Key)
  - `Last_Name`
  - `First_Name`
  - `Age`
  - `Specialty` ✅

### Associative Entities
#### Session_Member
- Correctly links `Session_ID` and `Member_ID` for many-to-many relationships between Sessions and Members. ✅

#### Session_Coach
- Correctly links `Session_ID` and `Coach_ID` for many-to-many relationships between Sessions and Coaches. ✅

## Relationships
- **Gymnasium to Member**: Represents the "enrolls" relationship with a 1:N cardinality. ✅
- **Gymnasium to Session**: Represents the "offers" relationship with a 1:N cardinality. ✅
- **Session to Coach**: Represents the "includes" (or "teaches") relationship with N:M cardinality. ✅
- **Session to Member**: Represents the "participates in" relationship with N:M cardinality. ✅

---

Feel free to modify or extend this README to include additional details about the system!
