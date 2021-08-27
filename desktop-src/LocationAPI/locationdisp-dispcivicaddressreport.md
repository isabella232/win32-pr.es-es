---
description: Representa un informe de direcciones cívicos.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Objeto LocationDisp.DispCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5646bd6df1a2523faf481bc867acc67dbd0a647b4cdf3f033d7327a66174d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129985"
---
# <a name="locationdispdispcivicaddressreport-object"></a>Objeto LocationDisp.DispCivicAddressReport

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Representa un informe de direcciones cívicos.

## <a name="members"></a>Miembros

El **objeto LocationDisp.DispCivicAddressReport** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto LocationDisp.DispCivicAddressReport** tiene estas propiedades.



| Propiedad                                                                              | Tipo de acceso          | Descripción                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Solo lectura<br/> | Primera línea de una dirección postal.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Solo lectura<br/> | Segunda línea de una dirección postal.<br/>             |
| [**City (Ciudad)**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Solo lectura<br/> | Nombre de la ciudad.<br/>                                   |
| [**CountryRegion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Solo lectura<br/> | Nombre del país o región.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Solo lectura<br/> | Nivel de detalle del informe.<br/>                 |
| [**PostalCode**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Solo lectura<br/> | El código postal.<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Solo lectura<br/> | Nombre del estado o provincia.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Solo lectura<br/> | Fecha y hora en que se generó el informe.<br/> |



 

## <a name="remarks"></a>Comentarios

Puede recuperar este objeto a través de la [**propiedad CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) de un [**objeto CivicAddressReportFactory.**](locationdisp-civicaddressreportfactory.md) Puede recibir este objeto a través del [**evento NewCivicAddressReport.**](newcivicaddressreport.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

