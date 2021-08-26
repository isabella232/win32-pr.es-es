---
description: Especifica si el códec debe usar la optimización perceptual conservadora al codificar.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f9eb74ae025dbddbdea7f76c2af8b15e912cf80ebd06e810a5214bf9798d1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953855"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>Propiedad \_ PERCEPTUALOPTLEVEL de MFPKEY

Especifica si el códec debe usar la optimización perceptual conservadora al codificar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

La optimización perceptual conservadora es un proceso por el que el códec intenta identificar regiones "importantes" y "no importantes" en el fotograma de vídeo. Después de identificar estas regiones del marco, el códec dará una prioridad más alta a la calidad de las regiones importantes, a costa de la calidad de las regiones no importantes.

La optimización perceptual hace que la imagen parezca correcta para el ojo humano en lugar de insospecar una precisión matemática estricta.

Los resultados de la optimización variarán considerablemente en función del tipo de vídeo que se va a codificar. Esta característica podría ser adecuada para codificación de baja velocidad de bits y baja resolución (por ejemplo, streaming web), pero probablemente se debe evitar al apuntar a la calidad del vídeo de archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




