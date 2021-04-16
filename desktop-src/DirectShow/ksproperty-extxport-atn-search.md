---
description: Esta propiedad envía un comando al dispositivo para buscar un número de pista absoluta (ATN). El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686276"
---
# <a name="ksproperty_extxport_atn_search"></a>búsqueda de KSPROPERTY \_ EXTXPORT \_ ATN \_

Esta propiedad envía un comando al dispositivo para buscar un número de pista absoluta (ATN). El controlador de dispositivo UVC admite esta propiedad.



|                   |                                       |
|-------------------|---------------------------------------|
| GUID del conjunto de propiedades | \_transporte ext \_ PROPSETID             |
| Id. de propiedad       | búsqueda de KSPROPERTY \_ EXTXPORT \_ ATN \_     |
| Tipo de datos         | **KSPROPERTY \_ Estructura EXTXPORT \_ S** |



 

## <a name="remarks"></a>Observaciones

Establezca el miembro **dwAbsTrackNumber** de la estructura **KSPROPERTY \_ EXTXPORT \_ S** en el siguiente valor:


```
(absolute track number << 1) + continuity bit
```



La especificación UVC no define el modo en que el dispositivo usa el bit de continuidad. La estructura **KSPROPERTY \_ EXTXPORT \_ S** se describe en el DDK de Windows.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjunto de propiedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



