## Q1 Events
1 Point

The Github repo for Pre-Lecture 2 is at https://github.com/ucsd-cse12-f23/ucsd-cse12-f23.github.io/tree/main/_pre-lectures/lecture-02

Using Pre-Lecture 2's Event code, the following Events are created. From the code below, select a pair of events where one occurs completely within the duration of the other:
~~~
LocalDateTime time1 = LocalDateTime.of(2020, 9, 27, 8, 0);
LocalDateTime time2 = LocalDateTime.of(2020, 9, 27, 9, 30);
LocalDateTime time3 = LocalDateTime.of(2020, 9, 27, 10, 0);
LocalDateTime time4 = LocalDateTime.of(2020, 9, 27, 8, 30);
LocalDateTime time5 = LocalDateTime.of(2020, 9, 27, 9, 0);
LocalDateTime time6 = LocalDateTime.of(2020, 9, 27, 7, 0);
LocalDateTime time7 = LocalDateTime.of(2020, 9, 27, 7, 30);
Event event1 = new Event(time6, time5, "WLH2005");
Event event2 = new Event(time4, time3, "YORK2622");
Event event3 = new Event(time1, time2, "PCYNH109");
Event event4 = new Event(time7, time4, "EBU3B3206");
~~~
- [ ] event1

- [ ] event2

- [ ] event3

- [ ] event4

## Q2 Interfaces
3 Points

For Sub questions 2.1-2.3 reference the following code:
~~~
interface Iface {
  public boolean m();
  public int n();
}

class A implements Iface {
  public String s;
  public String x;

  public boolean m() {
    return true;
  }

  public int n() {
    return 12;
  }
}

class B implements Iface {
  public String s;
  public String y;

  public boolean m() {
    return false;
  }

  public int n() {
    return 2;
  }
}
~~~
### Q2.1 Interfaces
1 Point

Select all of the declarations below that would NOT cause a compile error:
- [ ] Iface i1 = new A();
- [ ] Choice 2 of 5:B b = new Iface();
- [ ] Choice 3 of 5:A a1 = new B();
- [ ] Choice 4 of 5:Iface i2 = new Iface();
- [ ] Choice 5 of 5:A a2 = new A();

### Q2.2 
1 Point

Select all of the declarations below that would NOT cause a compile error:

- [ ] Iface i1 = new A(); String val1 = i1.s;
- [ ] Iface i2 = new B(); String val2 = i2.x;
- [ ] A a1 = new A(); String val3 = a1.s;
- [ ] A a2 = new A(); String val4 = a2.y;
