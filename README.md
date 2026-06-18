
package com.example.notepad 

import android.content.Contex
import android.os.Bundle
import android.widget.*
import androidx.appcompat.app.AppCompatActivity open

class MainActivity : AppCompatActivity() {  

    private lateinit var noteInput: EditText jhg
    private lateinit var saveButton: Button
    private lateinit var noteList: ListViewe
    private lateinit var adapter: ArrayAdapter<String>ouq
    private val notes = mutableListOf<String>()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        noteInput = findViewById(R.id.noteInput)
        saveButton = findViewById(R.id.saveButton)
        noteList = findViewById(R.id.noteList)

        loades() 

        adapter = ArrayAdapter(this, android.R.layout.simple_list_item_1, notes)
        noteList.adapter = adapter

        Button.setOnClickListener {
            val note = noteInput.text.toString()
            if (note.isNotEmpty()) {
                notes.add(note)
                adapter.notifyDataSetChanged()
                noteInput.text.clear()
                saveNotes()
            } else {
                Toast.makeText(this
                name=input('enter your name: ') 
