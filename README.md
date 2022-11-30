# gyuff
package sportsmanagementsystem;
import java.util.Scanner;
class user
{
   int id;
   String name;
   String gender;
   int contactNo;
   //String enrollNo;
   String email_id;
   String userType;
   //String username;
   String password;
   String teamName;
   
   void setid(int id)
     {
         this.id=id;
     }
     int getid()
     {
         return id;
     }
     
     void setname(String name)
     {
         this.name=name;
     }
     String getjob()
     {
         return name;
     }
     
     void setgender(String gender)
     {
         this.gender=gender;
     }
     String getgender()
     {
         return gender;
     }
     
     void setcontactNo(int contactNo)
     {
         this.contactNo=contactNo;
     }
     int getcontactNo()
     {
         return contactNo;
     }
     
     void setemail_id(String email_id)
     {
         this.email_id=email_id;
     }
     String getemail_id()
     {
         return email_id;
     }
     
     void setuserType(String userType)
     {
         this.userType=userType;
     }
     String getuserType()
     {
         return userType;
     }
     
     void setpassword(String password)
     {
         this.password=password;
     }
     String getpassword()
     {
         return password;
     }
     
   void login()
   {
       System.out.println("Login Page:");
       System.out.println("Enter your id:");
       Scanner sc=new Scanner(System.in);
       String input=sc.nextLine();
       setid(id);
       
       System.out.println("Enter Name:");
       Scanner sc1=new Scanner(System.in);
       String input1=sc.nextLine();
       setname(name);
       
       System.out.println("Enter gender:");
       Scanner sc2=new Scanner(System.in);
       String input2=sc.nextLine();
       setgender(gender);
       
       System.out.println("Enter Contact Number:");
       Scanner sc3=new Scanner(System.in);
       String input3=sc.nextLine();
       setcontactNo(contactNo);
       
       System.out.println("Enter Email:");
       Scanner sc4=new Scanner(System.in);
       String input4=sc.nextLine();
       setemail_id(email_id);
       
       System.out.println("Enter Usertype:");
       Scanner sc5=new Scanner(System.in);
       String input5=sc.nextLine();
       setuserType(userType);
       
       System.out.println("Enter Password:");
       Scanner sc6=new Scanner(System.in);
       String input6=sc.nextLine();
       setpassword(password);
   }
}
class normal extends user
{
    void details()
    {
        this.id=id;
        this.name = name;
        this.teamName= teamName;
        System.out.println("Player's name: " +name);
        System.out.println("Player's ID: "+id);
        System.out.println("The Player is a member of team: "+teamName);
    }
    void selectEvent()
    {
        
    }
    void selectTeam()
    {
        
    }
    void payment()
    {
        
    }
}
class volunteer extends user
{
    void checkParticipant()
    {
        
    }
    void checkTeamDetails()
    {
        
    }
    void updatePayment()
    {
        
    }
    void updateWinner()
    {
        
    }
}
class manager extends user
{
    void addVolunteer()
    {
        
    }
    void checkParticipant()
    {
        
    }
    void checkTeamDetails()
    {
        
    }
    void checkPayments()
    {
        
    }
    void checkWinner()
    {
        
    }
}
class admin extends user
{
    void addManager()
    {
        
    }
    void addVolunteer()
    {
        
    }
    void addEvents()
    {
        
    }
    void checkParticipant()
    {
        
    }
    void checkteamDetails()
    {
        
    }
    void checkPayment()
    {
        
    }
    void checkWinner()
    {
        
    }
}
class team
{
    int id;
    int event_id;
    int teamSize;
    user u = new user();
    
    void setevent_id(int event_id)
     {
         this.event_id=event_id;
     }
     int getevent_id()
     {
         return event_id;
     }
    void selectEvent()
    {
        System.out.println("Outdoor game events are:\n1. Football\n2. Cricket\n3. Badminton\n4. Table Tennis\n5. Basket Ball\nPress any number to get enrolled in any of them");
        Scanner ev=new Scanner(System.in);
        int event_id=ev.nextInt();
        setevent_id(event_id);
        System.out.println("You are  successfully enrolled in:"); 
        switch(event_id)
        {
            case 1:
                System.out.println("Football Team");
                break;
            case 2:
                System.out.println("Cricket Team");
                break;
            case 3:
                System.out.println("Badminton Team");
                break;
            case 4:
                System.out.println("Table Tennis");
                break;
            case 5:
                System.out.println("Basket Ball Team");
                break;
            default:
                System.out.println("Select any of the above!");
                break; 
        }
    }
    void selectTeam()
    {
    
    }
    void payment()
    {
     
    }
}
class event
{
    int id;
    int eventName;
    String organizingDepartment;
    int manager_id;
    int participationAmount;
    int eventType_id;
}
class winner
{
    int id;
    int event_id;
    int user_id;
    int position;
    event e = new event();
}
public class SportsManagementSystem
{
    public static void main(String[] args) 
    {
       user n=new normal();
       n.login();
       team t= new team();
       t.selectEvent();
    }
}
