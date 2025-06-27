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
        
    - Filter | cordition | sql = where
      - df[['column'] cordition] ex. df[df["saraly"] > 100]]
        
    - select columns | sql = select form table
      - df[['column1'], ['column2']]
        
    - short | sql = orderby select ... form table order by ... desc
      - df.sort_values(by='column', ascending=False)
        
    - group by | sql = select ... from table group by ...
      - df.groupby('...').size() or .agg()
        
    - count rows | sql = select count(...) form table
      - len(df) or df.shape[0]
     
    - ค่าเฉลี่ย mean avg | sql = select avg(...) from table
      - df['...'].mean()

    - sum | sql = select sum(...) from table
      - df['...'].sum()

    - remove | duplicates | distinct | sql = select distinct ... form table
      - df.drop_duplicates()  

    - join tables | sql = select * from a join b a.id = b.id
      - pd.merge(df1, df2, on='id')
     
    - create new column | sql = select salary, salary*10 as bonus from table
      - df['bonus'] = df['saraly']*10

    - rename column | sql = select column as new_colum from table
      - df.rename(colums={'old': 'new'}, inplace=True)
     
    - isnull | sql = depends on DB: use IS NULL, COALESCE()
      - df.fillna('') or df.droupna()

    - export | sql = usetools or insert into outfiles
      - df.to_csv('output.csv', index=False)
      - df.to_excel('output.xlsx', index=False)
      - df.to_json('output.json')
      - df.to_sql('table_name', con, if_exists='replace', index=False) (requires a database connection con)
      - extenion
          - index=False: This parameter prevents Pandas from writing the DataFrame index as a separate column in the CSV file. If omitted or set to             True, the index will be included.
          - sep: Specifies the delimiter to use (default is comma ,). For example, sep='\t' for tab-separated values.
          - header: A boolean (default True) to include or exclude the header row, or a list of strings to specify custom header names.
          - encoding: Specifies the character encoding (e.g., utf-8).
          - mode: Specifies the file mode ('w' for write, 'a' for append). Def
          - ault is 'w', which overwrites the file if it exists.
    - plot | sql power bi other
      - df.plot(kind ='bar'), include seaborn, matplotlib 

# analytics
    - 

# idea
  - ทำภาพให้ machine เรียน แล้ว บอกว่า ภาพนี้คืออะไร แล้วค่อยไปจับกับคำค้นหา แล้วค่อย ตอบแบบกว้าง เหมือน ค้นหาจากคำ
    - เช่น ภาพพัดลม ai อ่านว่าและ บอกว่าได้ว่า คือ พัดลม ใช้ คีย์เวิร์ด พัดลม ไปค้นหา จาก text
   
    - 

# tip
  - 1.23e3 คือ 1.23 X 10 ยกกำลัง 3
  - ดูโครงสร้าง ตาราง โดยไม่รู้ว่ามีอะไรบ้าง select * from sqlite_master Wherer type ='table'- 
      import sqlite3
      conn = sqlite3.connect("exercise.db")
      cursor = conn.cursor()
      cursor.execute("select name from sqlite_master where type = 'table';")
      tables = cursor.fetchall()
      print("table")
      for table in tables:
        print(table[0])
