---
description: Especifica el número de fotogramas de vídeo codificados por el códec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e836f2177311a2ffc13065187a1affce93c6dbe74ff9ff4c99ef78a6f492b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954735"
---
# <a name="mfpkey_codedframes-property"></a>Propiedad \_ CODEDFRAMES de MFPKEY

Especifica el número de fotogramas de vídeo codificados por el códec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Este valor es igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos los fotogramas que se han eliminado debido a restricciones de velocidad de bits. Puede obtener este valor una vez que haya terminado de pasar ejemplos.

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

 

 




