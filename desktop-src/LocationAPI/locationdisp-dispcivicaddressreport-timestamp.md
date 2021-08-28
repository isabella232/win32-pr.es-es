---
description: 'Propiedad LocationDisp.DispCivicAddressReport.Timestamp: la fecha y hora en que se generó el informe.'
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Propiedad LocationDisp.DispCivicAddressReport.Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 12388706c0b8e9205f398ec259314ab05ff5fe1c062f4b8920d610b7d74b36f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129995"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>Propiedad LocationDisp.DispCivicAddressReport.Timestamp

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use el [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Fecha y hora en que se generó el informe.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es una fecha de solo **lectura.** Las marcas de tiempo se proporcionan como hora universal coordinada (UTC).

## <a name="remarks"></a>Comentarios

Tenga en cuenta que los lenguajes de scripting, como Microsoft JScript, pueden requerir que realice conversiones a otros formatos de tiempo al mostrar marcas de tiempo como cadenas.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

