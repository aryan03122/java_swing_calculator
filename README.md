import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JButton;
import java.awt.BorderLayout;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.JTextField;
import javax.swing.SwingConstants;
import java.awt.Color;

public class Design_calc {
	double first ,  second , result;
	String operation;
	private JFrame frame;
	private JTextField textField;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Design_calc window = new Design_calc();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Design_calc() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.getContentPane().setBackground(Color.GRAY);
		frame.setBounds(100, 100, 450, 300);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JButton b1 = new JButton("1");
		b1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b1.getText();

				textField.setText(number);
			}
		});
		b1.setBounds(35, 90, 41, 23);
		frame.getContentPane().add(b1);
		
		JButton b2 = new JButton("2");
		b2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b2.getText();

				textField.setText(number);
			}
		});
		b2.setBounds(109, 90, 46, 23);
		frame.getContentPane().add(b2);
		
		JButton b3 = new JButton("3");
		b3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b3.getText();

				textField.setText(number);
			}
		});
		b3.setBounds(188, 90, 46, 23);
		frame.getContentPane().add(b3);
		
		JButton b4 = new JButton("4");
		b4.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b4.getText();

				textField.setText(number);
			}
		});
		b4.setBounds(35, 124, 41, 23);
		frame.getContentPane().add(b4);
		
		JButton b5 = new JButton("5");
		b5.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b5.getText();

				textField.setText(number);
			}
		});
		b5.setBounds(109, 124, 46, 23);
		frame.getContentPane().add(b5);
		
		JButton b6 = new JButton("6");
		b6.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b6.getText();

				textField.setText(number);
			}
		});
		b6.setBounds(188, 124, 46, 23);
		frame.getContentPane().add(b6);
		
		JButton b7 = new JButton("7");
		b7.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b7.getText();

				textField.setText(number);
			}
		});
		b7.setBounds(34, 158, 42, 23);
		frame.getContentPane().add(b7);
		
		JButton b8 = new JButton("8");
		b8.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b8.getText();

				textField.setText(number);
			}
		});
		b8.setBounds(109, 158, 46, 23);
		frame.getContentPane().add(b8);
		
		JButton b9 = new JButton("9");
		b9.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b9.getText();

				textField.setText(number);
			}
		});
		b9.setBounds(188, 158, 44, 23);
		frame.getContentPane().add(b9);
		
		JButton b0 = new JButton("0");
		b0.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String number=textField.getText()+b0.getText();

				textField.setText(number);
			}
		});
		b0.setBounds(109, 192, 46, 23);
		frame.getContentPane().add(b0);
		
		JButton btnNewButton = new JButton("+");
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first=Double.parseDouble(textField.getText());

				textField.setText("");

				operation="+";
			}
		});
		btnNewButton.setBounds(264, 112, 41, 35);
		frame.getContentPane().add(btnNewButton);
		
		JButton button_10 = new JButton("-");
		button_10.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first=Double.parseDouble(textField.getText());

				textField.setText("");

				operation="-";
			}
		});
		button_10.setBounds(315, 114, 41, 33);
		frame.getContentPane().add(button_10);
		
		JButton button_11 = new JButton("*");
		button_11.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first=Double.parseDouble(textField.getText());

				textField.setText("");

				operation="*";
			}
		});
		button_11.setBounds(264, 152, 41, 35);
		frame.getContentPane().add(button_11);
		
		JButton button_12 = new JButton("/");
		button_12.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first=Double.parseDouble(textField.getText());

				textField.setText("");

				operation="/";
			}
		});
		button_12.setBounds(315, 152, 41, 35);
		frame.getContentPane().add(button_12);
		
		JButton button_13 = new JButton("=");
		button_13.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String answer;

				second=Double.parseDouble(textField.getText());

				if(operation=="+")

				{

				result=first+second;

				answer=String.format("%.2f",result);

				textField.setText(answer);
			}
				if(operation=="-")

				{

				result=first-second;

				answer=String.format("%.2f",result);

				textField.setText(answer);
			}
				if(operation=="/")

				{

				result=first/second;

				answer=String.format("%.2f",result);

				textField.setText(answer);
			}
				if(operation=="%")

				{

				result=first%second;

				answer=String.format("%.2f",result);

				textField.setText(answer);
			}
				if(operation=="*")

				{

				result=first*second;

				answer=String.format("%.2f",result);

				textField.setText(answer);
			}}
		});
		button_13.setBounds(188, 192, 43, 23);
		frame.getContentPane().add(button_13);
		
		JButton button_14 = new JButton(".");
		button_14.setBounds(35, 192, 41, 23);
		frame.getContentPane().add(button_14);
		
		textField = new JTextField();
		textField.setBounds(10, 34, 358, 45);
		frame.getContentPane().add(textField);
		textField.setColumns(10);
		
		JButton btnDel = new JButton("CLR");
		btnDel.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				textField.setText(null);
			}
		});
		btnDel.setBounds(267, 227, 89, 23);
		frame.getContentPane().add(btnDel);
		
		JButton btnDel_1 = new JButton("DEL");
		btnDel_1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String backSpace=null;

				if(textField.getText().length()>0)

				{

				StringBuilder str= new StringBuilder(textField.getText());

				str.deleteCharAt(textField.getText().length()-1);

				backSpace=str.toString();

				textField.setText(backSpace);

				}
			}
		});
		btnDel_1.setBounds(267, 81, 89, 23);
		frame.getContentPane().add(btnDel_1);
		
		JButton btnNewButton_1 = new JButton("%");
		btnNewButton_1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				first=Double.parseDouble(textField.getText());

				textField.setText("");

				operation="%";
			}
		});
		btnNewButton_1.setBounds(264, 192, 89, 23);
		frame.getContentPane().add(btnNewButton_1);
	}
}
