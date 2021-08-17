---
description: Se produce cuando se genera un nuevo informe de direcciones cívicos.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Evento NewCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 61b5c6c05d8aa551148d278fa0cbafa8791bbc4c1a1f6b1142ef7f2ef80af318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386750"
---
# <a name="newcivicaddressreport-event"></a>Evento NewCivicAddressReport

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Se produce cuando se genera un nuevo informe de direcciones cívicos.

## <a name="syntax"></a>Sintaxis


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newReport* 
</dt> <dd>

Nuevo objeto [**LocationDisp.DispCivicAddressReport.**](locationdisp-dispcivicaddressreport.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este evento, vea [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

