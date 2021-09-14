---
description: Esta propiedad envía un comando al dispositivo para buscar un número de seguimiento absoluto (ATN). El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061042"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH

Esta propiedad envía un comando al dispositivo para buscar un número de seguimiento absoluto (ATN). El controlador de dispositivo UVC admite esta propiedad.



| Etiqueta | Value |
|-------------------|---------------------------------------|
| GUID del conjunto de propiedades | TRANSPORTE EXT DE PROPSETID \_ \_             |
| Id. de propiedad       | KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH     |
| Tipo de datos         | **KSPROPERTY \_ EXTXPORT \_ S (estructura)** |



 

## <a name="remarks"></a>Observaciones

Establezca el **miembro dwAbsTrackNumber** de la **estructura \_ EXTXPORT \_ S de KSPROPERTY** en el valor siguiente:


```
(absolute track number << 1) + continuity bit
```



La especificación UVC no define cómo el dispositivo usa el bit de continuidad. La **estructura \_ EXTXPORT \_ S de KSPROPERTY** se describe en el Windows DDK.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Conjunto de propiedades de transporte de dispositivos externos](external-device-transport-property-set.md)
</dt> </dl>

 

 



