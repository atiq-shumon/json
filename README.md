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
 
 # deserialise
 ```
 let data=JSON.parse(this.requisitionstring);
 
 ```
