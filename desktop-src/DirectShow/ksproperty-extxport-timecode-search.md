---
description: Esta propiedad envía un comando al dispositivo para buscar un código de tiempo especificado. El controlador de dispositivo UVC admite esta propiedad.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079930"
---
# <a name="ksproperty_extxport_timecode_search"></a>KSPROPERTY \_ \_ búsqueda de código de tiempo EXTXPORT \_

Esta propiedad envía un comando al dispositivo para buscar un código de tiempo especificado. El controlador de dispositivo UVC admite esta propiedad.



|                   |                                        |
|-------------------|----------------------------------------|
| GUID del conjunto de propiedades | \_transporte ext \_ PROPSETID              |
| Id. de propiedad       | KSPROPERTY \_ \_ búsqueda de código de tiempo EXTXPORT \_ |
| Tipo de datos         | **KSPROPERTY \_ Estructura EXTXPORT \_ S**  |



 

## <a name="remarks"></a>Observaciones

Rellene el miembro de **código de tiempo** de la estructura **KSPROPERTY \_ EXTXPORT \_ S** con el fotograma deseado, segundo, minuto y hora. La estructura **KSPROPERTY \_ EXTXPORT \_ S** se describe en el DDK de Windows.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjunto de propiedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



