# SoftwareDesign_MobileDevice . 
  
Read Java Vs. Kotlin  
---  

![img](https://github.com/xu9449/SoftwareDesign_MobileDevice/blob/master/img/from_java_to_kotlin.png)    
  
[Link]( https://github.com/MindorksOpenSource/from-java-to-kotlin)
  
Complete Kotlin Koans   
---
[link](https://try.kotlinlang.org/#/Examples/Hello,%20world!/Simplest%20version/Simplest%20version.kt)  
Lambdas : annomenous function  
Higer - Order Functions - Kotlin are first - class  
supports passing functions as arfuments to other functions, returning them as the value from other function   
First class :方便了函数的复用
[什么是 pass by value， pass by function， pass by argument](https://github.com/xu9449/SoftwareDesign_MobileDevice/wiki/%E4%BB%80%E4%B9%88%E6%98%AFpass-by-value%EF%BC%8C-pass-by-reference%EF%BC%8C-pass-by-argument)  


Kotlin . 
Itroduction of Kotlin   (google) . 
data class   
new tyoe money  (Val)read only . 
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
Review and bookmark this Kotlin cheatsheet  
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
  
      
