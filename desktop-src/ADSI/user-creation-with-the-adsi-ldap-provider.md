---
title: Creación de usuarios con el proveedor LDAP ADSI
description: Con el proveedor LDAP ADSI, solo puede crear una cuenta de usuario global.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- PROVEEDOR LDAP ADSI, objeto de usuario, creación de usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32d076805b9480ed0344712f7b023efab4ef0a025f367cc9c5ebb0bb7dfc0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023073"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Creación de usuarios con el proveedor LDAP ADSI

Con el proveedor LDAP ADSI, solo puede crear una cuenta de usuario global. Las cuentas locales residen en la base de datos SAM y deben crearse mediante el proveedor WinNT. Para obtener más información sobre cómo crear un objeto de usuario con el proveedor de WinNT, vea [Objeto de usuario de WinNT](winnt-user-object.md).

**Para crear un objeto de usuario**

1.  Enlace al contenedor donde residirá el objeto de usuario y obtenga la [**interfaz IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) del contenedor.
2.  Use el [**método IADsContainer.Create o**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para crear el objeto de usuario.
3.  Los atributos mínimos necesarios para crear un objeto de usuario dependerán del servicio de directorio usado. Para obtener más información sobre cómo crear Active Directory usuario, vea [Creating a User](/windows/desktop/AD/creating-a-user).
4.  Si se usa la interfaz [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) el nuevo objeto no se crea realmente hasta que se llama al método [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

    Si se usa la interfaz [**IDirectoryObject,**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) el nuevo objeto se crea cuando se llama al [**método CreateDSObject.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) Los atributos mínimos, incluido [**objectClass**](/windows/desktop/ADSchema/a-objectclass), deben especificarse en la matriz [**\_ ADS ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pasada al **método CreateDSObject.**

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se crea una cuenta de usuario con los atributos predeterminados.


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se crea una cuenta de usuario con los atributos predeterminados. Por brevedad, se omite la comprobación de errores.


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 