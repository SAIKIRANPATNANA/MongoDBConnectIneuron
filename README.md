## `mongo_operations`: MongoDB Operations Simplified

`mongo_operations` is a Python package designed to simplify common MongoDB operations. It provides an easy-to-use interface for interacting with MongoDB databases and collections. Whether you are inserting records, reading data, updating records, or performing bulk inserts, `mongo_operations` streamlines the process, making MongoDB operations straightforward.

### Installation

Install the package using pip:

```bash
pip install mayya-connect==0.0.1
```

### Usage

1. **Create an Instance of `mongo_operation`**

   ```python
   from mayya_database import mongo_crud

   # Provide your MongoDB client URL and database name
   mongo_op = mongo_crud.mongo_operation(client_url='your_mongo_client_url', database_name='your_database_name')
   ```
2. **Create a DataBase**

   ```python
   database = mongo_op.create_database()   
   ```

2. **Create a Collection**

   ```python
   # Provide the name for your MongoDB collection
   collection = mongo_op.create_collection(collection_name='your_collection_name')
   ```

3. **Insert Records**

   ```python
   # Insert a single record
   record = {'key': 'value'}
   mongo_op.insert_record(record=record, collection_name='your_collection_name')

   # Insert multiple records
   records = [{'key1': 'value1'}, {'key2': 'value2'}]
   mongo_op.insert_record(record=records, collection_name='your_collection_name')
   ```

4. **Read Records**

   ```python
   # Read all records from the collection
   mongo_op.read_record(collection_name='your_collection_name')
   ```

5. **Delete Records**

   ```python
   # Provide a query to match records to be deleted
   query = {'key': 'value'}
   mongo_op.delete_record(record=query, collection_name='your_collection_name')
   ```

6. **Update Records**

   ```python
   # Provide a query to match records to be updated and an update document
   query = {'key': 'value'}
   update = {'$set': {'new_key': 'new_value'}}
   mongo_op.update_record(query=query, update=update, collection_name='your_collection_name')
   ```

7. **Bulk Insert from Data File**

   ```python
   # Provide the path to your data file (CSV or Excel)
   data_file_path = 'path/to/your/datafile.csv'
   mongo_op.bulk_insert(datafile=data_file_path, collection_name='your_collection_name')
   ```

### Contributors

- SAIKIRANPATNANA

### License

This project is licensed under the MIT License - see the [LICENSE](link/to/LICENSE) file for details.

