---
description: Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Ac-3 de Dolby.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Propiedad AVDecDDDynamicRangeScaleLow (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91773eb20f3d0714223877acba4f26b01503202fc87f9f7b97dcde60ab99512e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586745"
---
# <a name="avdecdddynamicrangescalelow-property"></a>Propiedad AVDecDDDynamicRangeScaleLow

Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Ac-3 de Dolby.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecDDDynamicRangeScaleLow**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Valor | Descripción                                                    |
|-------|----------------------------------------------------------------|
| 0     | Sin compresión de intervalo dinámico. Conserve el intervalo dinámico completo. |
| 100   | Aplique la compresión de intervalo dinámico completa.                          |



 

## <a name="remarks"></a>Comentarios

Esta propiedad solo se aplica cuando el valor de la propiedad [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) es eAVDecDDOperationalMode \_ LINE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




