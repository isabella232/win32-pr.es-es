---
description: Algunas propiedades y campos de datos contienen matrices de información.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Recuperar tipos de vectores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15579d7067d0eafba0d181d8e8845dfa1bd78b060fb5fba8b08f196d2107d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739465"
---
# <a name="retrieving-vector-types"></a>Recuperar tipos de vectores

Algunas propiedades y campos de datos contienen matrices de información. Por ejemplo, la propiedad SENSOR PROPERTY LIGHT RESPONSE CURVE contiene una matriz de \_ \_ \_ \_ enteros de 4 bytes sin signo. Sin embargo, cuando recibe estas matrices a través de sensor API, siempre se representan como tipo VT VECTOR UI1, una matriz de caracteres de un solo byte, independientemente del tipo real de los datos de la \_ \| matriz. Para estos tipos, debe tener cuidado de convertir variables de matriz al tipo de datos correcto para la propiedad o el campo de datos.

Para obtener información sobre las propiedades, los campos de datos y sus tipos, vea [Constantes](constants.md).

En el código de ejemplo siguiente se muestra cómo convertir los datos recuperados en SENSOR \_ PROPERTY LIGHT RESPONSE CURVE al tipo \_ \_ \_ correcto.


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



 

 



