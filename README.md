# Capstone
## Synopsis
This is my capstone final titled Mock Banking Site(With ATM Intergration). You can create your own account if you do not already have one and access your checking and savings account. You are able to check the balances, withdraw, deposit, and transfer between both accounts.
## Motivation
I decided to build this just for fun. I wanted something that the user can interact with in a simple manner.
## How to Run
The files needed are Account.java, Checking.java, Savings.java, and ATM.java. The file you need to run is ATM.
## Code I Am Proud Of 
```
	    		 btYes.setOnAction(i -> {
	    			 double d = Double.parseDouble(tfTransAmount.getText().toString());
	    			  if(cmboFrom.getValue() == "Checking") {
	    				  if(checking.canWithdraw(d) && checking.getBalance() > 0 && d <= checking.getBalance()) {
	    					checking.withdraw(d);
	  	  			  		savings.deposit(d);
	  	  			  		primaryStage.setScene(choiceScene);
	    				  }
	    				  else {
	    						Button btReturn = new Button("Back");
	    			  			Label lblLimit = new Label("Cannot Withdraw From Checking. Amount Exceeds Balance");
	    			  			Label lblBalance = new Label("Account balance: $" + checking.getBalance());
	    			  			if(checking.getBalance() > 0) {
	    			  				lblBalance.setTextFill(Color.GREEN);
	    			  			}
	    			  			lblLimit.setTextFill(Color.RED);
	    			  			gpConfirm.getChildren().remove(lblAmountConfirm);
	    			  			gpConfirm.getChildren().remove(hbTrans);
	    			  			gpConfirm.add(lblLimit, 1, 0);
	    			  			gpConfirm.add(lblBalance, 1, 1);
	    			  			gpConfirm.add(btReturn, 1, 2);	    			  			
//Return to Transfer Scene 			  				
	    			  			btReturn.setOnAction(m -> {	
	    			  				primaryStage.setScene(transferScene);
	    			  			});	    					  
	    				  }
	    			  }
```
The main reason I am proud of this code is actually because it took me a while to get the combo boxes working, but once I figured it out I was able to make everything belond where it needed to be and work properly. All the problems I ran into were relatively small but required a little bit of thinking, and even if they were easy fixes, I am proud of being able to fix every bug I ran into.
## Contributors
The biggest contributors to my project were Rich Mallek, Jason Adams, and of course, Javadocs!
