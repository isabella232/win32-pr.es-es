---
description: El intervalo de eventos del informe de latitud y longitud actual en milisegundos.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Propiedad LocationDisp.LatLongReportFactory.ReportInterval
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
ms.openlocfilehash: d12ceab473ae9375a9a1a96ff28d5389cccf324f4a447f17df7c628a514dcf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386745"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>Propiedad LocationDisp.LatLongReportFactory.ReportInterval

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use el [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

El intervalo de eventos del informe de latitud y longitud actual en milisegundos.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un ULONG de **lectura y escritura.**

## <a name="remarks"></a>Comentarios

Este valor es una solicitud al proveedor de ubicación. No es necesario que el proveedor de ubicación proporcione informes en el intervalo que solicite. Lea el valor de esta propiedad para detectar la configuración del intervalo de informe verdadero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

