---
description: Especifica si el códec debe usar la optimización perceptual conservadora al codificar.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268839"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>Propiedad PERCEPTUALOPTLEVEL de MFPKEY \_

Especifica si el códec debe usar la optimización perceptual conservadora al codificar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

La optimización perceptual conservadora es un proceso por el que el códec intenta identificar regiones "importantes" y "no importantes" en el fotograma de vídeo. Después de identificar estas regiones del marco, el códec dará una prioridad más alta a la calidad de las regiones importantes, a costa de la calidad de las regiones no importantes.

La optimización perceptual hace hincapié en hacer que la imagen parezca correcta para el ojo humano en lugar de fírsela en una precisión matemática estricta.

Los resultados de la optimización variarán considerablemente en función del tipo de vídeo que se esté codificando. Esta característica podría ser adecuada para una codificación de baja velocidad de bits y baja resolución (por ejemplo, streaming web), pero probablemente se debe evitar al apuntar a la calidad del vídeo de archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




