---
description: Altitud actual, en metros. La altitud es relativa al Elipsoide de referencia.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Propiedad LocationDisp. DispLatLongReport. altitud
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910097"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>Propiedad LocationDisp. DispLatLongReport. altitud

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Altitud actual, en metros. La altitud es relativa al Elipsoide de referencia.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).

## <a name="remarks"></a>Observaciones

No es necesario que los sensores de ubicación proporcionen esta propiedad. Debe controlar las excepciones al intentar tener acceso a esta propiedad.

El método **altitud** recupera la altitud en relación con la Elipsoide de referencia definida por la última revisión del sistema geodésico mundial (WGS 84), en lugar de la altitud relativa al nivel del mar.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

