---
title: Método Put
description: Guarda el valor de una propiedad para un objeto Active Directory por nombre en la caché de propiedades.
ms.assetid: 8534ceba-5fcb-441f-9e76-3060319478af
ms.tgt_platform: multiple
keywords:
- Put ADSI ,about
- ADSI ADSI, código de ejemplo Visual Basic , mediante el método Put
- ADSI de propiedades, guardar un valor para una propiedad en la caché de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8be79892c62d788f711163ec1fad7c555f6e6f0a897f805341a588a4b6d3619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023213"
---
# <a name="the-put-method"></a>Método Put

El [**método IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) guarda el valor de una propiedad para un objeto Active Directory por nombre en la caché de propiedades. Use [**IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) para guardar propiedades multivalor en la caché de propiedades o para quitar una propiedad de un objeto . Estos valores no se conservan en el servicio de directorio subyacente hasta que se llama a [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)


```VB
Dim Namespace As IADsOpenDSObject
Dim User As IADsUser
Dim NewName As Variant
Dim sUserName As String
Dim sPassword As String

On Error GoTo CleanUp
 
Set Namespace = GetObject("LDAP:")

' Insert code to safely get the user name and password
 
Set User = Namespace.OpenDSObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=COM", sUserName, sPassword, ADS_SECURE_AUTHENTICATION)
 
NewName = InputBox("Enter a new name:")
 
' Set using IADs::PutMethod
User.Put "FullName", NewName
User.SetInfo

Exit Sub

CleanUp:
    Set IADsOpenDSObject = Nothing
    Set IADsUser = Nothing

End Sub
```



En el ejemplo de código siguiente se muestra cómo usar [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) con un solo valor:


```VB
Dim x As IADs
Dim sUserName As String
Dim sFull As String

On Error GoTo CleanUp

sUserName = InputBox("Enter your user name:")
 
Set x = GetObject("LDAP://CN="& sUserName &",CN=Users,DC=Fabrikam, DC=Com") 

sFull = InputBox ("Enter your full name:")
x.Put "name", sFull
 
' Commit to the directory.
x.SetInfo

Exit Sub

CleanUp:
    MsgBox ("An error has occurred. " & Err.Description)
    Set x = Nothing
```



En el ejemplo de código siguiente se muestra cómo usar [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) con varios valores:


```VB
Dim x As IADs
Dim sFirst As String
Dim sLast As String
Dim sUsername As String

On Error GoTo CleanUp

sUsername = InputBox("User name:")
 
Set x = GetObject("LDAP://CN=" & sUsername & ", CN=Users,DC=Fabrikam, DC=Com")

sFirst = InputBox("Enter your first name:")
sLast = InputBox("Enter your last name:")
 
x.Put "givenName", sFirst
x.Put "sn", sLast
 
'Commit to the directory
x.SetInfo

Exit Sub

CleanUp:
    MsgBox ("An error has occurred. " & Err.Description)
    Set x = Nothing
```



En el ejemplo de código siguiente se muestra cómo usar [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) con valores múltiples y únicos:


```C++
int main(int argc, char* argv[], LPWSTR pszADsPath)
{
   HRESULT hr;
   IADs *pADs=NULL;

   CoInitialize(NULL);

   hr = ADsGetObject(pszADsPath,
                     IID_IADs, 
                    (void**) &pADs );

   if (!SUCCEEDED(hr) )
   {
     return hr;
   }

   VARIANT var;
 
   // Using Put with a single value for the first name
   VariantInit(&var);
   V_BSTR(&var) = SysAllocString(L"Janet");
   V_VT(&var) = VT_BSTR;
   hr = pADs->Put( L"givenName", var );

   // Using Put with a single value for the last name
   VariantClear(&var);
   V_BSTR(&var) = SysAllocString(L"Johns");
   V_VT(&var) = VT_BSTR;
   hr = pADs->Put( L"sn", var ); 
   VariantClear(&var);

   // Using Put with multiple values for other telephones
   LPWSTR pszPhones[] = { L"425 844 1234", L"425 924 4321" };
   DWORD dwNumber = sizeof( pszPhones ) /sizeof(LPWSTR);

   hr = ADsBuildVarArrayStr( pszPhones, dwNumber, &var );
   hr = pADs->Put( L"otherTelephone", var ); 
   VariantClear(&var);

   hr = pADs->SetInfo();
   pADs->Release();

   if (!SUCCEEDED(hr) )
   {
     return hr;
   }

 CoUninitialize();
 return 0;
}
```



 

 




