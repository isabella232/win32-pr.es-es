---
description: Especifica el nivel de volumen medio deseado del contenido de audio de salida.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Propiedad MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276228"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>\_ \_ Propiedad AVGTARGET de MFPKEY WMADRC

Especifica el nivel de volumen medio deseado del contenido de audio de salida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

Vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

Puede establecer este valor en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .

> [!Note]  
> No se recomienda establecer el valor de destino medio. El ajuste del valor medio no afecta a la diferencia entre los sonidos fuertes y débiles. En su lugar, corta o aumenta el volumen medio global, lo que puede provocar una distorsión no deseada durante la reproducción.

 

Si solicita un control de intervalo dinámico desde el descodificador cuando no se establece esta propiedad, el códec calculará un valor predeterminado.

Use las propiedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) y [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular los valores adecuados para esta propiedad.

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

 

 




