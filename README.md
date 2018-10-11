﻿# NewRepo2MINalgorithm
მომხმარებელმა უნდა შემოიტანოს 10 რიცხვი რომელსაც დაიმახსოვრებთ მასივში ან ლისტში, კონსოლში უნდა დაბეჭდოთ ამ მასივში არსებული ორი ყველაზე მინიმალური რიცხვის ჯამი

პირველ რიგში ვქმნით მასივს და ვავსებთ user-ის მიერ შემოტანილი მნიშვნელობებით;
შემდეგ ვიწყებთ ორი მინიმუმის ძიებას მასივში შესაბამისი ალგორითმის საშუალებით;
ალგორითმის მუშაობის პრინციპი შემდეგნაირია: 
				      1. ვქმნით ორ ცვლადს და ვანიჭებთ მასივის პირველ ორ მნიშვნელობას 
					int min1 = arr[0];
           				int min2 = arr[1];
				      2.ჩვენი მიზანია min1-ში ეწეროს arr[0]-სა და arr[1] შორის მინიმალური რომელსაც შემდეგნაირად ვშვრებით:
					if (min2 < min1)
           				 {
             				   min1 = arr[1];
               				   min2 = arr[0];
           				 }
				      3. ამის შემდეგ ვატრიალებთ ციკლს i=2 დან მასივის ბოლომდე და ვცდილობთ მინიმუმების შენახვას შემდეგნაირად
					for (int i = 2; i < arr.Length; i++)
           				 {
               					 if (arr[i] < min1)
               					 {
                   					 min2 = min1;
                   					 min1 = arr[i];
                				}
               					 else if(arr[i] < min2)
               					 {
                  					  min2 = arr[i];
               					 }
           				 }

				      4. საბოლოოდ ვბეჭდავთ შესაბამისი მნიშვნელობების ჯამს 

					int sum = min2 + min1;
          				Console.WriteLine("ori minimaluri elementi: " + min1 + "  " + min2+'\n'+"Jami: "+sum);			