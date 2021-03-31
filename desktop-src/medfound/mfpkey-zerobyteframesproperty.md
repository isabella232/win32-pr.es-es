---
description: Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Propiedad MFPKEY_ZEROBYTEFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908382"
---
# <a name="mfpkey_zerobyteframes-property"></a>\_Propiedad ZEROBYTEFRAMES de MFPKEY

Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCZeroByteFrames

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Este valor no se resta del número total de fotogramas pasados ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) al calcular el número de fotogramas codificados ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).

Puede impedir que el códec omita fotogramas duplicados estableciendo [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en Variant \_ true.

Puede obtener este valor después de haber terminado de pasar ejemplos.

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

 

 




