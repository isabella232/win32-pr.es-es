---
description: Esta propiedad envía un comando al dispositivo para buscar un código de hora especificado. El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f49b8e71d664cf266428d33c99b87859765623ca8205843bbfee108da5f7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153193"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH

Esta propiedad envía un comando al dispositivo para buscar un código de hora especificado. El controlador de dispositivo UVC admite esta propiedad.



| Etiqueta | Valor |
|-------------------|----------------------------------------|
| GUID del conjunto de propiedades | TRANSPORTE EXT DE PROPSETID \_ \_              |
| Id. de propiedad       | KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH |
| Tipo de datos         | **KSPROPERTY \_ EXTXPORT \_ S (estructura)**  |



 

## <a name="remarks"></a>Comentarios

Rellene el miembro **Timecode de** la estructura **\_ EXTXPORT \_ S de KSPROPERTY** con el marco, el segundo, el minuto y la hora deseados. La **estructura \_ EXTXPORT \_ S de KSPROPERTY** se describe en el Windows DDK.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjunto de propiedades de transporte de dispositivos externos](external-device-transport-property-set.md)
</dt> </dl>

 

 



