---
description: Solicita eventos de informe de direcciones cívicos.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Método LocationDisp.CivicAddressReportFactory.ListenForReports (Locationapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 218684dcdb1c79b3b1a37517a4369ad492031cae1badfb9f0b16bbb6933289d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979775"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>Método LocationDisp.CivicAddressReportFactory.ListenForReports

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Solicita eventos de informe de direcciones cívicos.

## <a name="syntax"></a>Sintaxis


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Número **(palabra doble) que** representa el tiempo solicitado entre eventos de informe de direcciones cívicos, en milisegundos. Vea la sección Comentarios.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El proveedor de ubicación no es necesario para proporcionar la precisión que se solicita. Lea el valor de la [**propiedad ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) para detectar la configuración verdadera del intervalo de informe.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Header<br/>                   | <dl> <dt>Locationapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento NewCivicAddressReport**](newcivicaddressreport.md)
</dt> </dl>

 

