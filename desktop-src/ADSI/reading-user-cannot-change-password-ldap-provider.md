---
title: Leer el usuario no puede cambiar la contraseña (proveedor LDAP)
description: Obtenga información sobre cómo determinar si un usuario tiene permiso para cambiar una contraseña para el proveedor LDAP. La capacidad de un usuario para cambiar una contraseña se puede conceder o denegar.
ms.assetid: d0d95d20-dcdb-453a-9d15-c386217927c8
ms.tgt_platform: multiple
keywords:
- AdsI de lectura del usuario no se puede cambiar la contraseña (proveedor LDAP)
- ADSI del usuario no se puede cambiar la contraseña (proveedor LDAP), leer
- ADSI del proveedor LDAP, ejemplos de administración de usuarios, El usuario debe cambiar la contraseña en el siguiente inicio de sesión, leer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26818ee02d3876aa209dcd4990288ea1cfe96fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405938"
---
# <a name="reading-user-cannot-change-password-ldap-provider"></a><span data-ttu-id="81f96-107">Leer el usuario no puede cambiar la contraseña (proveedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="81f96-107">Reading User Cannot Change Password (LDAP Provider)</span></span>

<span data-ttu-id="81f96-108">La capacidad de un usuario para cambiar su contraseña es un permiso que se puede conceder o denegar.</span><span class="sxs-lookup"><span data-stu-id="81f96-108">The ability of a user to change their password is a permission that can be granted or denied.</span></span>

<span data-ttu-id="81f96-109">**Para determinar si se concede o se deniega el permiso de cambio de contraseña**</span><span class="sxs-lookup"><span data-stu-id="81f96-109">**To determine if the change password permission is granted or denied**</span></span>

