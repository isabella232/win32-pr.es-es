---
description: Error de altitud, en metros.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Propiedad LocationDisp. DispLatLongReport. AltitudeError
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
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910990"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>Propiedad LocationDisp. DispLatLongReport. AltitudeError

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Error de altitud, en metros.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).

## <a name="remarks"></a>Observaciones

No es necesario que los sensores de ubicación proporcionen esta propiedad. Debe controlar las excepciones al intentar tener acceso a esta propiedad.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

