## LIMIT OF SEQUENCE
  การหาลิมิตของลำดับว่าเป็น ลู่เข้า หรือลู่ออก

- ถ้าลู่เข้า เข้าสู่เลขอะไร
- ถ้าลู่ออก infinity

## MONOTONE SEQUENCE

Increasing

```
a1< a2 < a3 ... < an <...
```
Decreasing
```
a1 > a2 > a3 ... > an >...


```

มี 3 วิธีในการหาว่า มันเพิ่มหรือลด

1. DIFFERENCE
2. Ratio
3. DERIVATIVE

## SERIES
ผลบวกของลำดับ
  - ลู่เข้าเมื่อ S != INF
  - ที่เหลือ ลู่ออก

เชคว่ามันเป็น infinity หรือปร่าว ก็มีวิธีดังนี้
1. GEINETRIC
2. HARMONIC
3. P-SERIES

## TEST FOR CONVERGEN OF SERIES WITH POSITIVE TERMS
การทดสอบ ลู่เข้า สำหรับอนุกรม ที่มีค่าบวก

### 1.INTERGAL TEST  ใช้กับพวกเลขยกกำลัง
  - ถ้า an ลดลง
  - ถ้า Integral แล้ว หาค่าได้
  - สรุปได้ว่า ลู่เข้า

เพิ่มเติม ไปดูเรื่อง Integral By Pass

### 2.Comparison Test genaral team ระบุได้ว่าแบบไหน
  - ถ้า an <= bn && bn ลู่เข้า then an ลู่เข้าด้วย
  - ถ้า an >= bn && bn ลู่ออก then an ลู่ออกด้วย

เพิ่มเติม มันเร็วที่เงื่อนไขเยอะ เราต้องรู้จัก Geo,P,HARMONIC

### 3. RATIO Test ติดเฟค เศษส่วน
lim n->oo |an+1/an| = L
 - L < 1 CONVERGEN
 - L > 1 DIVERGEN
 - L = 1 test fail

## Altenating SERIES
ใช้ในกรณี อยู่ในรูป
an = (-1)^n
```
a1 - a2 + a3 - a4 + a5 -... - (-1)^n an +....
```
### Altenating Test
  - CHEAK Decreasing
  - LIM N->OO an = 0

### Absolute and Conditional ConV.

an เป็น Altenating แบบ ++ -- ไม่ใช้สลับ +-+-

```
|an| แล้ว CONVERGEN all team  then so abs CONVERGEN
```

```
an CONVERGEN but |an| DIVERGEN then so abs DIVERGEN
```

## FLOW

```javascript


const Check_MonotoneSeq = (an) => (
  switch (picktest) {

    case DIFFERENCE:

    result = an+1 - an

      if(result > 0)
        return Increasing
      else if(result < 0)
        return Decreasing
    break;

    case RATIO:

    result = an+1/an

    if(result > 1)
        return Increasing
    else if (result <1)
        return Decreasing
    break;

    case DERIVATIVE:

    f (x)diff = an
    result = f(x)

    if(result > 0)
      return Increasing
    else if(result < Decreasing)
      return Decreasing

    break;
    default:
  }

)
const TestGenaral_Term = (picktest) => (
  switch (picktest) {

    case INTERGRAL:
      if(Check_MonotoneSeq(an) == Decreasing){
        if (Integrade f(x) == หาค่าเป็ฯตัวเลขได้)
          CONVERGEN
        else
          DIVERGEN
      }
    break;

    case COMPARISON:
    if(YouCanFindBn == true){
      if( an <= bn && bn == ConV && an == ConV)
        CONVERGEN
      if( an => bn && bn == Div && an == Div)
        DIVERGEN
    }
    break;

    case RATIO:
    let L = lim|an+1/an|
    if(L < 1)
      CONVERGEN
    else if(L > 1)
      DIVERGEN
    else
      FAIL
    break;

    default:

  }
)
 if (|an| == CONVERGEN)
    an abs CONVERGEN
 else if (|an| == DIVERGEN){

    let pick = input();

    if (TestGenaral_Term (pick) == CONVERGEN)
      CONDITIONAL CONVERGEN
    else if (TestGenaral_Term (pick) == DIVERGEN)
      DIVERGEN
}
```
