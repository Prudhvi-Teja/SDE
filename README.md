# SDE
Preparation for SDE 


(987)-654-3210


import com.google.i18n.phonenumbers.PhoneNumberUtil;
import com.google.i18n.phonenumbers.Phonenumber;

public class PhoneNumberConverter {
    public static void main(String[] args) {
        // Replace this with the phone number you want to convert
        String phoneNumberStr = "9876543210";
        
        // Create an instance of PhoneNumberUtil
        PhoneNumberUtil phoneNumberUtil = PhoneNumberUtil.getInstance();
        
        try {
            // Parse the phone number
            Phonenumber.PhoneNumber phoneNumber = phoneNumberUtil.parse(phoneNumberStr, "US"); // Replace "US" with the appropriate country code
            
            // Convert the phone number to the desired format without spaces and dashes
            String formattedNumber = "(" + phoneNumberUtil.format(phoneNumber, PhoneNumberUtil.PhoneNumberFormat.NATIONAL).replace(" ", "").replace("-", "") + ")";
            
            System.out.println("Formatted Number: " + formattedNumber);
        } catch (Exception e) {
            System.err.println("Invalid phone number: " + phoneNumberStr);
            e.printStackTrace();
        }
    }
}









 // Replace this with the phone number you want to format
        String phoneNumberStr = "9876543210";

        // Check if the phone number has 10 digits
        if (phoneNumberStr.length() == 10) {
            // Format the phone number as (XXX)XXX-XXXX
            String formattedNumber = "(" + phoneNumberStr.substring(0, 3) + ")" +
                                     phoneNumberStr.substring(3, 6) + "-" +
                                     phoneNumberStr.substring(6);
            
            System.out.println("Formatted Number: " + formattedNumber);
        } else {
            System.err.println("Invalid phone number: " + phoneNumberStr);
        }
    }
