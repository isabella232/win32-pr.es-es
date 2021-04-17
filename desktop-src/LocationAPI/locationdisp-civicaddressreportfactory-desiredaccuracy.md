---
description: Valor de precisión deseado actual.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Propiedad LocationDisp. CivicAddressReportFactory. DesiredAccuracy
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
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669855"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>Propiedad LocationDisp. CivicAddressReportFactory. DesiredAccuracy

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Valor de precisión deseado actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es de lectura/escritura **ULong**.



| Value                                                                        | Significado                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Predeterminada. El sensor debe utilizar la precisión para la que puede optimizar el uso de energía y otras consideraciones de costo.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | El sensor debe proporcionar el informe más preciso posible. Para ello, pueden usarse servicios que no son gratuitos o aumentar el consumo de energía de la batería o del ancho de banda de la conexión.<br/> |



 

## <a name="remarks"></a>Observaciones

Este valor es una solicitud al proveedor de ubicación. No es necesario que el proveedor de ubicación proporcione la precisión que se solicita. Lea el valor de esta propiedad para detectar la configuración de precisión verdadera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

