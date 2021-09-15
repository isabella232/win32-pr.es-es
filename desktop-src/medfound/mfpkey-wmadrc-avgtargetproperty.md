---
description: Especifica el nivel de volumen medio deseado del contenido de audio de salida.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: MFPKEY_WMADRC_AVGTARGET propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579817"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>Propiedad MFPKEY \_ WMADRC \_ AVGTARGET

Especifica el nivel de volumen medio deseado del contenido de audio de salida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

Vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

Puede establecer este valor en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [ \_ MFPKEY WMADEC \_ DRCMODE.](mfpkey-wmadec-drcmodeproperty.md)

> [!Note]  
> No se recomienda establecer el valor de destino medio. El ajuste del valor medio no afecta a la diferencia entre los sonidos fuertes y los sonidos suave. En su lugar, reduce o aumenta el volumen medio general, lo que puede provocar una distorsión no deseada durante la reproducción.

 

Si solicita el control de intervalo dinámico del descodificador cuando no se establece esta propiedad, el códec calculará un valor predeterminado.

Use las [propiedades MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) y [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular los valores adecuados para esta propiedad.

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

 

 




