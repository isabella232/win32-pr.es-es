---
description: 'Propiedad LocationDisp.CivicAddressReportFactory.Status: el estado del informe actual.'
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Propiedad LocationDisp.CivicAddressReportFactory.Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ba7d9e26a9741f80caed84d2a4ee4198eae05736aa8dee91019452cc3345ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693125"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>Propiedad LocationDisp.CivicAddressReportFactory.Status

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Estado actual del informe.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un número de solo **lectura** (unsigned long).



| Status                                                                                               | Significado                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Informe no admitido.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Error.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Acceso denegado:<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | En ejecución.<br/>              |



 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

