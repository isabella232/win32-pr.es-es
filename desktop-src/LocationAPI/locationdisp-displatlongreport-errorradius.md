---
description: Distancia desde la ubicación indicada, en metros. Combinado con la ubicación indicada como origen, este radio describe el círculo en el que probablemente se encuentra la ubicación real.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: Propiedad LocationDisp. DispLatLongReport. ErrorRadius
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687702"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a>Propiedad LocationDisp. DispLatLongReport. ErrorRadius

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Distancia desde la ubicación indicada, en metros. Combinado con la ubicación indicada como origen, este radio describe el círculo en el que probablemente se encuentra la ubicación real.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

