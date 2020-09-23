# Share-Point-Recurrance-event-splitter
This is a DLL designed to split Sharepoint calendar recurrance events and to filter and fetch the details from current time to a specific time. We can specify the hours to which extend we need the data. Foe example, if we need some shift details of next 24 hours, you just have to specify 24 hours in the Hours parameter. It will provide you all the available resources start time , end time, Name and Email id for the mentioned hour.

Usage:

EventSplitter obj = new EventSplitter();
var x = obj.Execute(Site, ListName, Username, Password, Convert.ToInt32(Hour));
Out_dataTable = x.Item3;
Message = x.Item1;
Success = x.Item2;

Here 

Site = Share point site URL
List Name = Share point List Name
Username = Username to access the site
Password = Password to access the site
Hours = Time to which you have to fetch details
        eg: 9. If we mention 9 in hours, the DLL will fetch details of all resources, which is available in calendar from current time to next 9 hours.

Output:

Status : Flag value which states the current status of run
Message: Text value which provides exception details if any occurs
Out_dataTable : Result data set.
