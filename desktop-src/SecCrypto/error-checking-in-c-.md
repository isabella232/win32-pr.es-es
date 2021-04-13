---
description: En C++, cada método de servicios de certificados devuelve directamente un valor HRESULT que indica si la llamada al método se realizó correctamente o no. Si se produce un error en la llamada, el valor devuelto indica por qué se produjo un error.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Comprobación de errores en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544982"
---
# <a name="error-checking-in-c"></a><span data-ttu-id="875f6-104">Comprobación de errores en C++</span><span class="sxs-lookup"><span data-stu-id="875f6-104">Error Checking in C++</span></span>

<span data-ttu-id="875f6-105">En C++, cada método de servicios de certificados devuelve directamente un valor **HRESULT** que indica si la llamada al método se realizó correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="875f6-105">In C++, every Certificate Services method directly returns an **HRESULT** value that indicates whether the method call succeeded or failed.</span></span> <span data-ttu-id="875f6-106">Si se produce un error en la llamada, el valor devuelto indica por qué se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="875f6-106">If the call failed, the return value indicates why it failed.</span></span>

<span data-ttu-id="875f6-107">En el ejemplo siguiente se muestra cómo se pueden usar los valores **HRESULT** devueltos para la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="875f6-107">The following example shows how the returned **HRESULT** values can be used for error checking.</span></span> <span data-ttu-id="875f6-108">Para ver ejemplos de códigos de error, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="875f6-108">For example error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>


```C++
HRESULT hr;
BSTR strAttributeName;
BSTR strAttributeValue = NULL;

if(!(strAttributeName = SysAllocString(L"TheAttribute")))
{
     printf("Could not allocate memory for attribute name.\n");
     exit(1);
}

hr = pICertServerPolicy->GetRequestAttribute(
                                strAttributeName,
                                &strAttributeValue);
if(S_OK != hr)          // Check to determine whether method failed
{
    if (E_INVALIDARG == hr)
    {
        //... Do something to recover from errors and so on.
    }
}
// Free BSTRs when finished.
if (NULL != strAttributeName)
    SysFreeString(strAttributeName);
if (NULL != strAttributeValue)
    SysFreeString(strAttributeValue);
```



 

 



