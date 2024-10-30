# SQL useful tips

### 1) To filter a SQL query containing japanese charaters such as 「学」via LIKE

Add 'N' before the string as follows : 

```sql 

# Given that the column containing japanese characters must be a NVARCHAR 
SELECT TOP (1000) [Id]
      ,[Title]
      ,[Content]
      ,[Topic]
      ,[JLPTLevel]
      ,[KanjiCountN1]
      ,[KanjiCountN2]
      ,[KanjiCountN3]
      ,[KanjiCountN4]
      ,[KanjiCountN5]
      ,[EntryDate]
      ,[LastModification]
  FROM [JLPT].[dbo].[JLPTTexts]
  
  WHERE Title LIKE N'%学%';
```