Tool capture url:
https://www.analytics-debugger.com/tools/ios-android-debugger/


Sign apk


keytool -genkey -v -keystore {ten_keystore} -alias {alias} -keyalg RSA -keysize 2048 -validity 10000  --> tao keystore

//test
keytool -genkey -v -keystore keystore -alias manroid -keyalg RSA -keysize 2048 -validity 10000

jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore {ten_keystore} {ten_apk_can_sign} {alias} --> sign keystore


// doi ten file apk -> zip
//test
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore keystore app.apk manroid --> sign keystore


zipalign -v 4 {ten_apk_unsign} {ten_apk_signed}_signed.apk

//test
zipalign -v 4 app.apk app_signed.apk





Ví dụ check apk thì có thể dùng cmd để check
cho nhanh


Nếu chưa biết thì dùng lệnh này :
appt dump badging {tên file apk}


//======================================

jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore vn_funtap_tqvuonggia.keystore vnsg01_20190307.apk f05_vn{alias}


zipalign -v 4 vnsg01_20190307.apk vnsg01_20190307_signed.apk


//======================================
				WIFI
platform5G
dkmD0ngDut294

dontchangethiswordsdontchangethiswords


//======================================
			TEST RESIGN



//tên file
f05_vn
//package
vn.funtap.tqvuonggia
//đây là pass keystore
A6B698F2FE21AD756335EFD00BED6693

//câu lệnh
keytool -genkey -v -keystore vn_funtap_tqvuonggia.keystore -alias f05_vn -keyalg RSA -keysize 2048 -validity 10000
keytool -list -v -keystore vn_funtap_tqvuonggia.keystore -alias f05_vn -storepass A6B698F2FE21AD756335EFD00BED6693 -keypass A6B698F2FE21AD756335EFD00BED6693
5C:A1:4C:27:40:0F:8F:E5:17:8F:46:0A:02:FE:BB:95:3B:86:32:99



1. Xóa META-INF của apk cần sign ( if  có ) 
2. Sign theo cú pháp:
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore <file key store> <file APK > <alias>

vd : 

3. Nhập pas vào

4. Đặt lại tên cho file resign :

