# Demo
import java.util.Arrays;
import java.util.List;
import java.util.function.Consumer;

import org.omg.Messaging.SyncScopeHelper;

public class demo {

	public static void main(String[] args) 
	{

    List<Integer> values=Arrays.asList(1,2,3,4,5);
    System.out.println("using lamda expression");
  values.forEach(i ->System.out.println(i));  
  
  System.out.println("call by method ");
   values.forEach(System.out::println);  
   System.out.println("using sream API");
   values.stream().forEach(System.out::println);  
   System.out.println("using parallel stream");
    values.parallelStream().forEach(System.out::println);
    System.out.println("print hi");
    values.stream().forEach(i-> {if(i%2==0)
    	{
    	System.out.println("hi");
    	}
    else
    {
    	System.out.println("bye");
    }
    	});
    System.out.println(values.stream().map(i->i).reduce(1,(c,e)->c+e));

}
}
