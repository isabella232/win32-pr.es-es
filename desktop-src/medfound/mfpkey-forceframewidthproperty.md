---
description: Especifica un ancho de marco intermedio para el vídeo codificado.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: Propiedad MFPKEY_FORCEFRAMEWIDTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544918"
---
# <a name="mfpkey_forceframewidth-property"></a>\_Propiedad FORCEFRAMEWIDTH de MFPKEY

Especifica un ancho de marco intermedio para el vídeo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede establecer este valor y la propiedad [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) para obligar al codificador a codificar el flujo de vídeo con un tamaño de fotograma menor que los tamaños de fotogramas de entrada o salida. Al descodificar, el vídeo cambiará de tamaño a su resolución de entrada original.

Las dimensiones de fotogramas válidas en cualquiera de los ejes son de 2 a 8192 píxeles. Las dimensiones del marco deben ser divisibles en 2.

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

 

 




