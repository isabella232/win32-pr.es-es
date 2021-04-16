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
# <a name="retrieving-vector-types"></a><span data-ttu-id="ec02e-103">Recuperar tipos de vectores</span><span class="sxs-lookup"><span data-stu-id="ec02e-103">Retrieving Vector Types</span></span>

<span data-ttu-id="ec02e-104">Algunas propiedades y campos de datos contienen matrices de información.</span><span class="sxs-lookup"><span data-stu-id="ec02e-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="ec02e-105">Por ejemplo, la propiedad de la \_ curva de respuesta ligera de la propiedad del sensor \_ \_ \_ contiene una matriz de enteros sin signo de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="ec02e-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="ec02e-106">Sin embargo, cuando se reciben estas matrices a través de la API del sensor, siempre se representan como Type VT \_ Vector \| UI1, una matriz de caracteres de un solo byte, independientemente del tipo real de los datos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="ec02e-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="ec02e-107">Para estos tipos, debe tener cuidado de convertir variables de matriz al tipo de datos correcto para la propiedad o el campo de datos.</span><span class="sxs-lookup"><span data-stu-id="ec02e-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="ec02e-108">Para obtener información sobre las propiedades, los campos de datos y sus tipos, vea [constantes](constants.md).</span><span class="sxs-lookup"><span data-stu-id="ec02e-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="ec02e-109">En el ejemplo de código siguiente se muestra cómo convertir los datos recuperados en \_ la curva de respuesta de la luz de la propiedad del sensor \_ \_ \_ al tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="ec02e-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


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



 

 



