# XML-To-JSON
parse your xml generated by databinding to a json object
## Tips


To Serialization Work, you need to create a *Variable* for an *Interface* generated by a DataBinding class 


**(because in the body of this XMLNode have the especifications of Collections (wich will be parsed to a list to the json object)),**


if you don't create a *Variable Interface* from a databinding, unfortunately, lists in your XML don't work in the final JSON object.

## Usage
```Delphi
    var
      iVariable : IDataBindingXMLObject;
      sJSON : string;
    begin
        iVariable : NewDataBindingXMLObject;
        // do something in your XML Object 
        sJSON := xml_to_json(iVariable);
    end;
    

//Thanks to use, now parse or use your Json Object generated by XML! yay!
```
**Limitations**

Troubles with:

special chars, generic XMLDocuments (ausence of the Collections element specifications, needed for Delphi recognize lists presents on the XML).


Enjoy!
