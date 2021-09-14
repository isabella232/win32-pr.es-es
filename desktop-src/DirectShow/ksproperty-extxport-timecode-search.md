---
description: Esta propiedad envía un comando al dispositivo para buscar un código de hora especificado. El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061040"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH

Esta propiedad envía un comando al dispositivo para buscar un código de hora especificado. El controlador de dispositivo UVC admite esta propiedad.



| Etiqueta | Value |
|-------------------|----------------------------------------|
| GUID del conjunto de propiedades | TRANSPORTE EXT DE PROPSETID \_ \_              |
| Id. de propiedad       | KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH |
| Tipo de datos         | **KSPROPERTY \_ EXTXPORT \_ S (estructura)**  |



 

## <a name="remarks"></a>Observaciones

Rellene el miembro **Timecode de** la estructura **\_ EXTXPORT \_ S de KSPROPERTY** con el marco, el segundo, el minuto y la hora deseados. La **estructura \_ EXTXPORT \_ S de KSPROPERTY** se describe en el Windows DDK.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Conjunto de propiedades de transporte de dispositivos externos](external-device-transport-property-set.md)
</dt> </dl>

 

 



