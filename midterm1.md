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

### Q2.3
1 Point

What would be printed when the main method is executed?
~~~
class Q3 {
  A a1 = new A();
  boolean val1 = a1.m();

  Iface i1 = new B();
  int val2 = i1.n();

  Iface i2 = a1;
  int val3 = i2.n();

  public static void main(String[] args){
    Q3 q = new Q3();
    System.out.println(q.val1 + ", " + q.val2 + ", " + q.val3);
  }
}
~~~
- [ ] false, 2, 12

- [ ] false, 12, 2

- [ ] false, 12, 12

- [ ] true, 2, 2

- [ ] true, 2, 12

- [ ] true, 12, 2

## Q3 Tracing
2 Points

For Questions 3.1 and 3.2 reference the following code:
~~~
class Song {
  String title;
  String artist;
  int year;

  public Song(String title, String artist, int year) {
    this.title = title;
    this.artist = artist;
    this.year = year;
  }
}

class Playlist {
  String title;
  Song[] songs;
  int numSongs;

  public Playlist(int length, String title) {
    this.title = title;
    this.songs = new Song[length];
    this.numSongs = 0;
    for (int i = 0; i < songs.length; i++) {
      this.songs[i] = new Song("", "", 0);
    }
  }

  public Playlist(String title, int length) {
    this.title = title;
    this.songs = new Song[length];
    this.numSongs = 0;
  }

  public boolean setSong(int index, Song song) {
    if (index >= this.songs.length || index < 0) return false;
    this.songs[index] = song;
    return true;
  }

  // returns false if playlist already full, else true
  public boolean addSong(Song newSong) {
    if (this.songs.length == this.numSongs) return false;
    this.songs[this.numSongs] = newSong;
    this.numSongs++;
    return true;
  }
}
~~~

### Q3.1
1 Point

How many total Song and Playlist objects are created?
~~~
Playlist playlist1 = new Playlist("90s Pop", 3);
Song song1 = new Song("Say My Name", "Destiny's Child", 1999);
Song song2 = new Song("I Want It That Way", "Backstreet Boys", 1999);
playlist1.addSong(song1);
playlist1.addSong(song2);
~~~

- [ ] 3

- [ ] 4

- [ ] 5

- [ ] 6

- [ ] 7

## Q3.21 Point

How many total Song and Playlist objects are created?
~~~
Playlist playlist2 = new Playlist(4, "More 90s Pop");
Song song3 = new Song("Wannabe", "Spice Girls", 1996);
Song song4 = new Song("...Baby One More Time", "Britney Spears", 1998);
playlist2.setSong(2, song3);
playlist2.setSong(0, song4);
~~~
- [ ] 3

- [ ] 4

- [ ] 5

- [ ] 6

- [ ] 7

- [ ] 8

