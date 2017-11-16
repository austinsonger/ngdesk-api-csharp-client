# IO.Swagger.Api.DefaultApi

All URIs are relative to *https://localhost/api/v2/operations*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetTicket**](DefaultApi.md#getticket) | **GET** /tickets/{ticket_id} | 
[**GetTickets**](DefaultApi.md#gettickets) | **GET** /tickets | 
[**PostMessages**](DefaultApi.md#postmessages) | **POST** /tickets/{ticket_id}/messages | 
[**PostTickets**](DefaultApi.md#posttickets) | **POST** /tickets | 
[**PutTickets**](DefaultApi.md#puttickets) | **PUT** /tickets | 


<a name="getticket"></a>
# **GetTicket**
> Ticket GetTicket (string ticketId, string authenticationToken = null, string category = null, string statuses = null, string orderedColumn = null, string orderedBy = null, string clientId = null, string clientSecret = null)



Retrievs a ticket

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetTicketExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var ticketId = ticketId_example;  // string | 
            var authenticationToken = authenticationToken_example;  // string |  (optional) 
            var category = category_example;  // string |  (optional) 
            var statuses = statuses_example;  // string |  (optional) 
            var orderedColumn = orderedColumn_example;  // string |  (optional) 
            var orderedBy = orderedBy_example;  // string |  (optional) 
            var clientId = clientId_example;  // string |  (optional) 
            var clientSecret = clientSecret_example;  // string |  (optional) 

            try
            {
                Ticket result = apiInstance.GetTicket(ticketId, authenticationToken, category, statuses, orderedColumn, orderedBy, clientId, clientSecret);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.GetTicket: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticketId** | **string**|  | 
 **authenticationToken** | **string**|  | [optional] 
 **category** | **string**|  | [optional] 
 **statuses** | **string**|  | [optional] 
 **orderedColumn** | **string**|  | [optional] 
 **orderedBy** | **string**|  | [optional] 
 **clientId** | **string**|  | [optional] 
 **clientSecret** | **string**|  | [optional] 

### Return type

[**Ticket**](Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="gettickets"></a>
# **GetTickets**
> List<Ticket> GetTickets (decimal? authenticationToken = null, int? start = null, int? length = null, int? draw = null, string q = null, string sortBy = null, string sortByOrder = null, string passedAccountId = null, string passedUserId = null, int? viewId = null, string clientId = null, string clientSecret = null)



Retrieve tickets

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetTicketsExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var authenticationToken = 3.4;  // decimal? | User athentication uuid (optional) 
            var start = 56;  // int? | Start query value (optional) 
            var length = 56;  // int? | Number of rows query (optional) 
            var draw = 56;  // int? | Number of times table has been reloaded (optional) 
            var q = q_example;  // string | Values provided in q are tokenized and search on columns: TICKET_ID,SUBJECT,REQUESTOR_UERNAME, REQUESTOR_EMAIL, TICKET_MESSAGES (optional) 
            var sortBy = sortBy_example;  // string | Column name to order table by (optional) 
            var sortByOrder = sortByOrder_example;  // string | Sort by ascending or descending (optional) 
            var passedAccountId = passedAccountId_example;  // string |  (optional) 
            var passedUserId = passedUserId_example;  // string |  (optional) 
            var viewId = 56;  // int? | View Id (optional) 
            var clientId = clientId_example;  // string | API ID (optional) 
            var clientSecret = clientSecret_example;  // string | API Secret (optional) 

            try
            {
                List&lt;Ticket&gt; result = apiInstance.GetTickets(authenticationToken, start, length, draw, q, sortBy, sortByOrder, passedAccountId, passedUserId, viewId, clientId, clientSecret);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.GetTickets: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authenticationToken** | **decimal?**| User athentication uuid | [optional] 
 **start** | **int?**| Start query value | [optional] 
 **length** | **int?**| Number of rows query | [optional] 
 **draw** | **int?**| Number of times table has been reloaded | [optional] 
 **q** | **string**| Values provided in q are tokenized and search on columns: TICKET_ID,SUBJECT,REQUESTOR_UERNAME, REQUESTOR_EMAIL, TICKET_MESSAGES | [optional] 
 **sortBy** | **string**| Column name to order table by | [optional] 
 **sortByOrder** | **string**| Sort by ascending or descending | [optional] 
 **passedAccountId** | **string**|  | [optional] 
 **passedUserId** | **string**|  | [optional] 
 **viewId** | **int?**| View Id | [optional] 
 **clientId** | **string**| API ID | [optional] 
 **clientSecret** | **string**| API Secret | [optional] 

### Return type

[**List<Ticket>**](Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="postmessages"></a>
# **PostMessages**
> void PostMessages (Ticket body, string ticketId, string authenticationToken = null, string clientId = null, string clientSecret = null)



Insert a messages

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PostMessagesExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new Ticket(); // Ticket | The request body for the operation
            var ticketId = ticketId_example;  // string | 
            var authenticationToken = authenticationToken_example;  // string | User athentication (optional) 
            var clientId = clientId_example;  // string | api client (optional) 
            var clientSecret = clientSecret_example;  // string | api secret (optional) 

            try
            {
                apiInstance.PostMessages(body, ticketId, authenticationToken, clientId, clientSecret);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.PostMessages: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Ticket**](Ticket.md)| The request body for the operation | 
 **ticketId** | **string**|  | 
 **authenticationToken** | **string**| User athentication | [optional] 
 **clientId** | **string**| api client | [optional] 
 **clientSecret** | **string**| api secret | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="posttickets"></a>
# **PostTickets**
> Ticket PostTickets (List<TicketMessage> body, decimal? authenticationToken = null, string clientId = null, string clientSecret = null)



Insert a tickets

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PostTicketsExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new List<TicketMessage>(); // List<TicketMessage> | The request body for the operation
            var authenticationToken = 3.4;  // decimal? | User athentication uuid (optional) 
            var clientId = clientId_example;  // string |  (optional) 
            var clientSecret = clientSecret_example;  // string |  (optional) 

            try
            {
                Ticket result = apiInstance.PostTickets(body, authenticationToken, clientId, clientSecret);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.PostTickets: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**List&lt;TicketMessage&gt;**](TicketMessage.md)| The request body for the operation | 
 **authenticationToken** | **decimal?**| User athentication uuid | [optional] 
 **clientId** | **string**|  | [optional] 
 **clientSecret** | **string**|  | [optional] 

### Return type

[**Ticket**](Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="puttickets"></a>
# **PutTickets**
> List<Ticket> PutTickets (List<Ticket> body, bool? authenticationToken = null, string clientId = null, string clientSecret = null)



Update tickets

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PutTicketsExample
    {
        public void main()
        {
            var apiInstance = new DefaultApi();
            var body = new List<Ticket>(); // List<Ticket> | The request body for the operation
            var authenticationToken = true;  // bool? | User athentication uuid (optional) 
            var clientId = clientId_example;  // string |  (optional) 
            var clientSecret = clientSecret_example;  // string |  (optional) 

            try
            {
                List&lt;Ticket&gt; result = apiInstance.PutTickets(body, authenticationToken, clientId, clientSecret);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.PutTickets: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**List&lt;Ticket&gt;**](Ticket.md)| The request body for the operation | 
 **authenticationToken** | **bool?**| User athentication uuid | [optional] 
 **clientId** | **string**|  | [optional] 
 **clientSecret** | **string**|  | [optional] 

### Return type

[**List<Ticket>**](Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

