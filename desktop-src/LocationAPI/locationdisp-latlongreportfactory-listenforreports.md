---
description: Solicita eventos de informe de latitud y longitud.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Método LocationDisp. LatLongReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814806"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a>LocationDisp. LatLongReportFactory. ListenForReports, método

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Solicita eventos de informe de latitud y longitud.

## <a name="syntax"></a>Sintaxis


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Número (**palabra doble**) que representa el tiempo solicitado entre los eventos de informe de latitud y longitud, en milisegundos. Vea la sección Comentarios.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No es necesario que el proveedor de ubicación proporcione informes en el intervalo que solicite. Lea el valor de la propiedad [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) para detectar la configuración de intervalo de informes real.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Encabezado<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



 

