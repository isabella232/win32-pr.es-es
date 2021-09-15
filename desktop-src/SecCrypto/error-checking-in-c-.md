---
description: En C++, cada método de Servicios de certificados devuelve directamente un valor HRESULT que indica si la llamada al método se ha hecho correctamente o no. Si la llamada no se pudo hacer, el valor devuelto indica por qué se ha podido.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Comprobación de errores en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476407"
---
# <a name="error-checking-in-c"></a>Comprobación de errores en C++

En C++, cada método de Servicios de certificados devuelve directamente un **valor HRESULT** que indica si la llamada al método se ha hecho correctamente o no. Si la llamada no se pudo hacer, el valor devuelto indica por qué se ha podido.

En el ejemplo siguiente se muestra cómo se pueden usar **los valores HRESULT** devueltos para la comprobación de errores. Para obtener códigos de error de ejemplo, [vea Common HRESULT Values](common-hresult-values.md).


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



 

 



