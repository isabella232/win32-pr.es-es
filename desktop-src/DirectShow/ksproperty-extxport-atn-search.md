---
description: Esta propiedad envía un comando al dispositivo para buscar un número de seguimiento absoluto (ATN). El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d35c1fce1e958aa475cc0344c2db320daa806326a49d0d6e939bf4ea86d49f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823275"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH

Esta propiedad envía un comando al dispositivo para buscar un número de seguimiento absoluto (ATN). El controlador de dispositivo UVC admite esta propiedad.



| Etiqueta | Value |
|-------------------|---------------------------------------|
| GUID del conjunto de propiedades | TRANSPORTE EXT DE PROPSETID \_ \_             |
| Id. de propiedad       | KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH     |
| Tipo de datos         | **KSPROPERTY \_ EXTXPORT \_ S (estructura)** |



 

## <a name="remarks"></a>Comentarios

Establezca el **miembro dwAbsTrackNumber** de la **estructura \_ EXTXPORT \_ S de KSPROPERTY** en el valor siguiente:


```
(absolute track number << 1) + continuity bit
```



La especificación UVC no define cómo el dispositivo usa el bit de continuidad. La **estructura \_ EXTXPORT \_ S de KSPROPERTY** se describe en el Windows DDK.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjunto de propiedades de transporte de dispositivos externos](external-device-transport-property-set.md)
</dt> </dl>

 

 



