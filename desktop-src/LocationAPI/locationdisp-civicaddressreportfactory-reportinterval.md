---
description: El intervalo de eventos del informe de direcciones cívicos actual en milisegundos.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Propiedad LocationDisp.CivicAddressReportFactory.ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387166"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Propiedad LocationDisp.CivicAddressReportFactory.ReportInterval

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use el [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

El intervalo de eventos del informe de direcciones cívicos actual en milisegundos.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un ULONG de **lectura y escritura.**

## <a name="remarks"></a>Comentarios

Este valor es una solicitud para el proveedor de ubicación. No es necesario que el proveedor de ubicación proporcione informes en el intervalo solicitado. Lea el valor de esta propiedad para detectar la configuración del intervalo de informe verdadero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

