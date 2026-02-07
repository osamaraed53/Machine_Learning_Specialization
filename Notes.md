# General Rule: How To Detect If Something Is Sensitive To Outliers

### Rule 1 - Squaring or Power > 1 $\rArr$ VERY Sensitive to Outliers

If the formula contains:

$(X - center)^{2}$ or $(X - center)^{3}$,$(X - center)^{4}$ 

Outliers will have huge effect **Why?** Because powers grow very fast.

### Rule 2 - Absolute value $\rArr$ Medium Sensitivity 
If the formela uses : 

|X - Center|

Outliers affect it, but not too much **Why?** No explosion like squaring.

### Rule 3 - Median or Ranking $\rArr$ Very Resistant to Outliers

if method depends on
- Median 
- Percentiles 
- Ordering values insted of averaging
  
Outliers almost dont't affect it 