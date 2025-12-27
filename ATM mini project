import java.util.*;
class Main {
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.print("Enter the Acc no:");
		int ac=sc.nextInt();
		int blc=100000;

		if(ac>999999&&ac<9999999) {
			for(int i=0; i<=5; i++) {
			    if (i == 4) {
					int penalty = blc / 2; 
					blc -= penalty;
					System.out.println("penalty Applied (50%) : " + penalty);
					System.out.println("Balance After Penalty: " + blc);
				}
				if (i == 5) {
					int penalty = blc / 4; 
					blc -= penalty;
					System.out.println("penalty Applied (25%) : " + penalty);
					System.out.println("Balance After Penalty: " + blc);
					break;
				}
				System.out.print("Acc Type\n1.Saving \n2.Current \nSelect Acc Type:");
				int ent_acc_type=sc.nextInt();
				switch(ent_acc_type) {
				case 1:
				case 2:
					System.out.print("1.Withdraw \n2.Deposit \n3.Bal Enquiry \nSelect the Transction Type:");
					int at=sc.nextInt();
					switch(at) {
					case 1:
						System.out.print("Enter the Withdraw Amount:");
						int wi=sc.nextInt();
						if(wi<=blc) {
							if (ent_acc_type == 1 && (blc - wi) < 1000) {
								System.out.println("Minimum balance for Saving Account is 1000");
							}
							else if(ent_acc_type ==2) {
								if((blc-wi)<5000) {
									System.out.println("Minimum balance for Saving Account is 5000");
								}
								else {
									wi=wi-15;
									blc = blc - wi;
									System.out.println("Withdrawal Successfull:"+wi);
									System.out.println("Available Balance: " +(double) blc);
								}
							}
							else {
								wi=wi-10;
								blc = blc - wi;
								System.out.println("Withdrawal Successfull:"+wi);
								System.out.println("Available Balance: " + (double)blc);
							}
						}
						else {
							System.out.println("Insufficient Balance");
						}
						break;
					case 2:
						System.out.print("Enter the Deposit Amount:");
						int de=sc.nextInt();
						if(de>=15000) {
							int tax = (de * 15) / 100;
							de=de-tax;
							blc = blc + de;
							System.out.println("Deposit Successful:"+(double)de);
							System.out.println("Available Balance: " +(double) blc);
						}
						else {
							System.out.println("Deposit Successful:"+(double)de);
							System.out.println("Available Balance: " +(double) blc);
						}
						break;
					case 3:
						System.out.println("Available Balance: " + (double)blc);
						break;
					default:
						System.out.println("Invalid Transction Type");
					}
				}
			}

		} 
		else {
			System.out.println("Invalid Acc no");
		}
	}
}
