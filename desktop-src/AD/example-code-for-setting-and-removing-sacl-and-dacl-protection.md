---
title: Código de ejemplo para establecer y quitar la protección SACL y DACL
description: En este tema se incluye un ejemplo de código que se usa para establecer y quitar la protección SACL y DACL.
ms.assetid: 1982ee9a-022a-4e5d-be9c-fab8894afa9e
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, establecer y quitar la protección SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c77cb1da29aa650fe4559c3da27c6a00f59e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656342"
---
# <a name="example-code-for-setting-and-removing-sacl-and-dacl-protection"></a><span data-ttu-id="b1c96-104">Código de ejemplo para establecer y quitar la protección SACL y DACL</span><span class="sxs-lookup"><span data-stu-id="b1c96-104">Example Code for Setting and Removing SACL and DACL Protection</span></span>

<span data-ttu-id="b1c96-105">En este tema se incluye un ejemplo de código que se usa para establecer y quitar la protección SACL y DACL.</span><span class="sxs-lookup"><span data-stu-id="b1c96-105">This topic includes a code example used to set and remove SACL and DACL protection.</span></span>

<span data-ttu-id="b1c96-106">En el siguiente ejemplo de código de C y C++ se establece y se quitan los elementos **\_ \_ protegidos** de DACL y SACL **\_ \_ protegidos de se** en la propiedad [**IADsSecurityDescriptor. control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) de un descriptor de seguridad de objeto.</span><span class="sxs-lookup"><span data-stu-id="b1c96-106">The following C and C++ code example sets and removes the **SE\_DACL\_PROTECTED** and **SE\_SACL\_PROTECTED** elements in the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property of an object security descriptor.</span></span>


```C++
/***************************************************************************

    SetSDInheritProtect()

    This function sets and removes the SE_DACL_PROTECTED and 
    SE_SACL_PROTECTED elements in the Control property. Valid values for 
    lControl are:
        0 - Remove both SE_DACL_PROTECTED and SE_SACL_PROTECTED if they are 
        set.

        SE_DACL_PROTECTED - Add SE_DACL_PROTECTED and remove SE_SACL_PROTECTED.

        SE_SACL_PROTECTED - Add SE_SACL_PROTECTED and remove SE_DACL_PROTECTED.

    Be aware that SE_DACL_PRESENT must be present to set SE_DACL_PROTECTED 
    and SE_SACL_PRESENT must be present to set SE_SACL_PROTECTED.
 
***************************************************************************/

HRESULT SetSDInheritProtect(IADs *pObject, long lControl)
{
    if(!pObject)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    CComVariant svar;
    long lSetControl;
    long lOriginalControl;

    // Get the nTSecurityDescriptor
    CComBSTR sbstrAttribute = "nTSecurityDescriptor";
    hr = pObject->Get(sbstrAttribute, &svar);
    if(FAILED(hr))
    {
        return hr;
    }
    
    /*
    The type should be VT_DISPATCH which is an IDispatch pointer to the security 
    descriptor object.
    */
    if(svar.vt != VT_DISPATCH)
    {
        return E_FAIL;
    }

    /*
    Get the IDispatch pointer from VARIANT structure and call the QueryInterface method for 
    the IADsSecurityDescriptor pointer.
    */
    CComPtr<IADsSecurityDescriptor> spSD;
    hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (void**)&spSD);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the Control property.
    hr = spSD->get_Control(&lSetControl);
    if(FAILED(hr))
    {
        return hr;
    }

    // Save the original value to see if the value changes.
    lOriginalControl = lSetControl;

    if(lControl & SE_DACL_PROTECTED)
    {
        lSetControl |= SE_DACL_PROTECTED;
        lSetControl &= !SE_SACL_PROTECTED;
    }
    else if(lControl & SE_SACL_PROTECTED)
    {
        lSetControl |= SE_SACL_PROTECTED;
        lSetControl &= !SE_DACL_PROTECTED;
    }
    else
    {
        lSetControl &= !SE_DACL_PROTECTED;
        lSetControl &= !SE_SACL_PROTECTED;
    }

    /*
    If there was change to the Control property, write it to the Security 
    Descriptor, write the SD to object, and then call SetInfo to write the 
    object to the directory.
    */
    if(lOriginalControl != lSetControl)
    {
        hr = spSD->put_Control(lSetControl);
        if(SUCCEEDED(hr))
        {
            hr = pObject->Put(sbstrAttribute, svar);
            if(SUCCEEDED(hr))
            {
                hr = pObject->SetInfo();
            }
        }
    }

    return hr;
}
```



 

 