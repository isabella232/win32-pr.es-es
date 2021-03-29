---
title: La modificación del usuario no puede cambiar la contraseña (proveedor LDAP)
description: La capacidad de un usuario de cambiar su propia contraseña es un permiso que se puede conceder o denegar.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- La modificación del usuario no puede cambiar la contraseña (proveedor LDAP) ADSI
- El usuario no puede cambiar la contraseña (proveedor LDAP) ADSI, modificar
- ADSI Provider LDAP, ejemplos de administración de usuarios, el usuario debe cambiar la contraseña en el siguiente inicio de sesión, modificar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1628b113c2f15278bc72e41aa79e4be03a98f2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793857"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a><span data-ttu-id="775c2-106">La modificación del usuario no puede cambiar la contraseña (proveedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="775c2-106">Modifying User Cannot Change Password (LDAP Provider)</span></span>

<span data-ttu-id="775c2-107">La capacidad de un usuario de cambiar su propia contraseña es un permiso que se puede conceder o denegar.</span><span class="sxs-lookup"><span data-stu-id="775c2-107">The ability of a user to change their own password is a permission that can be grant or denied.</span></span> <span data-ttu-id="775c2-108">Para denegar este permiso, establezca dos entradas ACE en la lista de control de acceso discrecional (DACL) del descriptor de seguridad del objeto de usuario con el tipo de ACE de **\_ \_ objeto de acceso \_ denegado \_ de ADS ACETYPE** .</span><span class="sxs-lookup"><span data-stu-id="775c2-108">To deny this permission, set two ACEs in the security descriptor discretionary access control list (DACL) of the user object with the **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** ace type.</span></span> <span data-ttu-id="775c2-109">Una ACE deniega el permiso al usuario y otra ACE deniega el permiso al grupo todos.</span><span class="sxs-lookup"><span data-stu-id="775c2-109">One ACE denies the permission to the user and another ACE denies the permission to the Everyone group.</span></span> <span data-ttu-id="775c2-110">Ambas Ace son ACE de denegación específicas del objeto que especifican el GUID del permiso extendido para cambiar las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="775c2-110">Both ACEs are object-specific deny ACEs that specify the GUID of the extended permission for changing passwords.</span></span> <span data-ttu-id="775c2-111">Para conceder este permiso, establezca las mismas ACE con el tipo de ACE de **\_ \_ \_ \_ objeto permitidos de ADS ACETYPE Access** .</span><span class="sxs-lookup"><span data-stu-id="775c2-111">To grant this permission, set the same ACEs with the **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** ace type.</span></span>

<span data-ttu-id="775c2-112">En el procedimiento siguiente se describe cómo modificar o agregar ACE para este permiso.</span><span class="sxs-lookup"><span data-stu-id="775c2-112">The following procedure describes how to modify or add ACEs for this permission.</span></span>

<span data-ttu-id="775c2-113">**Para modificar o agregar las ACE para este permiso**</span><span class="sxs-lookup"><span data-stu-id="775c2-113">**To modify or add the ACEs for this permission**</span></span>

