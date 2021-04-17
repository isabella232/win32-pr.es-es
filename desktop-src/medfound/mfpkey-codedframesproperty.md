---
description: Especifica el número de fotogramas de vídeo codificados por el códec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Propiedad MFPKEY_CODEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667713"
---
# <a name="mfpkey_codedframes-property"></a>\_Propiedad CODEDFRAMES de MFPKEY

Especifica el número de fotogramas de vídeo codificados por el códec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Este valor es igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos cualquier fotograma que se haya quitado debido a restricciones de velocidad de bits. Puede obtener este valor después de haber terminado de pasar ejemplos.

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

 

 




