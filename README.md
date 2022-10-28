<html>
<h1 align="center">Raschet_ploskogo_secheniya</h1>
  
### The basic idea of the calculation

When specifying the characteristics of the concrete section can be used normative data from SP63.13330 (three-line diagram of deformation of concrete)
When specifying the characteristics of steel sections, the idea of linear dependence of strains and stresses in the material is used.
Taking the maximum deformations in the compressed zone of the concrete as a result of the work, the deformations in the tensile zone return and the calculation error is determined.
As a result of the program's work the graph of stress distribution over the section height is plotted.
<body>
  <p><img src="https://user-images.githubusercontent.com/111303182/198578082-4643ec4f-ed54-4724-b33c-a27c46337cb5.png"></p>
</body>
  
### Functions used

Functions are used to set the work of the concrete part of the section.

```python
def usiliya_b(row):
  if row['lin_int'] < -5: return row['Area_b']*-5*50
  if -5 <= row['lin_int'] < -2: return row['Area_b']*row['lin_int']*50
  if -2 <= row['lin_int'] < 0: return row['Area_b']*row['lin_int']*200
  if 0 <= row['lin_int'] < 3: return row['Area_b']*row['lin_int']*200
  if 3 <= row['lin_int']: return 0
```
</html>
