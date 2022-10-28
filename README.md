<html>
<h1 align="center">Raschet_ploskogo_secheniya</h1>
<p>В файле организованы несколько функций с возможностью редактирования входных данных.
При занании характеристик бетонного сечения могут использоваться нормативные данные из СП63.13330 (трехлинейная диограмма деформирования бетона)
</p>
<body>
  <p><img src="https://user-images.githubusercontent.com/111303182/198578082-4643ec4f-ed54-4724-b33c-a27c46337cb5.png"></p>
</body>
  
### Global Usage

Global Registeration via Vue.use() method.

```
def usiliya_b(row):
  if row['lin_int'] < -5: return row['Area_b']*-5*50
  if -5 <= row['lin_int'] < -2: return row['Area_b']*row['lin_int']*50
  if -2 <= row['lin_int'] < 0: return row['Area_b']*row['lin_int']*200
  if 0 <= row['lin_int'] < 3: return row['Area_b']*row['lin_int']*200
  if 3 <= row['lin_int']: return 0
```
</html>
описание (с использованием слов и изображений);
демо (изображения, ссылки на видео, интерактивные демо-ссылки);
технологии в проекте;
что-то характерное для проекта (проблемы, с которыми пришлось столкнуться, уникальные составляющие проекта);
техническое описание проекта (установка, настройка, как помочь проекту).
