---
description: Se produce cuando se genera un nuevo informe de latitud y longitud.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Evento NewLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678601"
---
# <a name="newlatlongreport-event"></a>Evento NewLatLongReport

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Se produce cuando se genera un nuevo informe de latitud y longitud.

## <a name="syntax"></a>Sintaxis


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newReport* 
</dt> <dd>

El nuevo objeto [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este evento, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

