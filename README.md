# railwayticket


   1. private void formWindowActivated(java.awt.event.WindowEvent evt)... to activate the window pane
   2. private void jButton3MouseClicked(java.awt.event.MouseEvent evt) ...to activate exit button                                                                         
     //total button :
    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        //to display the time
        Calendar timer = Calendar.getInstance(); 
        timer.getTime(); 
        SimpleDateFormat tTime = new SimpleDateFormat("HH:mm:ss"); 
        jLabel22.setText(tTime.format(timer.getTime()));  //set time label   
         //to dislay the date
        SimpleDateFormat Tdate = new SimpleDateFormat("dd-MM-yyyy");
        jLabel21.setText(Tdate.format(timer.getTime())); //set date label
         
        jLabel19.setText("DEHRADUN "); //set from label
        jLabel20.setText((String) jComboBox1.getSelectedItem()+ " "); //set to label
         //random no. generation for ticket no.
        int x;
        String a="";
        x=1+(int)(Math.random()*(1+(int)(Math.random()*9999)));
        a+=x;
        jLabel14.setText(a);//set ticket no. label                                      
    //total button
    private void jButton1MouseClicked(java.awt.event.MouseEvent evt)                                    
        // for calculation of total cost
         if(jRadioButton1.isSelected())
         {bp=2800; jLabel7.setText("FIRST CLASS");
           if(jComboBox1.getSelectedItem().equals("KOLKATA"))
           { ep=1500; no="23KOL32";}
           else if(jComboBox1.getSelectedItem().equals("DELHI"))
           { ep=500; no="17DL678";}
           else if(jComboBox1.getSelectedItem().equals("CHENNAI"))
           { ep=2000;no="90CH087";}
           else if(jComboBox1.getSelectedItem().equals("MUMBAI"))
           {ep=1800;no="65MU007";}
         }
         else if(jRadioButton2.isSelected())
         {bp=1500;jLabel7.setText("SECOND CLASS");
            if(jComboBox1.getSelectedItem().equals("KOLKATA"))
            { ep=800;no="23KOL32";}
           else if(jComboBox1.getSelectedItem().equals("DELHI"))
            { ep=200;no="17DL678";}
           else if(jComboBox1.getSelectedItem().equals("CHENNAI"))
            {ep=1000;no="90CH087";}
           else if(jComboBox1.getSelectedItem().equals("MUMBAI"))
           {ep=600;no="65MU007";}
         }
         else if(jRadioButton3.isSelected())
         {bp=800;jLabel7.setText("THIRD CLASS");
           if(jComboBox1.getSelectedItem().equals("KOLKATA"))
           {ep=300;no="23KOL32";}
           else if(jComboBox1.getSelectedItem().equals("DELHI"))
           { ep=100;no="17DL678";}
           else if(jComboBox1.getSelectedItem().equals("CHENNAI"))
           {ep=500;no="90CH087";}
           else if(jComboBox1.getSelectedItem().equals("MUMBAI"))
           { ep=400;no="65MU007";}
         }
        else if(jRadioButton4.isSelected())
         { bp=300;jLabel7.setText("SLEEPER CLASS");
            if(jComboBox1.getSelectedItem().equals("KOLKATA"))
            {ep=180;no="23KOL32";}
           else if(jComboBox1.getSelectedItem().equals("DELHI"))
            {ep=80;no="17DL678";}
           else if(jComboBox1.getSelectedItem().equals("CHENNAI"))
           { ep=250;no="90CH087";}
           else if(jComboBox1.getSelectedItem().equals("MUMBAI"))
           { ep=100;no="65MU007";}
         }
        if(jCheckBox1.isSelected())
           t=1;//adult
        else if(jCheckBox2.isSelected())
           t=0.5;//child
         double total=bp+(ep * t);
        String a=String.format(" Rs. ",total);
        jLabel16.setText(a);//set label total
        jLabel18.setText(a);
        jLabel15.setText(no);set class label
        


    // Variables declaration                     
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JButton jButton3;
    private javax.swing.JCheckBox jCheckBox1;
    private javax.swing.JCheckBox jCheckBox2;
    private javax.swing.JComboBox<String> jComboBox1;
    private javax.swing.JLabel jLabel1........
