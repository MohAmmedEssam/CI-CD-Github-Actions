HI THERE !!

If you need to us Github Actions in your native iOS project you need to add this file to your project and do some changes.

You need to have some files from your app store connect profile.

First: -

 - Development Certificate -> then add it to your keychain then export it again as .p12 file
 - Distribution Certificate -> then add it to your keychain then export it again as .p12 file
 - Development provision profile
 - app store provision profile
 - go to users and access and create app store connect api key
    there is 3 params you need to get with this step (key file, key name, issuer id) all in the same page
    Note: this file only downloaded once take care not to loose it

Second: -
 - Go to your Xcode project and sign it manually using the Development certificate and the Development provision profile
 - archive and export your app to your Desktop, open the folder you exported and get the file named ExportOptions.plist

put all your files in one folder to could manage it easy way.

Now you got 2 Certificate, 2 provision profile, 1 api key, 1 ExportOptions plist

add .github folder you download from this repo to your project directory

convert all those files you got to base 64 string and add it to the .yml file

push the .github folder to your main branch

Enjoy !!

Reference : https://www.andrewhoog.com/post/how-to-build-an-ios-app-with-github-actions-2023/
