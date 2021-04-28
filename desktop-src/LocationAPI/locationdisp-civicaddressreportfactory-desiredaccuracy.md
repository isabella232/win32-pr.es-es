---
description: 'Propiedad LocationDisp.CivicAddressReportFactory.DesiredAccuracy: el valor actual de precisión deseada.'
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Propiedad LocationDisp.CivicAddressReportFactory.DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a18a363c2f24e9b17e16064b7375a4f075a1a8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110923"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>Propiedad LocationDisp.CivicAddressReportFactory.DesiredAccuracy

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Valor actual de precisión deseada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un ULONG de **lectura y escritura.**



| Valor                                                                        | Significado                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Predeterminada. El sensor debe usar la precisión para la que puede optimizar el uso de energía y otras consideraciones de costos.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | El sensor debe proporcionar el informe más preciso posible. Para ello, pueden usarse servicios que no son gratuitos o aumentar el consumo de energía de la batería o del ancho de banda de la conexión.<br/> |



 

## <a name="remarks"></a>Comentarios

Este valor es una solicitud al proveedor de ubicación. El proveedor de ubicación no es necesario para proporcionar la precisión que se solicita. Lea el valor de esta propiedad para detectar la configuración de precisión verdadera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

