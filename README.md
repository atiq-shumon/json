### JSON fake data api

https://dummyjson.com/

https://jsonplaceholderapi

https://jsonplaceholder.typicode.com/


**JSON file does not purse if it has comments inside**
-------------------------------------------------------

**JSON file does not purse twice.**
-----------------------------------------------

# json Object serialise and deseriliase in c#

https://stackoverflow.com/questions/1056121/how-to-create-json-string-in-c-sharp

# uses example

```
BulkRequisitionBillApproval billmaster = new SDBulkRequisitionBillBLL().GetBulkBill_Masterdetails(new ParamsModel() {ActionControlMode= "get_by_bill_id",Param1=model.Param1,Param2="x",Param3="x" });
            List<DOBreakDown> billdetails = billmaster.dobreakdowndetailslist;
``` 

# serialise
```
 fields.Add(new BulkDORequisitionFieldJson("bulkdorequisionId", "DO Requisition", JsonConvert.SerializeObject(billmaster), "f fill-remaining-space", new Validation("false"), "", "false"));
 
 ````
 
 # deserialise and parse in js/angular
 ```
 let data=JSON.parse(this.requisitionstring);
 
 ```
 
 ### Another example
 ```C#
 //Create my object
        var my_jsondata = new
        {
            Host = @"sftp.myhost.gr",
            UserName = "my_username",
            Password = "my_password",
            SourceDir = "/export/zip/mypath/",
            FileName = "my_file.zip"
        };

        //Tranform it to Json object
        string json_data = JsonConvert.SerializeObject(my_jsondata);

        //Print the Json object
        Console.WriteLine(json_data);

        //Parse the json object
        JObject json_object = JObject.Parse(json_data);

        //Print the parsed Json object
        Console.WriteLine((string)json_object["Host"]);
        Console.WriteLine((string)json_object["UserName"]);
        Console.WriteLine((string)json_object["Password"]);
        Console.WriteLine((string)json_object["SourceDir"]);
        Console.WriteLine((string)json_object["FileName"]);
     ```   
