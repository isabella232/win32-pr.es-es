---
title: Enlace al elemento primario de un objeto
description: En ADSI, cada objeto de directorio se representa mediante un objeto COM ADSI que expone la interfaz IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , using, enlace al elemento primario de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b47bfd71491c3eb0e8410f421630cec20255364b1cfc41bba7d6b48ba67fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180400"
---
# <a name="binding-to-an-objects-parent"></a>Enlace al elemento primario de un objeto

En ADSI, cada objeto de directorio se representa mediante un objeto COM ADSI que expone la [**interfaz IADs.**](/windows/desktop/api/Iads/nn-iads-iads) Para obtener el contenedor primario de un objeto , use el método [**IADs::get \_ Parent**](iads-property-methods.md) para obtener el ADsPath del objeto primario y, a continuación, enlace a ADsPath del elemento primario.

En el siguiente ejemplo de código de C++ se muestra cómo obtener el elemento primario de un objeto .


```C++
HRESULT GetParentObject(IADs *pObject,   // Pointer to the object whose parent to bind to.
                        IADs **ppParent) // Return a pointer to the parent object.
{
    if(NULL == ppParent)
    {
        return E_INVALIDARG;
    }
 
    *ppParent = NULL;

    if(NULL == pObject)
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    BSTR bstr;

    // Get the ADsPath of the parent.
    hr = pObject->get_Parent(&bstr);
    if(SUCCEEDED(hr))
    {
        // Bind to the parent.
        hr = ADsOpenObject(bstr,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)ppParent);

        SysFreeString(bstr);
    }

    return hr;
}
```



 

 




