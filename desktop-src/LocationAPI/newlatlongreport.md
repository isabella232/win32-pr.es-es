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
ms.openlocfilehash: 3cc8a46267927aaf7bf3011acbd05a32244fd0dcd8cc354a2bde1a299aaca624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129805"
---
# <a name="newlatlongreport-event"></a>Evento NewLatLongReport

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

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

Nuevo objeto [**LocationDisp.DispLatLongReport.**](locationdisp-displatlongreport.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este evento, vea [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

