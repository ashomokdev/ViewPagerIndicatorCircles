# ViewPagerIndicatorCircles
ViewPagerIndicator widget for Android that are compatible with the ViewPager from the Android Support Library.
<a href="http://i.imgur.com/MSaNKsJ.png">
  <img src="http://imgur.com/MSaNKsJl.png" />
</a>
<a href="http://i.imgur.com/5aVwLpV.png">
  <img src="http://imgur.com/5aVwLpVl.png" />
</a>

<br>

Usage
----------------------

*For a working implementation of this project see the `sample/` folder.*

  1. Include the widget in your view. This should usually be placed
     adjacent to the `ViewPager` it represents.
```xml
    <android.support.v4.view.ViewPager
        android:id="@+id/pager"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
    </android.support.v4.view.ViewPager>

    <com.viewpagerindicator.library.CircleView
        android:id="@+id/circle_view"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"
        android:layout_centerVertical="true"
        />
```
  2. In your `onCreate` method (or `onCreateView` for a fragment), bind the
     indicator to the `ViewPager`.
```java
         //Set the pager with an adapter
        ViewPager pager = (ViewPager) findViewById(R.id.pager);
        PagerAdapter pagerAdapter = new MyFragmentPagerAdapter(getSupportFragmentManager());
        pager.setAdapter(pagerAdapter);

         //Bind the viewpagerindicator to the adapter
        CircleView circleView = (CircleView) findViewById(R.id.circle_view);
        circleView.setColorAccent(getResources().getColor(R.color.colorAccent)); //Optional
        circleView.setColorBase(getResources().getColor(R.color.colorPrimary)); //Optional
        circleView.setViewPager(pager);
```
Including In Your Project
-------------------------
 * Maven 
 ```xml
<dependency>
    <groupId>com.github.bieliaievays</groupId>
    <artifactId>viewpagerindicator</artifactId>
    <version>1.0</version>
</dependency>

 ```   
 * Gradle
 ```xml
   compile group: 'com.github.bieliaievays', name: 'viewpagerindicator', version: '1.0'
```

This project depends on the `ViewPager` class which is available in the Android Support Library.


Developed By
----------------------
Iuliia Ashomok - <ashomokdev@gmail.com>

License
-------------

    Copyright 2016 Iuliia Ashomok

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0
