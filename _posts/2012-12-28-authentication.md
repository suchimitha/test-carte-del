---
path: '/login'
title: 'Request'

layout: nil
---

# Request

## Actions
It’s a string, used to define the type of action that needs to be performed. We are providing below types of actions.

* createContact: Creates a Xero Contact.
* updateContact: Updates a Xero Contact.
* fetchContact: Fetches a single Xero Contact or a list of Xero Contacts from Xero.
* createInvoice Creates an Invoice in Xero.
* updateInvoice: Updates in Invoice in Xero.
* fetchInvoice: Fetches either a single Invoice or list of Invoices from Xero.
* createBill: Creates a Bill in Xero.
* updateBill: Updates a Bill in Xero.
* fetchBill: Fetches either a single Bill or list of Bills from Xero.
* createPurchaseOrder: Creates a Purchase Order (PO) in Xero.
* updatePurchaseOrder: Updates a Purchase Order (PO) in Xero.
* fetchPurchaseOrder: Fetches either a single Purhcase Order or list of Purchase Orders from Xero.

## RequestObject - Class
You have to create an Instance for RequestObject and pass to the “BreadwinnerAPI.call()” method as one of the parameters.
RequestObject req = new RequestObject();

It consists of the following variables:

1. xeroCustomer<br/>
It is an instance of the AccountWrapper (Xero Contact Wrapper) class. To Create/Insert customer we should pass desired values to variables. For all xeroCustomer variables you can refer here

```Ex: bw_xero_api01.BreadwinnerAPI.AccountWrapper xContact = new bw_xero_api01.BreadwinnerAPI.AccountWrapper();
    xContact.name = 'Test Customer'; 
    req.xeroCustomer = xContactc;```

2. xeroInvoice<br/>
It is an instance of the Invoice wrapper class. To Create/Insert customer we should pass desired values to variables. For all Invoice variables you can refer here

```Ex: bw_xero_api01.BreadwinnerAPI.Invoice inv = new bw_xero_api01.BreadwinnerAPI.Invoice();
    inv.CustomerId = 'Test Customer'; 
    inv.description = 'desc';… 
    req.xeroInvoice = inv;```

3. options<br/>
It is a collection of type Map (Map<String, Object>), used to pass any type of config settings that we enable. below options used for fetching records.

* Contacts : ContactId, ContactNumber, where, PageNumber, ModifiedAfter
* Invoices, Bills : InvoiceNumber, InvoiceId, where, PageNumber, ModifiedAfter
* PurchaseOrders : PurchaseOrderNumber, PurchaseOrderID, where, PageNumber, ModifiedAfter<br/>
Ex: req.options.put(‘PageNumber’,’1’);