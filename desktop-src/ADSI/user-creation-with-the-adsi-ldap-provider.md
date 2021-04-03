---
title: Creación de usuarios con el proveedor LDAP de ADSI
description: Con el proveedor LDAP de ADSI, solo puede crear una cuenta de usuario global.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI Provider de LDAP, objeto de usuario, creación de usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104083694"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="ef63b-104">Creación de usuarios con el proveedor LDAP de ADSI</span><span class="sxs-lookup"><span data-stu-id="ef63b-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="ef63b-105">Con el proveedor LDAP de ADSI, solo puede crear una cuenta de usuario global.</span><span class="sxs-lookup"><span data-stu-id="ef63b-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="ef63b-106">Las cuentas locales residen en la base de datos SAM y deben crearse con el proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="ef63b-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="ef63b-107">Para obtener más información sobre cómo crear un objeto de usuario con el proveedor de WinNT, vea el [objeto de usuario WinNT](winnt-user-object.md).</span><span class="sxs-lookup"><span data-stu-id="ef63b-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="ef63b-108">**Para crear un objeto de usuario**</span><span class="sxs-lookup"><span data-stu-id="ef63b-108">**To create a user object**</span></span>

1.  <span data-ttu-id="ef63b-109">Enlace al contenedor donde residirá el objeto de usuario y obtenga la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ef63b-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="ef63b-110">Use el método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) o [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para crear el objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef63b-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="ef63b-111">Los atributos mínimos necesarios para crear un objeto de usuario dependerán del servicio de directorio que se use.</span><span class="sxs-lookup"><span data-stu-id="ef63b-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="ef63b-112">Para obtener más información acerca de cómo crear un usuario Active Directory, consulte [crear un usuario](/windows/desktop/AD/creating-a-user).</span><span class="sxs-lookup"><span data-stu-id="ef63b-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="ef63b-113">Si se utiliza la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , el nuevo objeto no se crea realmente hasta que se llama al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="ef63b-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="ef63b-114">Si se usa la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) , se crea el nuevo objeto cuando se llama al método [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="ef63b-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="ef63b-115">Los atributos mínimos, incluido [**objectClass**](/windows/desktop/ADSchema/a-objectclass), deben especificarse en la matriz [**de \_ \_ información**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) de atributos de ADS pasada al método **CreateDSObject** .</span><span class="sxs-lookup"><span data-stu-id="ef63b-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="ef63b-116">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef63b-116">Example 1</span></span>

<span data-ttu-id="ef63b-117">En el ejemplo de código siguiente se crea una cuenta de usuario con los atributos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ef63b-117">The following code example creates a user account with the default attributes.</span></span>


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



## <a name="example-2"></a><span data-ttu-id="ef63b-118">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ef63b-118">Example 2</span></span>

<span data-ttu-id="ef63b-119">En el ejemplo de código siguiente se crea una cuenta de usuario con los atributos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ef63b-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="ef63b-120">Por motivos de brevedad, se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="ef63b-120">For brevity, error checking is omitted.</span></span>


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



 

 