1.  <span data-ttu-id="81f96-110">Enlace al objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="81f96-110">Bind to the user object.</span></span>
2.  <span data-ttu-id="81f96-111">Obtenga el [**objeto IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) de la **propiedad ntSecurityDescriptor** del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="81f96-111">Obtain the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) object from the **ntSecurityDescriptor** property of the user object.</span></span>
3.  <span data-ttu-id="81f96-112">Obtenga una [**interfaz IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) para el descriptor de seguridad de la [**propiedad IADsSecurityDescriptor.DiscretionaryAcl.**](iadssecuritydescriptor-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="81f96-112">Obtain an [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface for the security descriptor from the [**IADsSecurityDescriptor.DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) property.</span></span>
4.  <span data-ttu-id="81f96-113">Enumerar las entradas de control de acceso (ACE) del objeto y buscar las ACE que tienen el GUID de contraseña de cambio ({AB721A53-1E2F-11D0-9819-00AA0040529B}) para la propiedad [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) y las entidades de seguridad conocidas "Everyone" o "NT AUTHORITY SELF" para la propiedad \\ **IADsAccessControlEntry.Trustee.**</span><span class="sxs-lookup"><span data-stu-id="81f96-113">Enumerate the access control entries (ACE) for the object and search for the ACEs that have the change password GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) for the [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) property and "Everyone" or "NT AUTHORITY\\SELF" well-known security principals for the **IADsAccessControlEntry.Trustee** property.</span></span>
    > [!Note]  
    > <span data-ttu-id="81f96-114">Las cadenas "Todos" y "NT AUTHORITY SELF" se localizan en función del idioma del primer controlador \\ de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="81f96-114">The "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="81f96-115">Por lo tanto, las cadenas no deben usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="81f96-115">Therefore, the strings should not be used directly.</span></span> <span data-ttu-id="81f96-116">Los nombres de cuenta se deben obtener en tiempo de ejecución llamando a la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) con el SID de las entidades de seguridad conocidas "S-1-1-0") y "NT AUTHORITY \\ SELF" ("S-1-5-10").</span><span class="sxs-lookup"><span data-stu-id="81f96-116">The account names should be obtained at run time by calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function with the SID for the "Everyone" ("S-1-1-0") and "NT AUTHORITY\\SELF" ("S-1-5-10") well-known security principals.</span></span> <span data-ttu-id="81f96-117">Los siguientes ejemplos de código de C++ **GetSidAccountName**, **GetSidAccountName \_ Everyone** y **GetSidAccountName \_ Self** muestran cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="81f96-117">The following C++ **GetSidAccountName**, **GetSidAccountName\_Everyone**, and **GetSidAccountName\_Self** code examples show how to do this.</span></span>

     

5.  <span data-ttu-id="81f96-118">Si las ACE "Everyone" y "NT AUTHORITY SELF" tienen el valor \\ **ADS \_ ACETYPE ACCESS \_ DENIED \_ \_ OBJECT** para la propiedad [**IADsAccessControlEntry.AceType,**](iadsaccesscontrolentry-property-methods.md) se deniega el permiso.</span><span class="sxs-lookup"><span data-stu-id="81f96-118">If both the "Everyone" and "NT AUTHORITY\\SELF" ACEs have the **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** value for the [**IADsAccessControlEntry.AceType**](iadsaccesscontrolentry-property-methods.md) property, then the permission is denied.</span></span>

## <a name="example-code"></a><span data-ttu-id="81f96-119">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="81f96-119">Example Code</span></span>

<span data-ttu-id="81f96-120">En el ejemplo de código siguiente se muestra cómo determinar si el usuario no puede cambiar el permiso de contraseña mediante el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="81f96-120">The following code example shows how to determine if the User Cannot Change Password Permission using the LDAP provider.</span></span>


```C++
/***************************************************************************

    GetSidAccountName()

    Retrieves the account name for the specified SID.

    pSid - Pointer to the SID that the account name should be retrieved for.

    pbstrAccountName - Pointer to a BSTR that receives the account name. The 
    caller must free this with SysFreeString when it is no longer required.

***************************************************************************/

HRESULT GetSidAccountName(PSID pSid, BSTR *pbstrAccountName)
{
    if(!pbstrAccountName)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    BOOL fReturn;

    WCHAR wszAccountName[MAX_PATH];
    DWORD dwAccountName;
    WCHAR wszDomainName[MAX_PATH];
    DWORD dwDomainName;
    SID_NAME_USE SidNameUse;
    DWORD dwSidSize;

    dwAccountName = MAX_PATH;
    dwDomainName = MAX_PATH;
    dwSidSize = SECURITY_MAX_SID_SIZE;

    /*
    Get the account name for the specified SID.
    */
    fReturn = LookupAccountSidW(
        NULL, 
        pSid, 
        wszAccountName, 
        &dwAccountName, 
        wszDomainName, 
        &dwDomainName, 
        &SidNameUse);
    if(fReturn)
    {
        CComBSTR sbstrReturn;

        if(lstrlenW(wszDomainName) > 0)
        {
            sbstrReturn = wszDomainName;
            sbstrReturn += "\\";
            sbstrReturn += wszAccountName;
        }
        else
        {
            sbstrReturn = wszAccountName;
        }

        *pbstrAccountName = sbstrReturn.Detach();
        hr = S_OK;
    }

    return hr;
}

/***************************************************************************

    GetSidAccountName_Everyone()

    Retrieves the local account name for the "World", also known as 
    "Everyone", account.

    pbstrAccountName - Pointer to a BSTR that receives the account name. The 
    caller must free this with SysFreeString when it is no longer required.

***************************************************************************/

HRESULT GetSidAccountName_Everyone(BSTR *pbstrAccountName)
{
    if(!pbstrAccountName)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    BOOL fReturn;
    PSID psidAlloc;

    // Create the SID for "Everyone".
    SID_IDENTIFIER_AUTHORITY SidAuth = SECURITY_WORLD_SID_AUTHORITY;
    fReturn = AllocateAndInitializeSid(
        &SidAuth, 
        1, 
        SECURITY_WORLD_RID, 
        0, 0, 0, 0, 0, 0, 0, 
        &psidAlloc);
    if(fReturn)
    {
        hr = GetSidAccountName(psidAlloc, pbstrAccountName);

        LocalFree(psidAlloc);
    }

    return hr;
}

/***************************************************************************

    GetSidAccountName_Self()

    Retrieves the local account name for the "NT AUTHORITY\SELF" account.

    pbstrAccountName - Pointer to a BSTR that receives the account name. The 
    caller must free this with SysFreeString when it is no longer required.

***************************************************************************/

HRESULT GetSidAccountName_Self(BSTR *pbstrAccountName)
{
    HRESULT hr = E_FAIL;
    BOOL fReturn;
    PSID psidAlloc;

    // Create the SID for "Everyone".
    SID_IDENTIFIER_AUTHORITY SidAuth = SECURITY_NT_AUTHORITY;
    fReturn = AllocateAndInitializeSid(
        &SidAuth, 
        1, 
        SECURITY_PRINCIPAL_SELF_RID, 
        0, 0, 0, 0, 0, 0, 0, 
        &psidAlloc);
    if(fReturn)
    {
        hr = GetSidAccountName(psidAlloc, pbstrAccountName);

        LocalFree(psidAlloc);
    }

    return hr;
}

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    GetObjectACE()

    Retrieves the IADsAccessControlEntry for the ACE that matches the 
    specified object type and trustee in the specified IADsAccessControlList. 
    Returns a value other than S_OK if the ACE is not found.

    pACL - Pointer to an IADsAccessControlList object that will be searched.

    pwszObject - Pointer to a null-terminated Unicode string that contains 
    the object type to find.

    pwszTrustee - Pointer to a null-terminated Unicode string that contains 
    the trustee to find.

    ppACE - Pointer to an IADsAccessControlEntry pointer that receives the 
    ACE if successful. This receives NULL if not successful.

***************************************************************************/

HRESULT GetObjectACE(IADsAccessControlList* pACL, 
                     LPCWSTR pwszObject, 
                     LPCWSTR pwszTrustee, 
                     IADsAccessControlEntry** ppACE)
{
    if(NULL == pACL || NULL == pwszObject)
    {
        return E_INVALIDARG;
    }

    *ppACE = NULL;
                        
    HRESULT hr;
    IUnknown *pUnk;
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr))
    {
        return hr;
    }

    IEnumVARIANT *pEnum;

    hr = pUnk->QueryInterface(IID_IEnumVARIANT, (LPVOID*)&pEnum);
    if(SUCCEEDED(hr)) 
    {
        ULONG ulFetched;
        BOOL fEveryone = FALSE;
        BOOL fSelf = FALSE;
        CComVariant svarACE;

        for(hr = pEnum->Next(1, &svarACE, &ulFetched); 
            S_OK == hr && 1 == ulFetched; 
            hr = pEnum->Next(1, &svarACE, &ulFetched))
        {
            if(VT_DISPATCH == svarACE.vt)
            {
                IADsAccessControlEntry *pACE;
                
                hr = svarACE.pdispVal->QueryInterface(IID_IADsAccessControlEntry, (void**)&pACE);
                if(SUCCEEDED(hr))
                {
                    CComBSTR sbstrObjectType;

                    hr = pACE->get_ObjectType(&sbstrObjectType);
                    if(SUCCEEDED(hr))
                    {
                        if(0 == lstrcmpiW(pwszObject, sbstrObjectType))
                        {
                            CComBSTR sbstrTrustee;

                            hr = pACE->get_Trustee(&sbstrTrustee);
                            if(SUCCEEDED(hr) && (0 == lstrcmpiW(sbstrTrustee, pwszTrustee)))
                            {
                                *ppACE = pACE;
                                break;
                            }
                        }
                    }

                    pACE->Release();
                }
            }
        }

        pEnum->Release();
    }

    return hr;
}

/***************************************************************************

    UserCannotChangePassword()

    Retrieves the "User Cannot Change Password" privilege using the LDAP 
    provider. This is determined by the presence and value of the change 
    password GUID ACE for the Everyone and Self trustees. The default result 
    of this function is that the user can change their password unless the 
    two ACEs specifically deny the privilege.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to verify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    pfCannotChangePassword - Receives the setting for the privilege. 
    Receives nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT UserCannotChangePassword(LPCWSTR pwszUserDN, 
                                 LPCWSTR pwszUsername, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
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
    *pfCannotChangePassword = FALSE;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("ntSecurityDescriptor"), &svar);
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
                        BOOL fEveryone = FALSE;
                        BOOL fSelf = FALSE;
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        IADsAccessControlEntry *pACESelf = NULL;

                        // Get the ACE for everyone.
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        
                        // Get the ACE for self.
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        
                        if(pACEEveryone && pACESelf)
                        {
                            LONG lAceType;

                            hr = pACEEveryone->get_AceType(&lAceType);
                            if(SUCCEEDED(hr) && (ADS_ACETYPE_ACCESS_DENIED_OBJECT == lAceType))
                            {
                                fEveryone = TRUE;
                            }

                            hr = pACESelf->get_AceType(&lAceType);
                            if(SUCCEEDED(hr) && (ADS_ACETYPE_ACCESS_DENIED_OBJECT == lAceType))
                            {
                                fSelf = TRUE;
                            }
                        }

                        if(fEveryone && fSelf)
                        {
                            *pfCannotChangePassword = TRUE;
                        }
                        else
                        {
                            *pfCannotChangePassword = FALSE;
                        }
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



<span data-ttu-id="81f96-121">En el ejemplo de código siguiente se muestra cómo determinar el permiso User Cannot Change Password mediante el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="81f96-121">The following code example shows how to determine the User Cannot Change Password Permission using the LDAP provider.</span></span>

> [!Note]  
> <span data-ttu-id="81f96-122">El ejemplo de código siguiente solo funciona para los dominios en los que el idioma principal es el inglés, porque las cadenas "Todos" y "NT AUTHORITY SELF" se localizan en función del idioma del primer controlador de dominio del \\ dominio.</span><span class="sxs-lookup"><span data-stu-id="81f96-122">The following code example only works for domains where the primary language is English, because the "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="81f96-123">No hay ninguna manera de Visual Basic los nombres de cuenta de una entidad de seguridad conocida sin llamar a la [**función LookupAccountSid.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida)</span><span class="sxs-lookup"><span data-stu-id="81f96-123">There is no way in Visual Basic to obtain the account names for a well-known security principal without calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function.</span></span> <span data-ttu-id="81f96-124">Si usa Visual Basic, se recomienda usar el proveedor winNT para determinar el permiso Usuario no se puede cambiar la contraseña, como se muestra en Lectura del usuario no se puede cambiar la contraseña [(proveedor winNT).](reading-user-cannot-change-password-winnt-provider.md)</span><span class="sxs-lookup"><span data-stu-id="81f96-124">If using Visual Basic, it is suggested that you use the WinNT provider to determine the User Cannot Change Password Permission as shown in [Reading User Cannot Change Password (WinNT Provider)](reading-user-cannot-change-password-winnt-provider.md).</span></span>

 


```VB
Const CHANGE_PASSWORD_GUID = "{AB721A53-1E2F-11D0-9819-00AA0040529B}"
Const ADS_ACETYPE_ACCESS_DENIED_OBJECT = &H6

Function UserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    Dim fEveryone As Boolean
    Dim fSelf As Boolean
    
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
    
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" And oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT Then
                fEveryone = True
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" And oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT Then
                fSelf = True
            End If
        End If
    Next
    
    If fSelf And fEveryone Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



 

 