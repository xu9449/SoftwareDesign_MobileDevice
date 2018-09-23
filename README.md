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
