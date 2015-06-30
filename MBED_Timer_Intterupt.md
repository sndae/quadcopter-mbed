## Make a timer interrupt: ##

[http://mbed.org/forum/mbed/topic/906/?page=1#comment-4396 ](http://mbed.org/forum/mbed/topic/906/?page=1#comment-4396)

[http://mbed.org/handbook/Timeout](http://mbed.org/handbook/Timeout)

```
/*----Déclaration du TICKER----*/
Ticker Live;
.
.
/*---- Prototypes de fonctions ----*/
void Live_isr():
.
.
/*----MAIN----/*
int main()
{
    Live.attach(Live_isr, 0.1); // 0.1s = period
}
.
.
/*---- Déclaration fonction exécution ISR----*/ 
void Live_isr()
{
    myled2 = !myled2;
    myled3 = !myled3;
}
```