# BusinessRulesEngineRepository
Adding a repository

# In Actual all the classes(Service and Concrete classes) should be in different class file.

# Service Class Implementation : for all other new  rules , we can extend  the logic here

Public Class PaymentRuleService
{
 Public void PaymentMethod()
  {
    If (this.GetType().Name== "PhysicalProduct")
    {
      # Logic for generate a packing slip for shipping and generate a commission payment to the agent
    }
    If (this.GetType().Name== "Book")
    {
      # Logic for Create a duplicate packing slip for the royalty depaertment
    }
    If (this.GetType().Name== "Membership")
    {
      # Logic for activate that MemberShip as well as email the owner and inform them for the membership
    }
    If (this.GetType().Name== "UpgradeMembership")
    {
      # Logic for apply the  upgrade as well as email the owner and inform them about the upgrade
    }
    If (this.GetType().Name== "Video")
    {
      # Logic to add a  free "First Aid" video to the packing slip.
    }
  }
}

# Concrete  Class Implementation

Public Class PhysicalProduct : PaymentRuleService
{
 # logic for all other methods and properties
}
Public Class Book : PaymentRuleService
{
 # logic for all other methods and properties
}
Public Class Membership : PaymentRuleService
{
 # logic for all other methods and properties
}
Public Class UpgradeMembership : PaymentRuleService
{
 # logic for all other methods and properties
}
Public Class Video : PaymentRuleService
{
 # logic for all other methods and properties
}

# Payment Method call implementation

Public Class Payment
{
  PhysicalProduct physicalProd = new PhysicalProduct();
  physicalProd.PaymentMethod();
  
  Book book = new Book();
  book.PaymentMethod();
  
  # Similar logic should bewritten for all other payment classess
}
