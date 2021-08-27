---
description: Especifica el nivel de calidad para la codificación.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propiedad AVEncCommonQuality (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99202391e919fa1da9028a15a57154834feddd3039160b9b0562a713fe59ddaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087675"
---
# <a name="avenccommonquality-property"></a>Propiedad AVEncCommonQuality

Especifica el nivel de calidad para la codificación.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Value | Descripción                           |
|-------|---------------------------------------|
| 0     | Calidad mínima, tamaño de salida más pequeño. |
| 100   | Calidad máxima, tamaño de salida mayor.  |



 

## <a name="remarks"></a>Comentarios

Esta propiedad controla el nivel de calidad cuando el codificador no usa una velocidad de bits restringida. La [**propiedad AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina si la velocidad de bits está restringida.

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

 

 




