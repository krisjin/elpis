# Elpis




## Flink

1. 统计最近24小时，用户登录的设备号






## Thread


#### 1. wait和sleep的区别

wait方法是所有object类中的方法，是线程同步的实现方式，虽然两者都可以让程序阻塞指定的毫秒数，并且都可以通过interrupt()方法中断,还是有区别的。

wait()方法必须在synchronized同步块或方法中使用。
wait()方法会释放由synchronized锁上的对象锁，而sleep()则不会
由wait()方法造成的阻塞，可以通过针对同一对象锁的synchronized作用域调用notify()/notifyAll()来唤醒，sleep()则无法被唤醒，只能定时唤醒或被interrupt()方法中断。

#### 2. sleep和yield的区别
