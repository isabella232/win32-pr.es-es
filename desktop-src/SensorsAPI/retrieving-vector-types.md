---
description: Algunas propiedades y campos de datos contienen matrices de información.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Recuperar tipos de vectores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540894"
---
# <a name="retrieving-vector-types"></a>Recuperar tipos de vectores

Algunas propiedades y campos de datos contienen matrices de información. Por ejemplo, la propiedad de la \_ curva de respuesta ligera de la propiedad del sensor \_ \_ \_ contiene una matriz de enteros sin signo de 4 bytes. Sin embargo, cuando se reciben estas matrices a través de la API del sensor, siempre se representan como Type VT \_ Vector \| UI1, una matriz de caracteres de un solo byte, independientemente del tipo real de los datos de la matriz. Para estos tipos, debe tener cuidado de convertir variables de matriz al tipo de datos correcto para la propiedad o el campo de datos.

Para obtener información sobre las propiedades, los campos de datos y sus tipos, vea [constantes](constants.md).

En el ejemplo de código siguiente se muestra cómo convertir los datos recuperados en \_ la curva de respuesta de la luz de la propiedad del sensor \_ \_ \_ al tipo correcto.


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 



