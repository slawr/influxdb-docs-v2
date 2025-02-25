---
title: math.atan2() function
description: >
  The math.atan2() function returns the arc tangent of `y`/`x`, using the signs of
  the parameters to determine the quadrant of the return value.
aliases:
  - /influxdb/v2.0/reference/flux/functions/math/atan2/
  - /influxdb/v2.0/reference/flux/stdlib/math/atan2/
  - /influxdb/cloud/reference/flux/stdlib/math/atan2/
menu:
  flux_0_x_ref:
    name: math.atan2
    parent: math
weight: 301
introduced: 0.22.0
---

The `math.atan2()` function returns the arc tangent of `y`/`x`, using the signs
of the two to determine the quadrant of the return value.

_**Output data type:** Float_

```js
import "math"

math.atan2(y: 1.22, x: 3.14)

// Returns 0.3705838802763881
```

## Parameters

### y {data-type="float"}
The y coordinate used in the operation.

### x {data-type="float"}
The x coordinate used in the operation.

## Special cases
```js
math.atan2(y:y, x:NaN)        // Returns NaN
math.atan2(y: NaN, x:x)       // Returns NaN
math.atan2(y: +0, x: >=0)     // Returns +0
math.atan2(y: -0, x: >=0)     // Returns -0
math.atan2(y: +0, x: <=-0)    // Returns +Pi
math.atan2(y: -0, x: <=-0)    // Returns -Pi
math.atan2(y: >0, x: 0)       // Returns +Pi/2
math.atan2(y: <0, x: 0)       // Returns -Pi/2
math.atan2(y: +Inf, x: +Inf)  // Returns +Pi/4
math.atan2(y: -Inf, x: +Inf)  // Returns -Pi/4
math.atan2(y: +Inf, x: -Inf)  // Returns 3Pi/4
math.atan2(y: -Inf, x: -Inf)  // Returns -3Pi/4
math.atan2(y:y, x: +Inf)      // Returns 0
math.atan2(y: >0, x: -Inf)    // Returns +Pi
math.atan2(y: <0, x: -Inf)    // Returns -Pi
math.atan2(y: +Inf, x:x)      // Returns +Pi/2
math.atan2(y: -Inf, x:x)      // Returns -Pi/2
```
