# Reusable_Multi_Select_Lookup

Object-agnostic easily configurable multi-select lookup LWC 
* Configure on any lightning record page
* Ability to configure multiple search fields (not just Name) to bind to search query
* Ability to display other fields (like Email and Phone for example) in the search results
* Ability to specify where clause with dynamic id variables

Deploy to Salesforce: https://live.playg.app/play/reusable-multiselect-lookup

```html
<c-multi-select-lookup
        record-id={recordId}
        obj-api-name="Contact"
        field-paths="Id, Name, Email, Account.Owner.Name"
        field-paths-for-search="Name, Email"
        where-clause="AccountId = :recordId ORDER BY FirstName"
        icon-name="standard:contact"
        onselected={handleSelectedRecords}
        placeholder="Lookup record..."
      >
</c-multi-select-lookup>
```

![image](https://user-images.githubusercontent.com/124932501/227669992-258c5349-76c5-4fb5-b88d-3fc87a5618ce.png)

![image](https://user-images.githubusercontent.com/124932501/227670564-f31c0187-23ea-4363-8974-9e72f57c4751.png)

![image](https://user-images.githubusercontent.com/124932501/227670090-02603784-748c-43f2-a78b-9f74dded2ad9.png)
