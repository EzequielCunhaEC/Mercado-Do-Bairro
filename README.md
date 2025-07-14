```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">

    <Button
        android:id="@+id/btnAddProduct"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Publicar Produto"
        android:background="#D32F2F"
        android:textColor="#FFFFFF" />
MainActivity.kt`
`onCreate( ```kotlin
val btnAdd = findViewById<Button>(R.id.btnAddProduct)
btnAdd.setOnClickListener { )
    val intent = Intent(this, AddProductActivity::class.java)
    startActivity(intent)
}
    <ListView
        android:id="@+id/listViewProducts"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:dividerHeight="10dp"
        android:layout_marginTop="16dp" />
</LinearLayout>
```
*2. list_item_product.xml* (formato de cada produto)
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:orientation="horizontal"
    android:padding="8dp"
    android:background="#EEEEEE">

    <ImageView
android:id="@+id/imgProduct"
        android:layout_width="80dp"
        android:layout_height="80dp"
        android:src="@mipmap/ic_launcher"
        android:layout_marginEnd="8dp" />

    <LinearLayout
        android:orientation="vertical"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:id="@+id/txtProductName"
            android:text="Nome do Produto"
            android:textStyle="bold"
            android:textSize="16sp" />

        <TextView
            android:id="@+id/txtProductPrice"
            android:text="Preço"
            android:textColor="#D32F2F"
            android:textSize="14sp"
            android:layout_marginTop="4dp" />
    </LinearLayout>
```kotlin
class AddProductActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_add_product)

        val btnSave = findViewById<Button>(R.id.btnSaveProduct)
        val edtName = findViewById<EditText>(R.id.edtProductName)
        val edtPrice = findViewById<EditText>(R.id.edtProductPrice)
        val edtContact = findViewById<EditText>(R.id.edtProductContact)

        btnSave.setOnClickListener {
            val name = edtName.text.toString()
            val price = edtPrice.text.toString()
            val contact = edtContact.text.toString()
           if (name.isBlank() || price.isBlank() || contact.isBlank()) {
                Toast.makeText(this, "Preencha todos os campos", Toast.LENGTH_SHORT).show()
                return@setOnClickListener
            }
 Toast.makeText(this, "Produto salvo!", Toast.LENGTH_SHORT).show()
            finish()
        }
    }
}
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical" android:padding="16dp"
    android:layout_width="match_parent" android:layout_height="match_parent">

    <EditText android:id="@+id/edtProductName"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Nome do Produto"/>

    <EditText android:id="@+id/edtProductPrice"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Preço"/>

    <EditText android:id="@+id/edtProductContact"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Número WhatsApp"/>
<Button android:id="@+id/btnSaveProduct"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Salvar Produto"
        android:background="#D32F2F"
        android:textColor="#FFFFFF"
        android:layout_marginTop="20dp"/>

</LinearLayout>
```

