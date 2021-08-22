---
description: Altitud actual, en metros. La altitud es relativa al elipsoide de referencia.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Propiedad LocationDisp.DispLatLongReport.Altitude
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
ms.openlocfilehash: 8ee6c2cd4257d7f7db97b89a5af4603f5c5129b7f07fe9bfbe6444bb9d347422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067945"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>Propiedad LocationDisp.DispLatLongReport.Altitude

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Altitud actual, en metros. La altitud es relativa al elipsoide de referencia.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un número de solo **lectura** (punto flotante de precisión doble).

## <a name="remarks"></a>Comentarios

Los sensores de ubicación no son necesarios para proporcionar esta propiedad. Debe controlar las excepciones al intentar acceder a esta propiedad.

El **método Altitude** recupera la altitud con respecto al elipsoide de referencia definido por la revisión más reciente del Sistema geodésico mundial (WGS 84), en lugar de la altitud con respecto al nivel del mar.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

