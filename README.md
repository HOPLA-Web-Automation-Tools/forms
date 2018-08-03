# HOPLA Tools - Forms

## HT-Forms extends Google Forms by allowing users to customize and add more advanced inputs to Forms.

#### Extended Features
* Video/Audio Record - allows respondents to record a video through their webcam.
* Image Capture - allows respondents to take a picture through their webcam.
* Calendar Booking - allows respondents to choose a timeslot from the "free time" that you specifiy in your Google Calendar and create an event in your specified Google Calendar in HT-Forms' chrome extension.

#### Customized question entries such as:
* Image Select - Multiple image select with optional parameters such as maximum allowed selection.
* File Upload - Allows multiple file uploads, allowed file extensions, and file size limits. Uploaded files goes directly to your Google Drive.
* Scale input - Draggable scale input instead of native radio buttons.

### Installation
Install chrome extension: [https://chrome.google.com/webstore/detail/hopla-tools/okpkgekcmfhcdejammfjacanecihmfmo](https://chrome.google.com/webstore/detail/hopla-tools/okpkgekcmfhcdejammfjacanecihmfmo)



### How To Use
#### Sign-in your Google account and accept permissions:
* "View and manage files in your Google Drive" - Allows the script to upload your form's submitted media/files to your Google Drive.
* "View and manage your forms in Google Drive" - Allows the script to retrieve your form's question entries and render your advanced HT-Form.
![signin](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/67ad9ff5-b97e-4afa-a05a-7199e3882fcf/08.02.2018-15.39.GIF)

#### Create your Google Form: https://forms.google.com

Add your Google Form to HT-Forms. Copy your form-key and submit it to the extension. 

Example: If your google form *edit* URL is `https://docs.google.com/forms/d/1Bxl_cospwaErODsNcpovEPRe_HJU7gMvw2ze5jv4TdI/edit`, your key is **1Bxl_cospwaErODsNcpovEPRe_HJU7gMvw2ze5jv4TdI**.


After adding your form to HT-Forms, you should now be able to view your advanced form here: https://form.hopla.tools/?key=[YOUR-FORM-KEY]

![add form](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/299d4693-12d4-4957-be72-ca4f0f1f0dfd/08.02.2018-16.59.GIF)


### Advanced Inputs
*Shortcodes* are used by HT-Forms to parse and create advanced form elements.

For example, to add a Video Record element, you would add a question entry of the type "short answer". And in the question text you would put `[WAT_VIDEO] Record a video`. This will render the video recorder element like this: ![record element](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/4c83ef51-a706-4090-9364-2363245ed9e9/08.02.2018-17.10.png)

Recorded videos submitted by your form respondents will be uploaded directly to your Google Drive under the HOPLA Tools folder.

#### ShortCodes
Optional parameters can be added to shortcodes such as `t=30` to limit the video recording up to 30 seconds.
The short code would become `[WAT_VIDEO t=30]`.

|ShortCode 		| Optional Parameter | Sample Usage   | Question Type | Explanation|
|:--------:    	|:--------------------:|---------------|------------|---------------|
|[HT_VIDEO]		|t=30				 | [HT_VIDEO t=30] Record a video | short answer| Video record element with 30 seconds record limit. See [example](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/4c83ef51-a706-4090-9364-2363245ed9e9/08.02.2018-17.10.png)|
|[HT_AUDIO]		|t=20				 | [HT_AUDIO t=30] | short answer| Audio record element with 20 seconds record limit|
|[HT_IMAGE]		|				 	 | [HT_IMAGE] | short answer| Image capture element|
|[HT_AUDIO]		|t=20				 | [HT_AUDIO t=30] | short answer| Audio record element with 20 seconds record limit|
|[HT_IMAGE]		|				     | [HT_IMAGE] | short answer| Image capture element|
|[HT_FILE]		|size=10mb, amount=5, ext=jpg,pdf|[HT_FILE size=10mb amount=5 ext=jpg,pdf] | short answer| File upload element with limits of up to 5 files, max of 10mb per file, and allows only jpg and pdf file extensions|
[imageurl={URL-GOES-HERE}] | |Option 1 [imageurl=https://yoursite.com.option1.jpg], What kind of animal is this? [imageurl=https://lh3.googleusercontent.com/BPEqSio222fZJCTcTIiOH4An9jWhYrHhLflRpLiDvm9VHuijO-89QAeqyIkmZZDK5U2DYtIZ4R-OkcnttvEL1ya8j6Hnzb7rO6sqTzRVSEsEJ0BcWxt5tR48qEcA3raj8W_1ie1x6Wry6N0] | multiple choice - option, Dropdown | Make's a multiple choice's option as image select instead of the usual text in radio buttons. See [Example 1](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/7d544e8f-2798-4410-b271-c58161d8fcbb/08.03.2018-14.46.png), [Example 2](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/cab60b48-9637-4dfe-9dc4-7aa3b26d18d1/08.03.2018-14.37.png), [Example 3](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/753e4974-0361-47c0-a775-594c40a76109/08.03.2018-14.42.png)
|[video={URL-GOES-HERE}]||Tell us what you think about this video [videourl=https://www.youtube.com/watch?v=dWyBHbBbOCg]| short answer| Adds a video element. See [Example](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/35c3ebb1-496e-4bb4-a390-da8e7a0576d9/08.03.2018-14.48.png)|
|[HT_CALENDAR]||[HT_CALENDAR] Book a slot|short answer|Adds a calendar element that will allow users to create an event to your calendar. Calendar settings must be set in HT-Forms extension. [Example](https://content.screencast.com/users/SilverSerate9052/folders/Default/media/645d62c6-adfa-4db6-9d47-b08341f4c0c6/08.03.2018-14.51.png)|
