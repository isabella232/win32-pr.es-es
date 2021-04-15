---
description: Representa un informe de latitud y longitud.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Objeto LocationDisp. DispLatLongReport
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
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688640"
---
# <a name="locationdispdisplatlongreport-object"></a>Objeto LocationDisp. DispLatLongReport

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Representa un informe de latitud y longitud.

## <a name="members"></a>Miembros

El objeto **LocationDisp. DispLatLongReport** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **LocationDisp. DispLatLongReport** tiene estas propiedades.



| Propiedad                                                                         | Tipo de acceso          | Descripción                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Altitud**](locationdisp-displatlongreport-altitude.md)<br/>           | Solo lectura<br/> | Altitud actual, en metros.<br/>                                                                                                                                                           |
| [**AltitudeError**](locationdisp-displatlongreport-altitudeerror.md)<br/> | Solo lectura<br/> | Error de altitud, en metros.<br/>                                                                                                                                                             |
| [**ErrorRadius**](locationdisp-displatlongreport-errorradius.md)<br/>     | Solo lectura<br/> | Distancia desde la ubicación indicada, en metros. Combinado con la ubicación indicada como origen, este radio describe el círculo en el que se encuentra la ubicación real Proably.<br/> |
| [**Latitud**](locationdisp-displatlongreport-latitude.md)<br/>           | Solo lectura<br/> | Latitud actual, en grados.<br/>                                                                                                                                                          |
| [**Longitud**](locationdisp-displatlongreport-longitude.md)<br/>         | Solo lectura<br/> | Longitud actual, en grados.<br/>                                                                                                                                                         |
| [**Indicaciones**](locationdisp-displatlongreport-timestamp.md)<br/>         | Solo lectura<br/> | Fecha y hora en que se generó el informe.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Puede recuperar este objeto a través de la propiedad [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) del objeto [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) . Puede recibir este objeto a través del evento [**NewLatLongReport**](newlatlongreport.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

