# Dither
An implementation of t-way test case generation with IPOG (In-Parameter-Order-General).

# Usage

```java
import com.github.jesg.dither.Dither;

// 2-way IPOG
Object[][] results2 = Dither.ipog(new Object[][] {
		new Object[] { 0, 1 },
        new Object[] { 0, 1 },
        new Object[] { true, false },
        new Object[] { "cat", "dog", "bird" }});

// 3-way IPOG
Object[][] results3 = Dither.ipog(3, new Object[][] {
		new Object[] { 0, 1 },
        new Object[] { 0, 1 },
        new Object[] { true, false },
        new Object[] { "cat", "dog", "bird" }});

// 3-way IPOG with constraints
Object[][] results3constraints = Dither.ipog(3, new Object[][] {
		new Object[] { 0, 1 },
        new Object[] { 0, 1 },
        new Object[] { true, false },
        new Object[] { "cat", "dog", "bird" }},
        new Integer[][]{  // constraints
			new Integer[]{null, null, 0, 1}}); // exclude true cat combination
```

# Note on Patches/Pull Requests

* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a
  future version unintentionally.
* Commit, do not mess with rakefile, version, or history.
  (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
* Send me a pull request. Bonus points for topic branches

# Copyright

Apache License, Version 2.0
Copyright (c) 2015 Jason Gowan See LICENSE for details.
