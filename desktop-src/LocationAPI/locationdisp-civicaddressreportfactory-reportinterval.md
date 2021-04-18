---
description: El intervalo de eventos del informe de dirección cívica actual en milisegundos.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Propiedad LocationDisp. CivicAddressReportFactory. ReportInterval
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
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688645"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Propiedad LocationDisp. CivicAddressReportFactory. ReportInterval

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

El intervalo de eventos del informe de dirección cívica actual en milisegundos.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es de lectura/escritura **ULong**.

## <a name="remarks"></a>Observaciones

Este valor es una solicitud para el proveedor de ubicación. No es necesario que el proveedor de ubicación proporcione informes en el intervalo solicitado. Lea el valor de esta propiedad para detectar la configuración de intervalo de informes real.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

