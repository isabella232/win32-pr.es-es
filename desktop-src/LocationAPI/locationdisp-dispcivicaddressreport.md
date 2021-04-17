---
description: Representa un informe de direcciones cívica.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Objeto LocationDisp. DispCivicAddressReport
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
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678036"
---
# <a name="locationdispdispcivicaddressreport-object"></a>Objeto LocationDisp. DispCivicAddressReport

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Representa un informe de direcciones cívica.

## <a name="members"></a>Miembros

El objeto **LocationDisp. DispCivicAddressReport** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **LocationDisp. DispCivicAddressReport** tiene estas propiedades.



| Propiedad                                                                              | Tipo de acceso          | Descripción                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Solo lectura<br/> | La primera línea de una dirección postal.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Solo lectura<br/> | La segunda línea de una dirección postal.<br/>             |
| [**Ciudad**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Solo lectura<br/> | El nombre de la ciudad.<br/>                                   |
| [**CountryRegion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Solo lectura<br/> | Nombre del país o la región.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Solo lectura<br/> | Nivel de detalle del informe.<br/>                 |
| [**CódPostal**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Solo lectura<br/> | El código postal.<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Solo lectura<br/> | El nombre de estado o provincia.<br/>                      |
| [**Indicaciones**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Solo lectura<br/> | Fecha y hora en que se generó el informe.<br/> |



 

## <a name="remarks"></a>Observaciones

Puede recuperar este objeto a través de la propiedad [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) de un objeto [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) . Puede recibir este objeto a través del evento [**NewCivicAddressReport**](newcivicaddressreport.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

