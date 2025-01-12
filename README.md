# hospital_management_project


import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class Management {

    Management(){

        JFrame frame = new JFrame();
        frame.setTitle("Login Form");
        frame.setLayout(null);
        frame.setSize(2000,1333);

        ImageIcon img = new ImageIcon(getClass().getResource("hospital_background.jpeg"));
        JLabel backgroundlabel =new JLabel(img);
        backgroundlabel.setBounds(0,0,2000,1333);

        
        //main label
        JLabel l1 = new JLabel();

        l1.setText("AIUB HOSPITAL MANAGEMENT SYSTEM");
        l1.setBounds(500,50,1200,50);
        l1.setForeground(Color.BLACK);
        l1.setFont(new Font("Algerian",Font.BOLD,50));

        JLabel box = new JLabel();
        box.setBounds(750,600,400,220);
        box.setBackground(Color.white);

        JLabel l2 = new JLabel();
        l2.setText("Name:");
        l2.setBounds(50,20,400,25);
        l2.setFont(new Font("Times New Roman",Font.BOLD,25));

        JTextField f1 = new JTextField();
        f1.setBounds(210,20,150,25);

        //f1.setBackground(Color.blue);

        JLabel l5 = new JLabel();
        l5.setText("Email:");
        l5.setBounds(50,70,400,30);
        l5.setFont(new Font("Times New Roman",Font.BOLD,25));

        JTextField f5 = new JTextField();
        f5.setBounds(210,70,150,25);

        JLabel l3 = new JLabel();
        l3.setText("Password:");
        l3.setBounds(50,120,400,25);
        l3.setFont(new Font("Times New Roman",Font.BOLD,25));

        JPasswordField f2 = new JPasswordField();
        f2.setBounds(210,120,150,25);

        JButton b1 = new JButton();
        b1.setText("Clear");
        b1.setBounds(50,190,70,20);
        b1.setFont(new Font("Times New Roman",Font.BOLD,15));


        JButton b2 = new JButton();
        b2.setText("Login");
        b2.setBounds(270,190,80,20);
        b2.setFont(new Font("Times New Roman",Font.BOLD,15));


        box.add(b2);
        box.add(b1);
        box.add(f2);
        box.add(l3);
        box.add(l5);
        box.add(f5);
        box.add(f1);
        box.add(l2);
        box.setOpaque(true);
        frame.add(l1);
        frame.add(box);
        frame.add(backgroundlabel);

        b1.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                f1.setText("");
                f2.setText("");
                f5.setText("");

            }
        });

        b2.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                String name4 = "Lamin";
                String email4 = "lamin@gmail";
                String password4 = "Lamin12";

                String name1 = "Bushra";
                String email1 = "bushra@gmail.com";
                String password1 = "Bushra12";

                String name2 = "Nazia";
                String email2 = "nazia@gmail.com";
                String password2 = "Nazia12";

                String name3 = "Emon";
                String email3 = "emon@gmail.com";
                String password3 = "Emon12";

                String name = f1.getText();
                String email = f5.getText();
                String password = String.valueOf(f2.getPassword());

                if (name1.equals(name) && email1.equals(email) && password1.equals(password)||name2.equals(name) && email2.equals(email) && password2.equals(password)){
                    JOptionPane.showMessageDialog(box,"Login Sucess");

                }
                else {
                    JOptionPane.showMessageDialog(box,"Login Failed");
                }
            }
        });


        frame.setVisible(true);
        frame.setDefaultCloseOperation(WindowConstants.EXIT_ON_CLOSE);
    }
}
