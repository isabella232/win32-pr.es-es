---
description: Especifica si el códec debe utilizar la optimización perceptual conservadora al codificar.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Propiedad MFPKEY_PERCEPTUALOPTLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276310"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>\_Propiedad PERCEPTUALOPTLEVEL de MFPKEY

Especifica si el códec debe utilizar la optimización perceptual conservadora al codificar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

La optimización perceptual conservadora es un proceso por el cual el códec intenta identificar regiones "importantes" y "no importantes" en el fotograma de vídeo. Después de identificar estas regiones del fotograma, el códec dará una prioridad más alta a la calidad de las regiones importantes, a costa de la calidad de las regiones no importantes.

La optimización perceptual hace hincapié en hacer que la imagen parezca correcta para el ojo humano en lugar de insistir en una precisión matemática estricta.

Los resultados de la optimización variarán considerablemente según el tipo de vídeo que se está codificando. Esta característica puede ser adecuada para la codificación de baja velocidad y bajo nivel de bits (por ejemplo, transmisión por secuencias en Web), pero probablemente debe evitarse cuando se pretende tener una calidad de vídeo de archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




