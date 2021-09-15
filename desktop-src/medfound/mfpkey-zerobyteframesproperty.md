---
description: Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: MFPKEY_ZEROBYTEFRAMES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468604"
---
# <a name="mfpkey_zerobyteframes-property"></a>Propiedad ZEROBYTEFRAMES de MFPKEY \_

Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCZeroByteFrames

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Este valor no se resta del número total de[ \_ fotogramas pasados (TOTALFRAMES de MFPKEY)](mfpkey-totalframesproperty.md)al calcular el número de fotogramas[codificados (MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).

Puede impedir que el códec otee fotogramas duplicados estableciendo [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en VARIANT \_ TRUE.

Puede obtener este valor una vez que haya terminado de pasar ejemplos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




