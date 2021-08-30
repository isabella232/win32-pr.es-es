---
description: Representa un informe de latitud y longitud.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Objeto LocationDisp.DispLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: af6d0df9dfa3bec9249cb2e55cb34dc552ce6a19be26495430a8d602a4427da1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129875"
---
# <a name="locationdispdisplatlongreport-object"></a>Objeto LocationDisp.DispLatLongReport

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use el [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Representa un informe de latitud y longitud.

## <a name="members"></a>Miembros

El **objeto LocationDisp.DispLatLongReport** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto LocationDisp.DispLatLongReport** tiene estas propiedades.



| Propiedad                                                                         | Tipo de acceso          | Descripción                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Altitud**](locationdisp-displatlongreport-altitude.md)<br/>           | Solo lectura<br/> | Altitud actual, en metros.<br/>                                                                                                                                                           |
| [**Error de altitud**](locationdisp-displatlongreport-altitudeerror.md)<br/> | Solo lectura<br/> | Error de altitud, en metros.<br/>                                                                                                                                                             |
| [**ErrorRadius**](locationdisp-displatlongreport-errorradius.md)<br/>     | Solo lectura<br/> | Distancia desde la ubicación notificada, en metros. Combinado con la ubicación notificada como origen, este radio describe el círculo en el que se encuentra la ubicación real.<br/> |
| [**Latitud**](locationdisp-displatlongreport-latitude.md)<br/>           | Solo lectura<br/> | Latitud actual, en grados.<br/>                                                                                                                                                          |
| [**Longitud**](locationdisp-displatlongreport-longitude.md)<br/>         | Solo lectura<br/> | Longitud actual, en grados.<br/>                                                                                                                                                         |
| [**Timestamp**](locationdisp-displatlongreport-timestamp.md)<br/>         | Solo lectura<br/> | Fecha y hora en que se generó el informe.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentarios

Puede recuperar este objeto a través de [**la propiedad LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) del [**objeto LatLongReportFactory.**](locationdisp-latlongreportfactory.md) Puede recibir este objeto a través del [**evento NewLatLongReport.**](newlatlongreport.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

