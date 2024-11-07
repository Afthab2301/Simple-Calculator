# Simple-Calculator
Simple Calculator designed using 'Swing' packages in java.

import java.awt.Color;
<br>
import java.awt.Font;
<br>
import java.awt.event.ActionEvent;
<br>
import java.awt.event.ActionListener;
<br>

import javax.swing.JButton;
<br>
import javax.swing.JFrame;
<br>
import javax.swing.JLabel;
<br>
import javax.swing.SwingConstants;
<br>


public class Calculator implements ActionListener {

    boolean isOperatorClicked=false;
    String oldValue;
    int clickMull;
    

    JFrame jf;
    JLabel displaylabel;
    JButton sevenbutton,eightbutton,ninebutton,fourbutton,fivebutton,sixbutton,onebutton,twobutton,threebutton;
    JButton dotbutton,zerobutton,equalbutton,plusbutton,mulbutton,minusbutton,divbutton,clearbutton;


    public Calculator(){
        jf=new JFrame("CALCULATOR");
        jf.setLayout(null);
        jf.setSize(600,600);
        jf.setLocation(400, 100);
        

        displaylabel=new JLabel();
        displaylabel.setBounds(30, 50, 540, 50);
        displaylabel.setBackground(Color.LIGHT_GRAY);
        displaylabel.setOpaque(true);
        displaylabel.setHorizontalAlignment(SwingConstants.RIGHT);
        displaylabel.setForeground(Color.WHITE);
        displaylabel.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(displaylabel);
        jf.setVisible(true);

        sevenbutton=new JButton("7");
        sevenbutton.setBounds(30, 130, 80, 80);
        sevenbutton.addActionListener(this);
        sevenbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(sevenbutton);

        eightbutton=new JButton("8");
        eightbutton.setBounds(130, 130, 80, 80);
        eightbutton.addActionListener(this);
        eightbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(eightbutton);

        ninebutton=new JButton("9");
        ninebutton.setBounds(230, 130, 80, 80);
        ninebutton.addActionListener(this);
        ninebutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(ninebutton);

        fourbutton=new JButton("4");
        fourbutton.setBounds(30, 230, 80, 80);
        fourbutton.addActionListener(this);
        fourbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(fourbutton);

        fivebutton=new JButton("5");
        fivebutton.setBounds(130, 230, 80, 80);
        fivebutton.addActionListener(this);
        fivebutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(fivebutton);

        sixbutton=new JButton("6");
        sixbutton.setBounds(230, 230, 80, 80);
        sixbutton.addActionListener(this);
        sixbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(sixbutton);

        onebutton=new JButton("1");
        onebutton.setBounds(30, 330, 80, 80);
        onebutton.addActionListener(this);
        onebutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(onebutton);

        twobutton=new JButton("2");
        twobutton.setBounds(130, 330, 80, 80);
        twobutton.addActionListener(this);
        twobutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(twobutton);

        threebutton=new JButton("3");
        threebutton.setBounds(230, 330, 80, 80);
        threebutton.addActionListener(this);
        threebutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(threebutton);

        dotbutton=new JButton(".");
        dotbutton.setBounds(30, 430, 80, 80);
        dotbutton.addActionListener(this);
        dotbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(dotbutton);

        zerobutton=new JButton("0");
        zerobutton.setBounds(130, 430, 80, 80);
        zerobutton.addActionListener(this);
        zerobutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(zerobutton);

        equalbutton=new JButton("=");
        equalbutton.setBounds(230, 430, 80, 80);
        equalbutton.setBackground(Color.GREEN);
        equalbutton.addActionListener(this);
        equalbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(equalbutton);

        divbutton=new JButton("/");
        divbutton.setBounds(330, 130, 80, 80);
        divbutton.addActionListener(this);
        divbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(divbutton);

        mulbutton=new JButton("*");
        mulbutton.setBounds(330, 230, 80, 80);
        mulbutton.addActionListener(this);
        mulbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(mulbutton);

        minusbutton=new JButton("-");
        minusbutton.setBounds(330, 330, 80, 80);
        minusbutton.addActionListener(this);
        minusbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(minusbutton);
        
        plusbutton=new JButton("+");
        plusbutton.setBounds(430, 130, 80, 380);
        plusbutton.addActionListener(this);
        plusbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(plusbutton);

        clearbutton=new JButton("C");
        clearbutton.setBounds(330, 430, 80, 80);
        clearbutton.setBackground(Color.RED);
        clearbutton.addActionListener(this);
        clearbutton.setFont(new Font("Arial", Font.PLAIN, 30));
        jf.add(clearbutton);


    }
    public static void main(String args[]){
        new Calculator();
    }


   
    public void actionPerformed(ActionEvent e){
        if(e.getSource()==sevenbutton){
            if(isOperatorClicked){
                displaylabel.setText("7");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"7");
            }
        }
        else if (e.getSource()==eightbutton) {
            if(isOperatorClicked){
                displaylabel.setText("8");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"8");
            }
        }
        else if(e.getSource()==ninebutton){
            if(isOperatorClicked){
                displaylabel.setText("9");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"9");
            }
        }
        else if(e.getSource()==fourbutton){
            if(isOperatorClicked){
                displaylabel.setText("4");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"4");
            }
        }
        else if(e.getSource()==fivebutton){
            if(isOperatorClicked){
                displaylabel.setText("5");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"5");
            }
        }
        else if(e.getSource()==sixbutton){
            if(isOperatorClicked){
                displaylabel.setText("6");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"6");
            }
        }
        else if(e.getSource()==onebutton){
            if(isOperatorClicked){
                displaylabel.setText("1");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"1");
            }
        }
        else if(e.getSource()==twobutton){
            if(isOperatorClicked){
                displaylabel.setText("2");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"2");
            }
        }
        else if(e.getSource()==threebutton){
            if(isOperatorClicked){
                displaylabel.setText("3");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"3");
            }
        }
        else if(e.getSource()==dotbutton){
            if(isOperatorClicked){
                displaylabel.setText(".");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+".");
            }
        }
        else if(e.getSource()==zerobutton){
            if(isOperatorClicked){
                displaylabel.setText("0");
                isOperatorClicked=false;
            }
            else{
                displaylabel.setText(displaylabel.getText()+"0");
            }
        }
        else if(e.getSource()==equalbutton){
            String newValue=displaylabel.getText();
            float oldValueF=Float.parseFloat(oldValue);
            float newValueF=Float.parseFloat(newValue);

            if(clickMull==0){
                float resultF=oldValueF*newValueF;
                displaylabel.setText(resultF+"");  
            }
            else if(clickMull==1){
                float resultF=oldValueF/newValueF;
                displaylabel.setText(resultF+"");  
            }
            else if(clickMull==2){
                float resultF=oldValueF+newValueF;
                displaylabel.setText(resultF+"");  
            }
            else if(clickMull==3){
                float resultF=oldValueF-newValueF;
                displaylabel.setText(resultF+"");  
            }
             
        }
        else if(e.getSource()==mulbutton){
            isOperatorClicked=true;
            oldValue=displaylabel.getText();
            clickMull=0;
        }
        else if(e.getSource()==divbutton){
            isOperatorClicked=true;
            oldValue=displaylabel.getText();
            clickMull=1;
        }
        else if(e.getSource()==plusbutton){
            isOperatorClicked=true;
            oldValue=displaylabel.getText();
            clickMull=2;
        }
        else if(e.getSource()==minusbutton){
            isOperatorClicked=true;
            oldValue=displaylabel.getText();
            clickMull=3;
        }
        else if(e.getSource()==clearbutton){
            displaylabel.setText("");
        }
    }
}
