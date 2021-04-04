---
title: Detectar el maestro de esquema
description: Active Directory Domain Services tener un sistema de actualización con varios maestros; cada controlador de dominio contiene una copia de escritura del directorio.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Detección del anuncio maestro de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2019
ms.locfileid: "103903927"
---
# <a name="detecting-the-schema-master"></a>Detectar el maestro de esquema

Active Directory Domain Services tener un sistema de actualización con varios maestros; cada controlador de dominio contiene una copia de escritura del directorio. Las actualizaciones de esquema se propagan a todos los dominios que pertenecen al mismo árbol o bosque. Dado que es difícil conciliar las actualizaciones conflictivas en el esquema, las actualizaciones de esquema solo se pueden realizar en un solo servidor. El servidor con el derecho a realizar actualizaciones puede cambiar, pero solo un servidor tendrá el derecho en un momento dado. Este servidor se denomina maestro de esquema. El primer controlador de dominio instalado en una empresa es, de forma predeterminada, el maestro de esquema.

Los cambios de esquema solo se pueden realizar en el nivel de maestro de esquema. Para detectar qué controlador de dominio es el maestro de esquema, realice los pasos siguientes.

**Detectar el maestro de esquema DC**

1.  Lea el atributo **fsmoRoleOwner** del contenedor de esquemas en cualquier controlador de dominio. El atributo **fsmoRoleOwner** devuelve el nombre distintivo (DN) del objeto **nTDSDSA** para el maestro de esquema.
2.  Enlace al objeto **nTDSDSA** cuyo DN acaba de recuperar. El elemento primario de este objeto es el objeto de servidor del controlador de dominio que contiene el maestro de esquema.
3.  Obtiene el ADsPath para el elemento primario del objeto **nTDSDSA** . El elemento primario es un objeto de servidor.
4.  Enlazar al objeto de servidor.
5.  Obtiene el atributo **DnsHostName** del objeto de servidor. Es el nombre DNS del controlador de dominio que contiene el maestro de esquema.
6.  Especifique el nombre DNS del maestro de esquema como el servidor y el DN como el DN del contenedor de esquemas que se va a enlazar al maestro de esquema. Por ejemplo, si el servidor era "dc1.fabrikam.com" y el DN del contenedor de esquemas fuera "CN = Schema, CN = Configuration, DC = Fabrikam, DC = com", el ADsPath sería como se indica a continuación.
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

Se recomienda encontrar el maestro de esquema y enlazarlo para realizar cambios en el esquema. Sin embargo, puede trasladar el maestro de esquema a otro servidor.

Para convertir otro servidor en el maestro de esquema, un usuario con privilegios adecuados puede:

-   Use el complemento MMC del administrador de esquemas.
    > [!Note]
    > El complemento MMC de esquema Active Directory debe registrarse manualmente. Para registrar el complemento esquema, debe ejecutar el siguiente comando desde el símbolo del sistema en el directorio system32 de Windows.
    >
    > **regsvr32.exe schmmgmt.dll**

     

-   Use la utilidad de línea de comandos NTDSUTIL.
-   Usar una aplicación de terceros (una aplicación que emite la escritura LDAP adecuada).

Para convertirse en el maestro de esquema mediante programación, una aplicación que se ejecuta en el contexto de un usuario con privilegios adecuados puede emitir una escritura LDAP del atributo operativo **becomeschemamaster.** a RootDSE en dicho controlador de dominio. Esto inicia una transferencia atómica del derecho del maestro de esquema desde el titular actual hasta el controlador de dominio local.

En el ejemplo de código siguiente se busca el maestro de esquema. La función siguiente enlaza al contenedor de esquema en el equipo que es el maestro de esquema.


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



En el ejemplo de código siguiente se muestra el nombre DNS del equipo que es el maestro de esquema.


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




