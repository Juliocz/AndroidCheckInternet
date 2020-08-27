# AndroidCheckInternetReal
Bueno queria compartirles este pequeño aporte, con la cual podran codificar y saber cuando hay conexion real de internet
isNetworkRedconnect(Context context)
# Verificando la Conexion real de internet...
En este ejemplo, podemos verificar si hay una conexion real a internet.
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

# Verificando solo la conexion de Red (Wifi o Datos) 
Esto no garantiza que exista conexion real, solo que la conexion de red esta activa
```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        HCheckInternet nH_checkInternet=new HCheckInternet();
        if(nH_checkInternet.isNetworkRedconnect(this));
        {/*Existe conexion de red*/}
        else
        {/*No hay conexion de red*/}
        }   
 }
```

Con esto podran verificar la conexion real de internet, la conexion se verifica cada 1.5s, esto tambien lo pueden cambiar pero no lo recomiendo, otro detalle es que no modifiquen la clase.
Esto le sera de utilidad, si desean verificar la conexion en tiempo real.

Esto fue todo hazta la proxima
