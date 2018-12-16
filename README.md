# Donor-searching
// Author: Islam Riad
// Program: Donoor Searching Java Programming
// Instructor: Prof. Aaron
// Date: 28-Apr-2017
import java.util.*;
import javax.swing.JOptionPane;
public class PatientDatabasetest2
{
   public static void main(String[] args)
   {
     String[] mNum = {"01", "02", "03", "04", "05", "06", "07", "08", "09", "10"};
     
     String[] ssn = {"880-26-5981", "880-36-5901", "880-46-5912", "880-36-5976", "880-39-8979", "880-89-7845", 
                     "880-78-8698", "880-69-2691", "880-56-5632", "880-32-6548"};
                     
     String[] name = {"Jenifer Lopez", "Lindy Hieght", "Mansoor Khan", "Donald Butt", "Polen Sakar", "Nina Paul",
                      "Liza Afrin", "Mike Colin", "Abby Naj", "Sarah Raina"};
                      
     String[] bDate = {"03/05/1996", "08/27/1984", "06/25/1978", "12/20/1986", "12/20/1988", "09/16/1968", "06/25/1992",
                        "08/29/1990", "03/12/1987", "09/23/1985"}; 
     
     String[] pNum = {"404-564-9532", "404-566-9531", "404-678-9534", "770-328-5523", "770-628-5621", "404-456-2312", 
                        "404-987-2457", "707-564-3219", "404-297-4884", "404-985-5647"};
     String[] cNum = {"404-698-5647", "404-398-5149", "404-398-5149", "404-752-3326", "678-225-3698", "326-564-9875",
                        "329-654-2398", "404-365-6312", "678-654-2132", "404-875-9632"};
       
     String[] pAddress ={"House# 1254 Lainster Dr. SW, Atlanta ,GA 30124",
                         "House# 1745 J1456 Hollowel Road NW, Atlanta, GA 30215",
                         "House# 1546 14th Street, Atlanta, GA 30175",
                         "House# 2156 NorthHils Dr. SE, Duluth, GA 30265",
                         "House# 3264 Circle Oaks Dr Se, Atlanta, GA 30218",
                         "House# 1245 Circlewood Rd Ne, Conyers, GA 30175",
                         "House# 5468 Apple Jack Dr, Douglasville, GA 30165",
                         "House# 2154 Buckner Creek Ct Se, Mableton, GA 30126",
                         "House# 1325 N Sweetwater Rd, Lithia Spring, GA 30189",
                         "House# 1875 Oak Creek Cir, Lithia Spring, GA 30625"};
         
     String[]pHistory = {"Patient both Kidneys are failure and had open heart surgery 2 times for coronary artery bloackage",
                         "Patient liver malfuntion and found symtom of liver seorosis",
                         "Patient left kidney totally failure",
                         "Patient have Heart blockage and liver damage",
                         "Patient has a mental disorder and right kidney failure",
                         "Patient has acute Lungs infection and Diabetes,Both kidneys are failure",
                         "Patient kidney damange by seriours road accident",
                         "Patient has mild Heart attack and both kidney failure",
                         "Patient has no other problem but right Kidney failure",
                          "Patient liver are malfuction"};
                        
     String[] condition = {"moderate", "severe", "moderate", "severe", "moderate", "severe", "moderate", "severe",
                            "moderate", "severe"};
     String[] bodyType = {"S", "M", "L", "S", "M", "L", "S", "M", "L", "S"};
     String[] bloodType = {"A", "O", "A", "B", "A", "O", "B", "A", "O", "A"};
     String dBloodType;
     String dBodyType; 
      int x = 0;
      int y = 5;
      final int MAX = 5;
      final int MAXTWO = 10;
      String input;
      String inputTwo;
      String inputThree;
      String inputFour;
      String inputFive;
      String inputSix;  
     
      input = JOptionPane.showInputDialog(null, "Enter ''1'' to find all patients information at a glance" 
         + "\nEnter ''2'' to find a patient information" + "\nEnter ''3'' to match patient information to donors");
      if(input.equals("1"))
      {
         for(x = 0; x < MAX; ++x)
         {
            JOptionPane.showMessageDialog(null, "Medical no: " + mNum[x] + "\n" + "Patient name: " + name[x] + "\n" + "Condition: "
                + condition[x]);         }
      }
      if(input.equals("2"))
      {
         inputTwo = JOptionPane.showInputDialog(null, "Enter the Medical number of the patient to look up their information");
         {
            for(x = 0; x < MAXTWO; ++x)
            {
               if(mNum[x].contains(inputTwo))
               JOptionPane.showMessageDialog(null,"Patient information: " + "\n" + "Patient no: " +  mNum[x] + "\nSSN: " + ssn[x] + "\nDOB: "
                  + bDate[x] + "\nPatient Name: " + name[x] + "\nPhone number: " + pNum[x] + "\nMobile number: " + cNum[x] + "\nPatient Address: " + pAddress[x]  
                  + "\nPatient Medical History: " + pHistory[x] +
                  "\nCondition: " + condition[x] + "\nPatient bodytype: " + bodyType[x] + "\nPatient bloodtype: " + bloodType[x]);            }
            }
         }
      else if(input.equals("3"))
      {
     
     
         dBodyType = JOptionPane.showInputDialog(null, "Enter the Donor's BodySize, S for small, M for medium, L for large: ");
         dBloodType = JOptionPane.showInputDialog(null, "Enter the donor's bloodtype");
         {
            for(x = 0; x < MAXTWO; ++x)
            {
               if(bodyType[x].equalsIgnoreCase(dBodyType)&& bloodType[x].equalsIgnoreCase(dBloodType))
               {
                  JOptionPane.showMessageDialog(null, "Medical no: " + mNum[x] + "\nPatient Name: " + name[x] 
                     + "\nCondition: " + condition[x] + "\nDonor and Patient are a match");
               }
               else
               {
                  JOptionPane.showMessageDialog(null, "Medical no: " + mNum[x] + "\nPatient Name: " + name[x] + "\nDonor and Patient are not a match");
               }
            }
          } 
       }                              
  
     if(input.equals("1"))
     {
        inputThree = JOptionPane.showInputDialog(null, "Do you want to see the next list of patients?"
              + "\nIf so, enter ''yes''");
        {
           if(inputThree.equals("yes"))
           {
              for(y = 5; y < MAXTWO; ++y)
              {
                 JOptionPane.showMessageDialog(null, "Medical no: " + mNum[y] + "\n" + "Patient name: " + name[y] + "\n" + "Condition: "
                + condition[y]);
              }
           } 
           
          if(input.equals("1"))
          {
             inputFour = JOptionPane.showInputDialog(null,"Do you want to see the patient details Medical information?"
                + "\nIf so, enter ''2''");
             inputTwo = JOptionPane.showInputDialog(null, "Enter the Medical number of the patient to look up their information");
         {
            for(x = 0; x < MAXTWO; ++x)
       
             {
             if(inputFour.equals("2"))
             {
              inputTwo = JOptionPane.showInputDialog(null, "Please Enter Patient Medical no:");
                for(x = 0; x < MAX; ++x)
                {
                  JOptionPane.showMessageDialog(null,"Patient information: " + "\n" + "Patient no: " +  mNum[x] + "\nSSN: " + ssn[x] + "\nDOB: "
                     + bDate[x] + "\nPatient Name: " + name[x] + "\nPhone number: " + pNum[x] + "\nMobile number: " + cNum[x] + "\nPatient Address: " + pAddress[x] 
                     + "\nPatient Medical History: " + pHistory[x] +
                     "\nCondition: " + condition[x] + "\nPatient bodytype: " + bodyType[x] + "\nPatient bloodtype: " + bloodType[x]);
                }
             }
         if(input.equals("1") && inputFour.equals("2"))
         {
            inputSix = JOptionPane.showInputDialog(null, "Do you want to see the next list of patients?"
               + "\nIf so, enter ''yes''");
            {
               for(y = 5; y < MAXTWO; ++y)
               {
                  JOptionPane.showMessageDialog(null, "Patient information: " + "\n" + "Patient no: " +  mNum[y] + "\nSSN: " + ssn[y] + "\nDOB: "
                     + bDate[y] + "\nPatient Name: " + name[y] + "\nPhone number: " + pNum[y] + "\nMobile number: " + cNum[y] + "\nPatient Address: " + pAddress[y] 
                     + "\nPatient Medical History: " + pHistory[y] +
                     "\nCondition: " + condition[y] + "\nPatient bodytype: " + bodyType[y] + "\nPatient bloodtype: " + bloodType[y]);
                }
             }
         }
         if(input.equals("1"))
         {
            inputFive = JOptionPane.showInputDialog(null,"Do you want to see Patient and donor Match status?"
               +"\nif so, enter ''3''");
            {
               if(inputFive.equals("3"))
               {
                  dBodyType = JOptionPane.showInputDialog(null, "Enter the Donor's BodySize, S for small, M for medium, L for large: ");
                  dBloodType = JOptionPane.showInputDialog(null, "Enter the donor's bloodtype");
                  {
                     for(x = 0; x < MAXTWO; ++x)
                     {
                        if(bodyType[x].equalsIgnoreCase(dBodyType)&& bloodType[x].equalsIgnoreCase(dBloodType))
                        {
                           JOptionPane.showMessageDialog(null, "Medical no: " + mNum[x] + "\nPatient Name: " + name[x] 
                              + "\nCondition: " + condition[x] + "\nDonor and Patient are a match");
                        }
                        else
                        {
                           JOptionPane.showMessageDialog(null, "Medical no: " + mNum[x] + "\nPatient Name: " + name[x] + "\nDonor and Patient are not a match");
                        }
                     } 
                   }
                }
         else
         {
            JOptionPane.showMessageDialog(null, "You have exited the program!");
         }
        }
       }
      }   
     }
    }
   }
  }
}
}
