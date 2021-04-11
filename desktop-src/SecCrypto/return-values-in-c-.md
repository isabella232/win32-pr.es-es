---
description: En C++, el valor devuelto suele ser de tipo HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Valores devueltos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276801"
---
# <a name="return-values-in-c"></a>Valores devueltos en C++

En C++, el valor devuelto suele ser de tipo **HRESULT**. Es de este valor devuelto que se puede determinar si el método se realizó correctamente o no, y si no es así, cuál fue el error. Los servicios de Certificate Server normalmente devuelven \_ los valores correctos para **HRESULT** cuando el método se ha completado correctamente. Los valores de programación que se deben devolver se devuelven a través de los parámetros "out" en el método. En el ejemplo siguiente se muestra una llamada al método de C++ para recuperar una propiedad de solicitud:


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



En el fragmento de código anterior, se devuelve SUCCESS o Failure a la variable **HRESULT** , *HR*. Es imperativo comprobar que la variable **HRESULT** se ha \[ controlado correctamente en el código por la condición (S \_ OK! = hr) \] . Si el método se completó correctamente, el valor de la propiedad de solicitud se devuelve en el parámetro **Variant** *varProp* .

 

 



