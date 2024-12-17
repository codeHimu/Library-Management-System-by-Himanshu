# Library-Management-System-by-Himanshu
class employee2{
    String name;
    int id;
    int age;
    String designation;

    public employee2(String name, int age, int id, String designation) {
        this.name = name;
        this.age = age;
        this.id = id;
        this.designation = designation;
    }
    public String toString()
    {
        return "\n"+"name = "+name+" age = "+age+" id = "+id+" Designation = "+designation;
    }
}
class employee20 {
    ArrayList<employee2> emp;

    public employee20(ArrayList<employee2> emp) {
        this.emp = emp;
    }

    public void addEmployee(employee2 name) {
        emp.add(name);
    }
    public void removeEmployee(employee2 name,int id)
    {
       emp.remove(name);
    }

    public void showEmployee() {
        System.out.println(emp);
    }
    public void viewEmployee(employee2 name)
    {
        
    }
}
public class EmployeeManagement {
    public static void main(String[] args) {
        ArrayList<employee2> bk = new ArrayList<>();
        employee2 b1=new employee2("Himanshu",19,101,"Java developer");
        bk.add(b1);
        employee20 obj = new employee20(bk);
        obj.addEmployee(new employee2("Ram",20,102,"python developer"));
        obj.removeEmployee(b1,101);
        obj.showEmployee();
        obj.addEmployee(new employee2("Vedant",24,103,"Financial advisor"));
        obj.addEmployee(new employee2("Bhumika",21,102,"Consultant"));
        obj.addEmployee(new employee2("Harsh",230,102,"head of HR"));
        obj.showEmployee();
    }
}
