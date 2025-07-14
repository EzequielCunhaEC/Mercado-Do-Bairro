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

    <ListView
        android:id="@+id/listViewProducts"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:dividerHeight="10dp"
        android:layout_marginTop="16dp" />
</LinearLayout>
```

---

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
</LinearLayout>
```

