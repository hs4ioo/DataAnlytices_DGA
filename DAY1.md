# Python
  - colab web IDE

# การตั้งชื่อตัวแปร
    - ต้องขึ้นต้นด้วย eng หรือ _ เท่านั้น
    - Case sensitive

# ประเภท 
  - ทูเพิล Tuples 
    - x = ("...","...","...")
  - list
    - x = [xxx, xxx, xxx]
  - set
    - x = {xxx, xxx, xxx, xxx}
    - union set
      - x = {1, 2, 3}
      - y = {4, 5, 6}
      - union_show = x.union(y) หรือ union_show = x | Y
  - dictionaries
    - x = {"name": "banl", "age": 45, } คล้าย Json

# operators
    - == เท่ากับ
    - !== ไม่เท่ากับ
    - < น้อยกว่า
    - > มากกว่า 
    - >= มากกว่าหรือเท่ากับ
    - <= น้อยกว่าหรือเท่ากับ

# install lib
  - in computer
    - pip install
    - pip uninstall
  - in google colab
    - !pip install
    - !pip uninstall
    

# Library
  - pandas สำหรับอ่านและสำรวจข้อมูลที่มีโครงสร้าง
  - numpy สำหัรบทำงานกับ array และ คำนวณเชิงตัวเลข
  - matplotlib / seaborn

# Function

# pandas
  - import pandas as pd
    - load data
      - df = pd.read_csv("")
      - df = pd.read_json("")
      - df = pd.read_excel("", sheet_name='')

# tip
  - 1.23e3 คือ 1.23 X 10 ยกกำลัง 3
  - ดูโครงสร้าง ตาราง โดยไม่รู้ว่ามีอะไรบ้าง select * from sqlite_master Wherer type ='table'
      import sqlite3
      conn = sqlite3.connect("exercise.db")
      cursor = conn.cursor()
      cursor.execute("select name from sqlite_master where type = 'table';")
      tables = cursor.fetchall()
      print("table")
      for table in tables:
        print(table[0])
