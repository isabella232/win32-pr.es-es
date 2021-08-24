---
description: Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcf103da1d629c90209aef4badd604651d73af3e9101cac0f613b47c82883e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555425"
---
# <a name="mfpkey_numbframes-property"></a>Propiedad \_ MFPKEY DEFRAMES

Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Tipo de datos

VT-I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

De forma predeterminada, Windows Media Video 9 solo usa intraframes (fotogramas I), también conocidos como fotogramas clave o fotogramas delimitadores, que son fotogramas totalmente codificados, y fotogramas predictivos (fotogramas P), que se codifican como una diferencia con respecto al marco I anterior. Los fotogramas B son diferentes de los fotogramas P porque almacenan las diferencias con respecto al fotograma anterior y las diferencias con respecto al fotograma siguiente.

Al configurar el códec para que use fotogramas B, usará el número especificado de fotogramas B entre cada par de fotogramas del tipo I o P.

Por ejemplo, si una secuencia de fotogramas sin fotogramas B es "IPPPPPP PPP", la misma codificación de secuencia con dos fotogramas B sería "IBBPBBPBBI".

Para la mayoría del contenido, uno o dos fotogramas B son adecuados. A velocidades de datos más altas, una trama B suele ser la opción óptima. Tres o más son poco útiles.

El intervalo válido de valores para esta propiedad es de 0 a 7.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




