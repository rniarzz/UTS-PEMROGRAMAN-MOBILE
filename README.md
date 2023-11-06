![Screenshot (365)](https://github.com/rniarzz/UTS-PEMROGRAMAN-MOBILE/assets/115542704/5e716fd6-6038-4c3a-b4fb-3aca71b2f0c3)<h1 <p align="center"><b>UTS MOBILE</b></p></h1> 

**Nama: Rini Ariza**

**NIM: 312210337**

**Kelas: TI.22.A3**

---

## Menambahkan Kodingan Java

ini adalah kodingan utama untuk menjalankan program bilangan fibonacci

```java
    package com.hellotoast;
    
    import android.os.Bundle;
    import android.view.View;
    import android.widget.EditText;
    import android.widget.TextView;
    import android.widget.Toast;
    
    import androidx.appcompat.app.AppCompatActivity;

    public class MainToast extends AppCompatActivity {
    private TextView showCount;
    private int count = 0;
    private long fibNMinus1 = 1;
    private long fibNMinus2 = 0;
    private EditText edit_max_fibonacci;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_toast);

        showCount = findViewById(R.id.show_count);
        edit_max_fibonacci = findViewById(R.id.edit_max_fibonacci);

        updateCountDisplay();

        fibNMinus1 = 0;
        fibNMinus2 = 1;
    }

    private void updateCountDisplay() {
        showCount.setText(String.valueOf(fibNMinus2));

        if (count % 4 == 0) {
            showCount.setTextColor(getResources().getColor(R.color.colorPrimary));
        } else if (count % 4 == 1) {
            showCount.setTextColor(getResources().getColor(R.color.colorAccent));
        } else if (count % 4 == 2) {
            showCount.setTextColor(getResources().getColor(R.color.colorPrimary));
        } else {
            showCount.setTextColor(getResources().getColor(R.color.colorAccent));
        }
    }

    public void showToast(View view){
        Toast.makeText(this, "Bilangan Fibonacci",
                Toast.LENGTH_SHORT).show();
    }

    public void countUp(View view) {
        int maxFibonacci = Integer.parseInt(edit_max_fibonacci.getText().toString());

        if (count >= maxFibonacci) {
            Toast.makeText(this, "Maksimum Fibonacci tercapai", Toast.LENGTH_SHORT).show();
            return;
        }

        long fibCurrent;
        if (count == 0 || count == 0) {
            fibCurrent = 1;
        } else {
            fibCurrent = fibNMinus1 + fibNMinus2;
        }

        fibNMinus2 = fibNMinus1;
        fibNMinus1 = fibCurrent;
        updateCountDisplay();

        count++;
    }

    public void back1(View view) {
        count = 1;
        fibNMinus1 = 1;
        fibNMinus2 = 0;
        updateCountDisplay();
    }
    }

```
### output

![Screenshot (365)](https://github.com/rniarzz/UTS-PEMROGRAMAN-MOBILE/assets/115542704/6300f179-2918-4a2a-a06b-9f36f9566d60)

![Screenshot (364)](https://github.com/rniarzz/UTS-PEMROGRAMAN-MOBILE/assets/115542704/710cb2e6-60ef-4e07-8f1c-7be2eed8e2c0)

![Screenshot (363)](https://github.com/rniarzz/UTS-PEMROGRAMAN-MOBILE/assets/115542704/e2c01031-70e2-48d6-9389-e8f06cb0786a)

---

<h1 <p align="center"><b>======== Sekian Terima Kasih ==========</b></p></h1>
