# Kullanıcı Girişi
Patika.dev > Java101 > Koşullu İfadeler ve Kod Blokları > Pratik2 - Kullanıcı Girişi

## Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız.

		import java.util.*;
		
		public class kullaniciGirisi {

			public static void main(String[] args) {
				// Yeni bir tarayıcı(scanner) oluştur.
				Scanner sc = new Scanner(System.in);
		
				// Kullanıcıdan kullanıcı adı ve şifresini isteyin.
				System.out.println("Kullanıcı Adınız:");
				String kullaniciAdi = sc.nextLine();
		
				System.out.println("Şifreniz: ");
				String sifre = sc.nextLine();
		
				// Kullanıcının bilgilerinin doğruluğunu kontrol edin. Eğer yanlışsa şifresini sıfırlamak isteyip istemediğini sorun.
				if (kullaniciAdi.equals("patika") && sifre.equals("java123"))
					System.out.println("Giriş Yaptınız");

				else
					System.out.println("Bilgileriniz Yanlış! Şifrenizi sıfırlamak ister misiniz? "
							+ "\n1-Evet\n2-Hayır ");
					int secim= sc.nextInt();
			
					switch(secim) {
					case 1:
						System.out.println("Yeni şifre giriniz: ");
						String sifre2 = sc.nextLine();
						if (sifre2.equals(sifre))
							System.out.println("Şifre oluşturulamadı, lütfen başka şifre giriniz.");
						else 
							System.out.println("Şifre oluşturuldu");
						break;
					case 2: 
						System.out.println("Şifre sıfırlanmıyor. Yeniden deneyiniz.");
						break;
					}
			}
		}
