# Calculator.java
creating a own calculator
import java.awt.*;
import java.awt.event.*;
public class calculator extends Frame implements ActionListener
 {
     TextField t1,t2,t3;
     
     Label l1,l2,l3;
     Button b1,b2,b3,b4;
     calculator()
     {
      l1 = new Label("Enter First");
      l2 = new Label("Enter Second");
      l3 = new Label("Result");
    
      t1 = new TextField(20);
      t2 = new TextField(20);
      t3 = new TextField("");
      
      b1 = new Button("+");
      b2 = new Button("-");
      b3 = new Button("*");
      b4 = new Button("/");
      setLayout (new GridLayout(6,2));
      add(l1);
      add(t1);
      add(l2);
      add(t2);
      add(l3);
      add(t3);
    
      add(b1);
      add(b2);
      add(b3);
      add(b4);
      
      b1.addActionListener(this);
      b2.addActionListener(this);
      b3.addActionListener(this);
      b4.addActionListener(this);
      setVisible(true);
      setSize(200,200);
      addWindowListener(new WindowAdapter()
      {
          public void windowClosing(WindowEvent we)
          {
              System.exit(0);
            }
        });

     
    }
    public static void main(String args[])
    {
        new calculator();
    }
    public void actionPerformed(ActionEvent ae)
    {
        int n1=Integer.parseInt(t1.getText());
int n2=Integer.parseInt(t2.getText());
if(ae.getSource()==b1)
{
t3.setText(String.valueOf(n1+n2));
}
if(ae.getSource()==b2)
{
t3.setText(String.valueOf(n1-n2));
}
if(ae.getSource()==b3)
{
t3.setText(String.valueOf(n1*n2));
}
if(ae.getSource()==b4)
{
t3.setText(String.valueOf(n1/n2));
}


    }
    
}
