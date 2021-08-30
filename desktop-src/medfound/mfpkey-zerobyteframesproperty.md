---
description: Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373d0e7d40b27edff8ae47c9081ef6acb55252858a677c6516877fe88bee392c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953255"
---
# <a name="mfpkey_zerobyteframes-property"></a>Propiedad ZEROBYTEFRAMES de MFPKEY \_

Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCZeroByteFrames

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Este valor no se resta del número total de[fotogramas pasados (MFPKEY \_ TOTALFRAMES)](mfpkey-totalframesproperty.md)al calcular el número de fotogramas[codificados (MFPKEY \_ CODEDFRAMES).](mfpkey-codedframesproperty.md)

Puede impedir que el códec otee fotogramas duplicados estableciendo [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en VARIANT \_ TRUE.

Puede obtener este valor una vez que haya terminado de pasar ejemplos.

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

 

 




