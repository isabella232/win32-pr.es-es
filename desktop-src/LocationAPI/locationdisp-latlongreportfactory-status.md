---
description: 'Propiedad LocationDisp.LatLongReportFactory.Status: el estado del informe actual.'
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Propiedad LocationDisp.LatLongReportFactory.Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088903"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a>Propiedad LocationDisp.LatLongReportFactory.Status

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Estado actual del informe.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un número de solo **lectura** (unsigned long).



| Status                                                                                               | Significado                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Informe no admitido.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Error.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Acceso denegado.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | En ejecución.<br/>              |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

