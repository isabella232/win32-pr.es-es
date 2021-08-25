---
description: En C++, cada método de Servicios de certificados devuelve directamente un valor HRESULT que indica si la llamada al método se ha hecho correctamente o no. Si la llamada no se ha podido llamar, el valor devuelto indica por qué se ha fallado.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Comprobación de errores en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e374c6f0bd933c2e4de7a477fea02b4e1538a7a1fa9b4de78e45fd896b192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874075"
---
# <a name="error-checking-in-c"></a>Comprobación de errores en C++

En C++, cada método de Servicios de certificados devuelve directamente un **valor HRESULT** que indica si la llamada al método se ha hecho correctamente o no. Si la llamada no se ha podido llamar, el valor devuelto indica por qué se ha fallado.

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



 

 



