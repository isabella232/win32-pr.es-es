---
title: Enlazar al elemento primario de un objeto
description: En ADSI, cada objeto de directorio se representa mediante un objeto COM ADSI que expone la interfaz IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, enlazar con el elemento primario de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d72f3b3db3af9f13892494d3855dc5dcb2a74d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903076"
---
# <a name="binding-to-an-objects-parent"></a><span data-ttu-id="317de-104">Enlazar al elemento primario de un objeto</span><span class="sxs-lookup"><span data-stu-id="317de-104">Binding to an Object's Parent</span></span>

<span data-ttu-id="317de-105">En ADSI, cada objeto de directorio se representa mediante un objeto COM ADSI que expone la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="317de-105">In ADSI, every directory object is represented by an ADSI COM object that exposes the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="317de-106">Para obtener el contenedor primario de un objeto, use el método [**IADs:: get \_ Parent**](iads-property-methods.md) para obtener el ADsPath del objeto primario y, a continuación, enlace al ADsPath del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="317de-106">To obtain the parent container of an object, use the [**IADs::get\_Parent**](iads-property-methods.md) method to obtain the ADsPath of the parent object, then bind to the ADsPath of the parent.</span></span>

<span data-ttu-id="317de-107">En el ejemplo de código de C++ siguiente se muestra cómo obtener el elemento primario de un objeto.</span><span class="sxs-lookup"><span data-stu-id="317de-107">The following C++ code example shows how to obtain the parent of an object .</span></span>


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



 

 




