# Lab2
using System;
using System.Collections.Generic; 
using System.ComponentModel;
using System.Data;
using System. Drawing;
using System.Linq;
using System. Text;
using System. Windows. Forms;

namespace  WindowsFormsApplication1
{
	public partial class Form1 : Form 
	{
	    public Form1()
	    {
	        InitializeComponent();
	        button.Enabled = false;
	        private void textBox1_KeyPass(object sender, KeyPressEventArgs e)
	        {
	            if ((e.Keychar >= '0') && (e.Keychar <= '9'))
	            return;
	            if (e.Keychar == '.') e.Keychar = ',';
	            if (e.Keychar == ',')
	            {
	                if ( (textBox1.Text.IndexOf(',') != -1) || 
	                ( textBox1.Text.Length == 0 ))
	                {
	                    en.Handled = true;
	                }
	                return;
	                
	           
	            }
	            e.Handled = true;
	            
	        }
	        private void textBox1_TextChanged(object sender, EventArgs e)
	        {
	            labe12.Text = "";
	            if (textBox1.Text.Length == 0)
	                button1.Enabled = false;
	            else 
	                button1.Enabled = true; 
	        }
	        
	        private void button1_Click(object sender, EventArgs e)
	        {
	            double funt; 
	            double kg;
	            
	            funt = Convert.Todouble(textBox1.Text);
	            kg = funt * 0.4095;
	            labe12.Text = funt.toString("N") + "ф. = " + kg.toString("N") + " кг."; 
	        }
	    }	 

	   
	
	    
	    
	    
}
