# Settings Reference

This integration requires a valid Clickatell account and an SOAP API endpoint. Fill this in the first 3 fields labelled API ID, username and password. Note that the API ID that is created by default when you open the Clickatell account is a REST API ID, which will not work with current integration. Follow instructions at step 2 above for setting up a SOAP API ID.

The Clickatell integration allows the following configuration options:
* Message

This can be a text message, or it can be a token that references the actual message. The token can be either a form field, in which case it will pull whatever value was submitted with form, or it can be a My Token. Note that an SMS is limited to 160 chars. If the message is larger, it will be split automatically by Clickatell, and may be merged back into a single message depending on the delivery network and the receiver phone.

* Max. Length of the Message

This parameter is optional and allows administrators to limit the size of the messages that can be sent (for example, content submitted by users or content derived from user tokens). If set, it must be an integer. If left empty, there is no limit imposed by the administrator. Be aware that there is a limit though imposed by Clickatell, which is  5355 characters (SMS gateway technical  limits). The extension will truncate the text to this Clickatell maximum, even if field is left empty.

* Phone Number(s) to Send TO

SMS messages need to be sent in the standard international format, with country code followed by number. No leading zero to the number and no special characters such as "+" or spaces must be used. For example, a number in the UK being 07901231234 should be changed to 447901231234. You can send to more that one number by placing one phone number per line. The phone numbers can be hardcoded or can come from tokens - either form tokens such as [PhoneNumber] or DNN/My Tokens such as [Profile:Cell].

