---
title: Código de ejemplo para enumerar la ACL de un objeto en Active Directory Domain Services
description: Los ejemplos de código siguientes se pueden usar para enumerar la lista de control de acceso (ACL) de un objeto en Active Directory Domain Services.
ms.assetid: 3629ffde-c516-4566-8b40-a913b8355656
ms.tgt_platform: multiple
keywords:
- Código de ejemplo para enumerar la ACL de un Active Directory Object AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17ff3a28b66b0217e2b10037ec5a6ebb817aec33780a5ad1ba4efa6092a3cbe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190633"
---
# <a name="example-code-for-enumerating-the-acl-of-an-object-in-active-directory-domain-services"></a>Código de ejemplo para enumerar la ACL de un objeto en Active Directory Domain Services

Los ejemplos de código siguientes se pueden usar para enumerar la lista de control de acceso (ACL) de un objeto en Active Directory Domain Services.

En el ejemplo de código siguiente se muestra una función que enumera los administradores de confianza de un objeto .


```C++
//*******************************************************************
//
//  EnumTrustees()
//
//*******************************************************************

HRESULT EnumTrustees(IADsAccessControlList *pACL)
{
    if(NULL == pACL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IUnknown *pUnk;

    /*
    Get the enumerator from the access control list.
    */
    hr = pACL->get__NewEnum(&pUnk);
    if(SUCCEEDED(hr))
    {
        IEnumVARIANT *pEnum;
        
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (LPVOID*)&pEnum);
        if(SUCCEEDED(hr))
        {
            VARIANT var;
            ULONG ulFetched;
            
            wprintf(L"Trustees:\n");
            
            VariantInit(&var);

            /*
            Enumerate the access control entries 
            in the access control list.
            */
            while( SUCCEEDED(hr = pEnum->Next(1, &var, &ulFetched)) 
                   && (ulFetched > 0) )
            {
                IADsAccessControlEntry *pACE;
                
                /*
                Get the access control entry.
                */
                hr = V_DISPATCH(&var)->QueryInterface(IID_IADsAccessControlEntry, 
                                                      (LPVOID*)&pACE);
                if(SUCCEEDED(hr))
                {
                    CComBSTR sbstrTrustee;

                    /*
                    Get the Trustee for this ACE and print
                    it to the console window.
                    */
                    hr = pACE->get_Trustee(&sbstrTrustee);
                    if(SUCCEEDED(hr))
                    {
                        wprintf(L"\t");
                        wprintf(sbstrTrustee);
                        wprintf(L"\n");
                    }
                    
                    pACE->Release();
                }
                
                VariantClear(&var);
            }
            
            pEnum->Release();
        }

        pUnk->Release();
    }

    return hr;
}

//*******************************************************************
//
//  EnumAccessInfo()
//
//*******************************************************************

HRESULT EnumAccessInfo(IADs *pads)
{
    if(NULL == pads)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    VARIANT var;

    // Get the ntSecurityDescriptor attribute
    VariantInit(&var);
    hr = pads->Get(CComBSTR("ntSecurityDescriptor"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_DISPATCH == var.vt)
        {
            /*
            Get the security descriptor from the
            ntSecurityDescriptor attribute.
            */
            IADsSecurityDescriptor *pSD;
            hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor,
                                                  (LPVOID*)&pSD);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                /*
                Get the DACL from the security descriptor.
                */
                hr = pSD->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, 
                                               (LPVOID*)&pACL);
                    if(SUCCEEDED(hr))
                    {
                        /*
                        Enumerate the trustees of this ACL.
                        */
                        hr = EnumTrustees(pACL);
                        
                        pACL->Release();
                    }
                    
                    pDisp->Release();
                }
                
                pSD->Release();
            }
        }

        VariantClear(&var);
    }

    return hr;
}
```



En el ejemplo de código siguiente se muestra una función que enumera los administradores de confianza de un objeto .


```VB
Private Sub EnumAccessInfo(ByVal oObject As IADs)
    Dim SecDesc As SecurityDescriptor
    Dim Dacl As AccessControlList
    
    On Error GoTo CleanUp
    
    ' Get the security descriptor for the object.
    Set SecDesc = oObject.Get("ntSecurityDescriptor")
    
    ' Get the DACL for the object.
    Set Dacl = SecDesc.DiscretionaryAcl
    
    Debug.Print "Trustees:"

    ' Enumerate the ACEs in the DACL, printing the Trustee for each.
    For Each oACE In Dacl
        Debug.Print vbTab + oACE.Trustee
    Next
    
CleanUp:
    Set SecDesc = Nothing
    Set Dacl = Nothing
End Sub
```



 

 




