---
description: Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Propiedad MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648305"
---
# <a name="mfpkey_numbframes-property"></a>\_Propiedad NUMBFRAMES de MFPKEY

Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Tipo de datos

VT-I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

De forma predeterminada, Windows Media Video 9 solo utiliza intragramas (fotogramas I), también conocidos como fotogramas clave o fotogramas delimitadores, que son fotogramas totalmente codificados, y marcos de predicción (fotogramas P), que se codifican como una diferencia respecto del fotograma I anterior. Los fotogramas B son diferentes de los fotogramas P porque almacenan las diferencias con respecto al fotograma anterior y las diferencias con el siguiente fotograma.

Al configurar el códec para que use fotogramas B, usará el número especificado de fotogramas B entre cada par de fotogramas de tipo I o P.

Por ejemplo, si una secuencia de marcos sin fotogramas B es "IPPPPPPPPI", la misma codificación de secuencia con dos fotogramas B sería "IBBPBBPBBI".

Para la mayoría del contenido, uno o dos fotogramas B son adecuados. Con una velocidad de datos superior, un fotograma B suele ser la opción óptima. Tres o más no suelen ser útiles.

El intervalo válido de valores para esta propiedad es de 0 a 7.

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

 

 




