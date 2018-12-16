# SoftwareDesign_MobileDevice . 

**01**   
  
Read Java Vs. Kotlin  
---  

![img](https://github.com/xu9449/SoftwareDesign_MobileDevice/blob/master/img/from_java_to_kotlin.png)    
  
[Java Vs Kotlin]( https://github.com/MindorksOpenSource/from-java-to-kotlin)
  
  
Complete Kotlin Koans   
---
[link](https://try.kotlinlang.org/#/Examples/Hello,%20world!/Simplest%20version/Simplest%20version.kt)  
Lambdas : annomenous function  
Higer - Order Functions - Kotlin are first - class  
supports passing functions as arguments to other functions, returning them as the value from other function   
First class :方便了函数的复用
[什么是 pass by value， pass by function， pass by argument](https://github.com/xu9449/SoftwareDesign_MobileDevice/wiki/%E4%BB%80%E4%B9%88%E6%98%AFpass-by-value%EF%BC%8C-pass-by-reference%EF%BC%8C-pass-by-argument)  


**02**   

Itroduction of Kotlin   (google) . 
data class   
(Val)read only . 
top entry point of Kotlin   
In kotlin , you can put everthing in top level   
.copy()  the same value as before if you don't input anything 
interop between java and kotlin  
It don't have getters and setters, it only have properties 
Kotlin don't have semicolons 
extension
there are several you can extend   
null point exception   
question mark   
safe operator (?.) if it is not null, then do something   
higer order function    
create a pair  
algebraic data type . 
opem modifier . 
sealed  
eager evaluation .  
companion object  == static   
call back method  
activity lifecycle    

Stopping an Activity  
---
```  
// 1
val taskDescription = descriptionText.text.toString()

if (!taskDescription.isEmpty()) {
  // 2
  val result = Intent()
  result.putExtra(EXTRA_TASK_DESCRIPTION, taskDescription)
  setResult(Activity.RESULT_OK, result)
} else {
  // 3
  setResult(Activity.RESULT_CANCELED)
}

// 4
finish()
```  
Registering Broadcast Receivers  
---  
```
companion object {
  private const val LOG_TAG = "MainActivityLog"

  private fun getCurrentTimeStamp(): String {
    val simpleDateFormat = SimpleDateFormat("yyyy-MM-dd HH:mm", Locale.US)
    val now = Date()
    return simpleDateFormat.format(now)
  }
}
  
  private fun makeBroadcastReceiver(): BroadcastReceiver {
  return object : BroadcastReceiver() {
    override fun onReceive(context: Context, intent: Intent?) {
      if (intent?.action == Intent.ACTION_TIME_TICK) {
        dateTimeTextView.text = getCurrentTimeStamp()
      }
    }
  }
}
```   
  Review and bookmark this Kotlin cheatsheet . 
  

[Intro to Android Activities in Kotlin](https://www.raywenderlich.com/500-introduction-to-android-activities-with-kotlin)   
[Device Compatibility overview   ](https://developer.android.com/guide/practices/compatibility) . 
APK provides an optimized user experience on a variety of devices . 
Yet, a device is "Android compatible" only if it can correctly run apps written for the Android execution environment.    Each device must pass the Compatibility Test Suite (CTS) in order to be considered compatible
   
Each platform version specifies an API level.  
The minSdkVersion attribute declares the minimum version with which your app is compatible and the targetSdkVersion attribute declares the highest version on which you've optimized your app.  
  
Intent : messaging object you can use to request an action fro another app component.  
Building an intent:    
ComponentName    
Action  
Data  
 The type of data supplied is generally dictated by the intent's action.
Category  
Extras  
Flags
  
**03**  
[Kotlin tips]（https://savvyapps.com/blog/kotlin-tips-android-development）  
Lazy Loading  

 
---     

lElvis operator  : val length2: Int? = name?.length  
If: val more = if (x > y) x else y;   
Sets ignore duplicate items  
[lambda](https://juejin.im/entry/58a382da61ff4b0058ab4542)
  
Read Kotlin Tips  
---
[link](https://savvyapps.com/blog/kotlin-tips-android-development)  
### Lazy Loading  
1) faster startup time  
2) memory efficient  
3)encapsulate initialization  
### Custom Getters/Setters  
simply access other modifier  
### Lambdas  
reduce the overall lines of code  
allow functional programming 
### Data Classes  
### Collection Filtering  
### Object Expressions  
### Companion Object  
### Global Constants  
constants should be kept to as small a scope as possible to reduce complexity  
### Optional Parameters  
### Extensions  
### Lateinit  
### Safe Typecasting    

### Leveraging Let    
let automatically assign user to an unnullable variable  
### Isnullorempty | Isnullorblank  
provide benefit of checking for just whitespace  
### Avoiding single abstract method for classes  
SAM(Single abstract method)  
### Coroutines instead of asynctask  
  
Code along with ListView Tutorial  
---
[link](https://www.raywenderlich.com/155-android-listview-tutorial-with-kotlin)  
What exacgtly is an adapter  
private lateinit var listView ListView (缺少冒号）  

 Read ListView vs RecyclerView  
 ---  
 
   [link](https://www.thedroidsonroids.com/blog/what-is-the-difference-between-listview-recyclerview)
   1. ViewHolder
    2. LayoutManager
      3.ItemDecoration
                        therecylerviewlisthasnodividersvetweenrowasbydefaultandit'sconsistentwithethematerialdesignguidelines 
  4. IteAnimator 
  
   Code along with Design Tutorial  
   ---
   
Recycle List View  
---  
  
    
# iOS_Application_Design   

[An illustrated history of iOS](https://www.git-tower.com/blog/history-of-ios) .   
2007: iPhone OS1, First iPhone 
2008: iPhone OS2, SDK, AppStore
2009: iOS3, iPad, copy/paste, Spotlight, voice control, Skeuomorphism . 
2010: iOS4, multitaking,folders, wallpapers, Mail, FaceTime, Retina . 
2011: iOS5, iCloud, iMessage, Notification Center, Twitter, Siri  
2012: iOS6, YouTube and Google Maps no longer perinstalled, Shared Photo Streams, Facebook, Passbook
2013: iOS7, (the world is not flat anymore) design change, Jony Ive, Touch ID, Control Center , AirDrop . 
2014: iOS8, Continuity(read and write iMessages), Notification Center Widgets, HealthKit, HomeKit. 
2015: iOS9, Proctivity(predict its users' needs. Maps, performance & stability improvements  
2016: iOS10, iMessage Stickers, App Store, Home, Notifications . 
2017: iOS11, App Store, customizable Control Center, Quick Type keyboard, Photos, Files app and Dock . 
2018: iOS12, Performance, long-standing limitation of Facetime, new Screen Time
  
[Introduction： Swift for Complete Beginners](https://www.hackingwithswift.com/read/0/overview)  
\()  
type(of: songs)  
what is type safety  : like only store strings in the list    
var songs: [String] = [ , , , ]  
var songs: [String]  
songs[0] = " "  
  
  for _ in 1 ... 5 {
    str += " fake"
}
  Section 2.
  [Intro to StroyBoards](https://www.raywenderlich.com/464-storyboards-tutorial-for-ios-part-1)   
  Segue 继续
