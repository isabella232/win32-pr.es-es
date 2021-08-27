---
description: 'Propiedad LocationDisp.LatLongReportFactory.DesiredAccuracy: el valor actual de precisión deseada.'
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Propiedad LocationDisp.LatLongReportFactory.DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3deccb2dcc71a62b64a508e55759e5cc9c00b5cb0a7a59fb3390046371d2fac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129855"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>Propiedad LocationDisp.LatLongReportFactory.DesiredAccuracy

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Valor actual de precisión deseada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un ULONG de **lectura y escritura.**



| Value                                                                        | Significado                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Predeterminada. El sensor debe usar la precisión para la que puede optimizar el uso de energía y otras consideraciones de costos.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | El sensor debe proporcionar el informe más preciso posible. Para ello, pueden usarse servicios que no son gratuitos o aumentar el consumo de energía de la batería o del ancho de banda de la conexión.<br/> |



 

## <a name="remarks"></a>Comentarios

Este valor es una solicitud al proveedor de ubicación. No es necesario que el proveedor de ubicación proporcione informes en el intervalo solicitado. Lea el valor de esta propiedad para detectar la configuración verdadera del intervalo de informe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

