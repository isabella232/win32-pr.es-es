---
description: Solicita eventos del informe de direcciones cívica.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Método LocationDisp. CivicAddressReportFactory. ListenForReports (Locationapi. h)
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
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003053"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>LocationDisp. CivicAddressReportFactory. ListenForReports, método

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Solicita eventos del informe de direcciones cívica.

## <a name="syntax"></a>Sintaxis


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Número (**palabra doble**) que representa la hora solicitada entre eventos de informe de direcciones cívica, en milisegundos. Vea la sección Comentarios.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No es necesario que el proveedor de ubicación proporcione la precisión que se solicita. Lea el valor de la propiedad [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) para detectar la configuración de intervalo de informes real.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de direcciones cívica](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Encabezado<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento NewCivicAddressReport**](newcivicaddressreport.md)
</dt> </dl>

 

