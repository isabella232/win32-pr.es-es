---
description: Error de altitud, en metros.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Propiedad LocationDisp.DispLatLongReport.AltitudeError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d84c09a143808302a623ab7b098a105ef74ee4ad7aecfe3a4a172b765fcbdfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809532"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>Propiedad LocationDisp.DispLatLongReport.AltitudeError

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use el [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Error de altitud, en metros.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un número de solo **lectura** (punto flotante de precisión doble).

## <a name="remarks"></a>Comentarios

Los sensores de ubicación no son necesarios para proporcionar esta propiedad. Debe controlar las excepciones al intentar acceder a esta propiedad.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

