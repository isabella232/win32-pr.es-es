---
description: El intervalo de eventos de informe de latitud y longitud actual en milisegundos.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Propiedad LocationDisp. LatLongReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277378"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>Propiedad LocationDisp. LatLongReportFactory. ReportInterval

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

El intervalo de eventos de informe de latitud y longitud actual en milisegundos.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es de lectura/escritura **ULong**.

## <a name="remarks"></a>Observaciones

Este valor es una solicitud al proveedor de ubicación. No es necesario que el proveedor de ubicación proporcione informes en el intervalo que solicite. Lea el valor de esta propiedad para detectar la configuración de intervalo de informes real.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

