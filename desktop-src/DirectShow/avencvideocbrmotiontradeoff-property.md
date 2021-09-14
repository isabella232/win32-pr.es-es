---
description: Especifica el equilibrio entre el movimiento y las imágenes fijas. Esta propiedad solo se aplica al modo de control de velocidad de bits constante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propiedad AVEncVideoCBRMotionMotionMotionOff (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161797"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>Propiedad AVEncVideoCBRMotionMotionMotionOff

Especifica el equilibrio entre el movimiento y las imágenes fijas. Esta propiedad solo se aplica al modo de control de velocidad de bits constante (CBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoCBRMotionMotionOff**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Value | Descripción               |
|-------|---------------------------|
| 0     | Optimización de imágenes fijas |
| 100   | Optimización del movimiento.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




