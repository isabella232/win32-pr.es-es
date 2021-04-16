---
description: Fecha y hora en que se generó el informe.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Propiedad LocationDisp. DispLatLongReport. timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5ec179c5958b1be73a5fd5f74e48d0063edb6696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678477"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>Propiedad LocationDisp. DispLatLongReport. timestamp

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Fecha y hora en que se generó el informe.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es una **fecha** de solo lectura. Las marcas de tiempo se proporcionan como hora universal coordinada (UTC).

## <a name="remarks"></a>Observaciones

Tenga en cuenta que los lenguajes de scripting, como Microsoft JScript, pueden requerir que realice conversiones a otros formatos de hora al mostrar las marcas de tiempo como cadenas.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

