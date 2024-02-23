package com.example.myapplicationtwo

import android.content.Intent
import android.os.Bundle
import android.util.Log
import android.view.View
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity


class MainActivity : AppCompatActivity() {

    private val TAG = "MainActivity"
    var count: Int = 0
    private val countVariableKey = "COUNT_VARIABLE"
    var dataView: TextView? = null

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        Log.d(TAG, "onCreate")
        dataView = findViewById<TextView>(R.id.dataView)
        dataView!!.text = " Count: " + count
    }

    override fun onStart() {
        super.onStart()
        Log.d(TAG, "onStart")
    }

    override fun onResume() {
        super.onResume()
        Log.d(TAG, "onResume")
    }

    override fun onRestart() {
        super.onRestart()
        Log.d(TAG, "onRestart")
    }

    override fun onPause() {
        super.onPause()
        Log.d(TAG, "onPause")
    }

    override fun onStop() {
        super.onStop()
        Log.d(TAG, "onStop")
    }

    override fun onDestroy() {
        super.onDestroy()
        Log.d(TAG, "onDestroy")
    }

    // сохранение состояния
    override fun onSaveInstanceState(outState: Bundle) {
        count += 1
        outState.putSerializable(countVariableKey, count)
        super.onSaveInstanceState(outState)
        Log.d(TAG, "onSaveInstanceState")
    }

    // получение ранее сохраненного состояния
    override fun onRestoreInstanceState(savedInstanceState: Bundle) {
        super.onRestoreInstanceState(savedInstanceState)
        count = savedInstanceState.getInt(countVariableKey)
        dataView?.setText(" Count: " + count)
        Log.d(TAG, "onRestoreInstanceState")
    }

    fun onClick(view: View) {
        val intent = Intent(this, SecondActivity::class.java)
        intent.putExtra(countVariableKey, count);
        startActivity(intent)
    }

}

