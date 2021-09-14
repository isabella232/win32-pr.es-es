---
description: Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268887"
---
# <a name="mfpkey_numbframes-property"></a>Propiedad \_ MFPKEY DEFRAMES

Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Tipo de datos

VT-I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

De forma predeterminada, Windows Media Video 9 solo usa intraframes (fotogramas I), también conocidos como fotogramas clave o fotogramas delimitadores, que son fotogramas totalmente codificados, y fotogramas predictivos (fotogramas P), que se codifican como una diferencia con respecto al marco I anterior. Los fotogramas B son diferentes de los fotogramas P porque almacenan las diferencias con respecto al fotograma anterior y las diferencias con respecto al fotograma siguiente.

Al configurar el códec para que use fotogramas B, usará el número especificado de fotogramas B entre cada par de fotogramas del tipo I o P.

Por ejemplo, si una secuencia de fotogramas sin fotogramas B es "IPPPPPP PPP", la misma codificación de secuencia con dos fotogramas B sería "IBBPBBPBBI".

Para la mayoría del contenido, uno o dos fotogramas B son adecuados. A velocidades de datos más altas, una trama B suele ser la opción óptima. Tres o más son poco útiles.

El intervalo válido de valores para esta propiedad es de 0 a 7.

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

 

 




