package com.example.myapplicationtwo

import android.os.Bundle
import android.util.Log
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity
import java.lang.String
import kotlin.Int


class SecondActivity : AppCompatActivity() {

    private val TAG = "SecondActivity"
    private var count: Int = 0
    private val countVariableKey = "COUNT_VARIABLE"
    var textView: TextView? = null

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_second);
        textView = TextView(this)
        textView!!.textSize = 26f
        textView!!.setPadding(16, 16, 16, 16)

        val arguments = intent.extras
        if (arguments != null) {
            count = arguments.getInt(countVariableKey)
            val value: Int = count
            val result = Math.pow(value.toDouble(), 2.0)
                .toInt() // возвращает число a, возведенное в степень b
            count = result
            textView!!.text = "Count: " + String.valueOf(count)
        }
        setContentView(textView)
    }

    // сохранение состояния
    override fun onSaveInstanceState(outState: Bundle) {
        outState.putSerializable(countVariableKey, count)
        super.onSaveInstanceState(outState)
        Log.d(TAG, "onSaveInstanceState")
    }

    // получение ранее сохраненного состояния
    override fun onRestoreInstanceState(savedInstanceState: Bundle) {
        super.onRestoreInstanceState(savedInstanceState)
        count = savedInstanceState.getInt(countVariableKey)
        textView?.setText(" Count: " + count)
        Log.d(TAG, "onRestoreInstanceState")
    }

}

