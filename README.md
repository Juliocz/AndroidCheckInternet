# AndroidCheckInternetReal
Bueno queria compartirles este pequeño aporte, con la cual podran codificar y saber cuando hay conexion real de internet

# Aqui les muestro un ejemplo...
```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        HCheckInternet nH_checkInternet=new HCheckInternet();
        nH_checkInternet.setListener(new HCheckInternet.onlinelistener() {
        @Override
        public void isConnect(boolean connect) {
            //recibe señal true o false si hay conexionreal, la conexion se verifica cada 1,5s
        }});nH_checkInternet.execute();//Inicia el hilo
            nH_checkInternet.stop();//detiene el hilo
        
        }   
 }
```

Con esto podran verificar la conexion real de internet, la conexion se verifica cada 1.5s, esto tambien lo pueden cambiar pero no lo recomiendo, otro detalle es que no modifiquen la clase.
Esto le sera de utilidad, si desean verificar la conexion en tiempo real.

Esto fue todo hazta la proxima
