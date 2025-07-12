Simple Dialog (Custom Layout R.layout) we need to open:
```
<androidx.constraintlayout.widget.ConstraintLayout android:id="@+id/custom_dialog_box_view"Add commentMore actions
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:background="#03A9F4"
    xmlns:app="http://schemas.android.com/apk/res-auto">

        <ImageView
            android:id="@+id/custom_layout_img"
            android:layout_width="50sp"
            android:layout_height="50sp"
            android:src="@drawable/baseline_cloud_done_24"
            app:layout_constraintTop_toTopOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"/>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:layout_constraintTop_toBottomOf="@id/custom_layout_img"
        android:orientation="vertical">

        <TextView
            android:id="@+id/custom_layout_title"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Success"
            android:textAlignment="center"
            android:background="@color/white"
            android:paddingBottom="5sp"
            android:textSize="30sp"/>

        <TextView
            android:id="@+id/custom_layout_txt"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Alright! You may now proceed further."
            android:textAlignment="center"
            android:background="@color/white"
            android:paddingBottom="20sp"
            android:paddingStart="10sp"
            android:paddingEnd="10sp"/>

    </LinearLayout>


</androidx.constraintlayout.widget.ConstraintLayout>
```
and also simpler code to understand the principle:
```
        Dialog dialog = new Dialog(this);Add commentMore actions
        dialog.setContentView(R.layout.custom_dialog_box);
        dialog.show();
        dialog.setCancelable(false); //This is just for locking the dialog (test yourself please)
```
