import java.util.*;

public class Main
{
  public static void main(String[] args) {
      Person person = new Person();
      person.readName();
      person.readFriends();
      person.printDescription();
    
  }
}

class Person{
    String name = "";
    List<String> friends = new ArrayList<String>();
                                                                            
    public void readName(){
        Scanner scanner = new Scanner(System.in);
    System.out.println("What is your name??");
    name = scanner.nextLine();
    }
    
    public void readFriends(){              
         String name;
         Scanner scanner = new Scanner(System.in);
         do {
            System.out.println("Enter your frinds name:");
            name = scanner.nextLine();
            if (name.equals("stop") || name.equals("")){
                break;
            }
            friends.add(name);
        }
        while (true);
    }
    
    public void printDescription(){
        if (friends.size() == 0){
        System.out.println("Hello, " + name);
    }else{
        System.out.println(name + " your friends are " + friends);
    }
    }
}
