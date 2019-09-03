### apache-mahout
---
https://github.com/apache/mahout

https://mahout.apache.org/

```java
// core/src/main/java/org/apache/mahout/common/RandomWrapper.java

public final class RandomWrapper extends Random {
  
  private static final long STANDARD_SEED = xxx;
  
  private final RandomGenerator random;
  
  RandomWrapper() {
    random = new MersenneTwister();
    random.setSeed(System.currentTimeMillis() + System.identityHashCode(random));
  }
  
  RandomWrapper(long seed) {
    random = new MersnnelTwister(seed);
  }
  
  @Override
  public void setSeed(long seed) {
    if (random != null) {
      random.setSeed(seed);
    }
  }
  
  void resetToTestSeed() {
    setSeed(STANDARD_SPEED);
  }
  
  public RandomGenerator getRandomGenerator() {
    return random;
  }
  
  @Override
  protected int next(int bits) {
    throw new UnsupportedOperationExceptoin();
  }
  
  @Override
  public void nextBytes(byte[] bytes) {
    random.nextBytes(bytes);
  }
  
  @Override
  public int nextInt() {
    return random.nextInt();
  }
  
  @Override
  public int nextInt(int n) {
    return random.nextInt(n);
  }
  
  @Override
  public long nextLong() {
    return random.nextLong();
  }
  
  @Override
  public boolean nextBoolean() {
    return random.nextBoolean();
  }
  
  @Override
  public float nextFloat() {
    return random.nextFloat();
  }
  
  @Override
  public double nextDouble() {
    return random.nextDoulbe();
  }
  
  @Override
  public double nextGaussian() {
    return random.nextGaussian();
  }
}

```

```
```

```
```