1.  <span data-ttu-id="775c2-114">Enlazar al objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="775c2-114">Bind to the user object.</span></span>
2.  <span data-ttu-id="775c2-115">Obtenga el objeto [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) de la propiedad **ntSecurityDescriptor** del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="775c2-115">Obtain the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) object from the **ntSecurityDescriptor** property of the user object.</span></span>
3.  <span data-ttu-id="775c2-116">Obtenga una interfaz [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) para el descriptor de seguridad de la propiedad [**IADsSecurityDescriptor. DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="775c2-116">Obtain an [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface for the security descriptor from the [**IADsSecurityDescriptor.DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) property.</span></span>
4.  <span data-ttu-id="775c2-117">Enumere las ACE para el objeto y busque las ACE que tengan el GUID de cambio de contraseña ({AB721A53-1E2F-11D0-9819-00AA0040529B}) para la propiedad [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) y "everyone" o "NT Authority \\ Self" para la propiedad **IADsAccessControlEntry. Trustee** .</span><span class="sxs-lookup"><span data-stu-id="775c2-117">Enumerate the ACEs for the object and search for the ACEs that have the change password GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) for the [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) property and "Everyone" or "NT AUTHORITY\\SELF" for the **IADsAccessControlEntry.Trustee** property.</span></span>

    > [!Note]  
    > <span data-ttu-id="775c2-118">Las cadenas "todos" y "NT AUTHORITY \\ Self" se localizan en función del idioma del primer controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="775c2-118">The "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="775c2-119">Por este motivo, las cadenas no deben usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="775c2-119">Because of this, the strings should not be used directly.</span></span> <span data-ttu-id="775c2-120">Los nombres de cuenta se deben obtener en tiempo de ejecución mediante una llamada a la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) con el SID para "todos" ("s-1-1-0") y "NT Authority \\ Self" ("s-1-5-10") entidades de seguridad conocidas.</span><span class="sxs-lookup"><span data-stu-id="775c2-120">The account names should be obtained at run time by calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function with the SID for "Everyone" ("S-1-1-0") and "NT AUTHORITY\\SELF" ("S-1-5-10") well-known security principals.</span></span> <span data-ttu-id="775c2-121">Las funciones de ejemplo **GetSidAccountName**, **GetSidAccountName \_ Everyone** y **GetSidAccountName \_ Self** C++ que se muestran en [lectura de usuarios no pueden cambiar la contraseña (proveedor LDAP)](reading-user-cannot-change-password-ldap-provider.md) demuestran cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="775c2-121">The **GetSidAccountName**, **GetSidAccountName\_Everyone**, and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md) demonstrate how to do this.</span></span>

     

5.  <span data-ttu-id="775c2-122">Modifique la propiedad [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md) de las ACE encontradas a **ADS AceType el \_ \_ objeto de acceso \_ denegado \_** si el usuario no puede cambiar su contraseña o **ADS \_ AceType \_ acceso \_ permitido \_** si el usuario puede cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="775c2-122">Modify the [**IADsAccessControlEntry.AceType**](iadsaccesscontrolentry-property-methods.md) property of the ACEs that were found to **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span>
6.  <span data-ttu-id="775c2-123">Si no se encuentra la ACE "everyone", cree un nuevo objeto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) que contenga los valores de propiedad que se muestran en la tabla siguiente y agregue la nueva entrada a la ACL con el método [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="775c2-123">If the "Everyone" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object that contains the property values shown in the table below and add the new entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
7.  <span data-ttu-id="775c2-124">Si \\ no se encuentra la ACE "NT Authority Self", cree un nuevo objeto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) con los mismos valores de propiedad que se muestran en la tabla siguiente, excepto que la propiedad [**Trustee**](iadsaccesscontrolentry-property-methods.md) contiene el nombre de cuenta del SID "S-1-5-10" ("NT Authority \\ Self").</span><span class="sxs-lookup"><span data-stu-id="775c2-124">If the "NT AUTHORITY\\SELF" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object with the same property values shown in the table below except the [**Trustee**](iadsaccesscontrolentry-property-methods.md) property contains the account name for SID "S-1-5-10" ("NT AUTHORITY\\SELF").</span></span> <span data-ttu-id="775c2-125">Agregue la entrada a la ACL con el método [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="775c2-125">Add the entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
8.  <span data-ttu-id="775c2-126">Para actualizar la propiedad **ntSecurityDescriptor** del objeto, llame al método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) con el mismo [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtenido en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="775c2-126">To update the **ntSecurityDescriptor** property of the object, call the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method with the same [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtained in Step 2.</span></span>
9.  <span data-ttu-id="775c2-127">Confirme los cambios locales en el servidor con el método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="775c2-127">Commit the local changes to the server with the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>
10. <span data-ttu-id="775c2-128">Si se creó alguna de las ACE, debe reordenar la ACL para que las ACE estén en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="775c2-128">If either of the ACEs were created, you must reorder the ACL so that the ACEs are in the correct order.</span></span> <span data-ttu-id="775c2-129">Para ello, llame a la función [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) con la ADsPath LDAP del objeto y, a continuación, la función [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) con la misma DACL.</span><span class="sxs-lookup"><span data-stu-id="775c2-129">To do this, call the [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) function with the LDAP ADsPath of the object and then the [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) function with the same DACL.</span></span> <span data-ttu-id="775c2-130">Esta reordenación se realizará automáticamente cuando se agreguen las ACE.</span><span class="sxs-lookup"><span data-stu-id="775c2-130">This reordering will occur automatically when the ACEs are added.</span></span>

<span data-ttu-id="775c2-131">En la tabla siguiente se enumeran los valores de propiedad del objeto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="775c2-131">The following table lists the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object property values.</span></span>



| <span data-ttu-id="775c2-132">Propiedad IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="775c2-132">IADsAccessControlEntry Property</span></span>                                        | <span data-ttu-id="775c2-133">Value</span><span class="sxs-lookup"><span data-stu-id="775c2-133">Value</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="775c2-134">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="775c2-134">**AccessMask**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="775c2-135">**\_acceso de \_ \_ control DS derecho de \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="775c2-135">**ADS\_RIGHT\_DS\_CONTROL\_ACCESS**</span></span>                                                                                                                                   |
| [<span data-ttu-id="775c2-136">**AceType**</span><span class="sxs-lookup"><span data-stu-id="775c2-136">**AceType**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="775c2-137">**Anuncios \_ de ACETYPE \_ acceso \_ denegado a un \_ objeto** si el usuario no puede cambiar su contraseña o el **\_ \_ \_ \_ objeto ACETYPE permitido de acceso a ADS** si el usuario puede cambiar su contraseña.</span><span class="sxs-lookup"><span data-stu-id="775c2-137">**ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span> |
| [<span data-ttu-id="775c2-138">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="775c2-138">**AceFlags**</span></span>](iadsaccesscontrolentry-property-methods.md)            | <span data-ttu-id="775c2-139">0</span><span class="sxs-lookup"><span data-stu-id="775c2-139">0</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="775c2-140">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="775c2-140">**Flags**</span></span>](iadsaccesscontrolentry-property-methods.md)               | <span data-ttu-id="775c2-141">**\_tipo de objeto de marca ADS \_ \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="775c2-141">**ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**</span></span>                                                                                                                                  |
| [<span data-ttu-id="775c2-142">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="775c2-142">**ObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="775c2-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}", que es el GUID de cambio de contraseña en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="775c2-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}" which is the change password GUID in string form.</span></span>                                                                            |
| [<span data-ttu-id="775c2-144">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="775c2-144">**InheritedObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md) | <span data-ttu-id="775c2-145">No se usa</span><span class="sxs-lookup"><span data-stu-id="775c2-145">Not used</span></span>                                                                                                                                                              |
| [<span data-ttu-id="775c2-146">**Confianza**</span><span class="sxs-lookup"><span data-stu-id="775c2-146">**Trustee**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="775c2-147">Nombre de cuenta del SID "S-1-1-0" (todos).</span><span class="sxs-lookup"><span data-stu-id="775c2-147">Account name for SID "S-1-1-0" (Everyone).</span></span>                                                                                                                            |



 

## <a name="example-code"></a><span data-ttu-id="775c2-148">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="775c2-148">Example Code</span></span>

<span data-ttu-id="775c2-149">En el ejemplo de código siguiente se muestra cómo obtener una interfaz para cambiar una DACL.</span><span class="sxs-lookup"><span data-stu-id="775c2-149">The following code example shows how to obtain an interface to change a DACL.</span></span> <span data-ttu-id="775c2-150">La interfaz [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) se puede usar si se establece la opción DACL de información de seguridad de **ADS \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="775c2-150">The [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) interface can be used by setting the **ADS\_SECURITY\_INFO\_DACL** option.</span></span>

> [!Note]  
> <span data-ttu-id="775c2-151">Para usar el código documentado en este ejemplo, debe ser administrador.</span><span class="sxs-lookup"><span data-stu-id="775c2-151">To use the code documented in this example, you will need to be an Administrator.</span></span> <span data-ttu-id="775c2-152">Si no es administrador, tendrá que agregar más código que utilizará una interfaz que permitirá a un usuario cambiar la manera en que la memoria caché del lado cliente se vacía de nuevo en el servicio de Dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="775c2-152">If you are not an Administrator, then you will need to add more code that will use an interface that will allow a user to change the way the client-side cache is flushed back to the Active Directory Domain Service.</span></span>

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



<span data-ttu-id="775c2-153">En el ejemplo de código siguiente se muestra cómo modificar el permiso el usuario no puede cambiar la contraseña mediante el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="775c2-153">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span> <span data-ttu-id="775c2-154">En este ejemplo de código se usa la función de utilidad **GetObjectACE** definida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="775c2-154">This code example uses the **GetObjectACE** utility function defined above.</span></span>

<span data-ttu-id="775c2-155">En este ejemplo se usan las funciones de ejemplo **GetSidAccountName \_ Everyone** y **GetSidAccountName \_ Self** C++ que se muestran en [leer el usuario no puede cambiar la contraseña (proveedor LDAP)](reading-user-cannot-change-password-ldap-provider.md).</span><span class="sxs-lookup"><span data-stu-id="775c2-155">This example uses the **GetSidAccountName\_Everyone** and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md).</span></span>


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="775c2-156">En el ejemplo de código siguiente se muestra cómo modificar el permiso el usuario no puede cambiar la contraseña mediante el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="775c2-156">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span>

> [!Note]  
> <span data-ttu-id="775c2-157">El siguiente ejemplo solo funcionará en los dominios en los que el idioma principal sea el inglés, ya que las cadenas "todos" y "NT AUTHORITY \\ Self" se localizan en función del idioma del primer controlador de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="775c2-157">The example below will only work on domains where the primary language is English because the "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="775c2-158">No hay ninguna manera de Visual Basic para obtener los nombres de cuenta de una entidad de seguridad conocida sin llamar a la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) .</span><span class="sxs-lookup"><span data-stu-id="775c2-158">There is no way in Visual Basic to obtain the account names for a well-known security principal without calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function.</span></span> <span data-ttu-id="775c2-159">Si usa Visual Basic, se recomienda que use el proveedor de WinNT para modificar el permiso el usuario no puede cambiar la contraseña, tal como se muestra en [modificación de usuario no puede cambiar la contraseña (proveedor de WinNT)](modifying-user-cannot-change-password-winnt-provider.md).</span><span class="sxs-lookup"><span data-stu-id="775c2-159">If using Visual Basic, it is suggested that you use the WinNT provider to modify the User Cannot Change Password Permission as shown in [Modifying User Cannot Change Password (WinNT Provider)](modifying-user-cannot-change-password-winnt-provider.md).</span></span>

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 