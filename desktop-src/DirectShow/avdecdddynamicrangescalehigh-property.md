---
description: Especifica el corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Ac-3 de Dolby.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Propiedad AVDecDDDynamicRangeScaleHigh (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 725737b797d969d46293a9bf9e8f6d590e9fc51ac01d530fed6b8bc59c651629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103535"
---
# <a name="avdecdddynamicrangescalehigh-property"></a>Propiedad AVDecDDDynamicRangeScaleHigh

Especifica el corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Ac-3 de Dolby.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Value | Descripción                                                    |
|-------|----------------------------------------------------------------|
| 0     | Sin compresión de intervalo dinámico. Conserve el intervalo dinámico completo. |
| 100   | Aplique la compresión de intervalo dinámico completa.                          |



 

## <a name="remarks"></a>Comentarios

Esta propiedad solo se aplica cuando el valor de la propiedad [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) es eAVDecDDOperationalMode \_ LINE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




