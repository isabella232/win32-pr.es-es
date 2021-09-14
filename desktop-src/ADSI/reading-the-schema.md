---
title: Leer el esquema
description: La mayoría de los proveedores admiten el esquema que se incluye Active Directory.
ms.assetid: cc35789e-5cfe-49e9-9fb3-489b949768c5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091d225c1be90d887f6994eda782ad7a7adb65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174577"
---
# <a name="reading-the-schema"></a>Leer el esquema

La mayoría de los proveedores admiten el esquema que se incluye Active Directory. El esquema contiene definiciones de clase y atributo. ADSI abstrae el esquema en "Provider://schema". Cada objeto lleva la ubicación del esquema en la que se define su clase. Puede usar el método [**de propiedad IADs::get \_ Class**](iads-property-methods.md) para obtener esta información.

Para enlazar al contenedor de esquemas en un dominio determinado, haga lo siguiente:


```VB
Dim SchemaContainer As Object
Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
```


```C++

hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, IID_IADsContainer, (void**) &pSchema );
```





Para mostrar información en el contenedor de esquemas, enlace al contenedor y enumere cada objeto del contenedor como se muestra a continuación:


```VB
Dim prop As Object
Dim obj As Object
Dim SchemaContainer As Object
Dim Class As Object

Set SchemaContainer = GetObject("LDAP://Fabrikam/Schema")
'Show all items in the schema container
For Each obj In SchemaContainer
     Debug.Print obj.Name & " (" & obj.Class & ")"
Next

'Show the optional attributes
For Each prop In Class.OptionalProperties
   Debug.Print prop
Next
```


```C++

IADsContainer *pSchema=NULL;
 HRESULT hr;

 CoInitialize(NULL);

 hr = ADsGetObject(L&quot;LDAP://Fabrikam/Schema&quot;, 
                   IID_IADsContainer, (void**) &pSchema );

 if ( !SUCCEEDED(hr) )
 {
   return hr;
 }

 // Enumerate schema objects
 IEnumVARIANT *pEnum = NULL;
 hr = ADsBuildEnumerator( pSchema, &pEnum );
 pSchema->Release(); // This is no longer needed, since we have the enumerator already.
    
 if ( SUCCEEDED(hr) )
 {
   VARIANT var;
   ULONG lFetch;
   IADs *pChild=NULL;
   VariantInit(&var);
        
   while( SUCCEEDED(ADsEnumerateNext( pEnum, 1, &var, &lFetch )) && lFetch == 1 )
   {
     hr = V_DISPATCH(&var)->QueryInterface( IID_IADs, (void**) &pChild );
     if ( SUCCEEDED(hr) )
     {
       BSTR bstrName;
       BSTR bstrClass;
       // Get more information on the child classes
       pChild->get_Name(&bstrName);
       pChild->get_Class(&bstrClass);
                
       printf(&quot;%S\t\t(%S)\n&quot;, bstrName, bstrClass );
                
       // Clean-up
       SysFreeString(bstrName);
       SysFreeString(bstrClass);
                
       pChild->Release();
     }
     VariantClear(&var);
   }
 }

 CoUninitialize();
```





También puede enlazar a un objeto y obtener la ubicación del esquema, como se muestra a continuación:


```VB
Dim prop As Object
Dim dom As Object
Dim Class As Object

Set dom = GetObject("LDAP://Fabrikam")
Debug.Print dom.Schema
Set Class = GetObject(dom.Schema)
'Mandatory attributes
For Each prop In Class.MandatoryProperties
    Debug.Print prop
Next
```



 

 




