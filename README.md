#SauceLib 
本意为尝试各种新鲜的技术 提高自身技术水平 生命不息 学习不止
##injectExtra 
使用注解提取Extra 
```java
public class ExampleActivity extends AppCompatActivity {
    @InjectExtra("data")
    String data;
    @InjectExtra("math")
    int math = 200;   

    public static void start(Context context) {
        Intent starter = new Intent(context, Main2Activity.class);
        starter.putExtra("data", "hello world");
        context.startActivity(starter);
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        BindExtra.inject(this);
        setContentView(R.layout.activity_main2);
     } 
}

```
Download
--------

```groovy


allprojects {
    repositories {
     jcenter()
    }

}



dependencies {
   compile  "me.sauce:injectExtra:0.2.1"
   annotationProcessor "me.sauce:injectExtra-compiler:0.2.1"
}
```