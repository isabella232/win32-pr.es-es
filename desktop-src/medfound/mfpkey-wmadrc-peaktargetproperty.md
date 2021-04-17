---
description: Especifica el nivel de volumen máximo deseado del contenido de audio de salida.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Propiedad MFPKEY_WMADRC_PEAKTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696894"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>\_ \_ Propiedad PEAKTARGET de MFPKEY WMADRC

Especifica el nivel de volumen máximo deseado del contenido de audio de salida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCPeakTarget

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

Vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

Puede establecer este valor en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .

Si solicita un control de intervalo dinámico desde el descodificador cuando no se establece esta propiedad, el códec calculará un valor predeterminado.

Use las propiedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) y [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular los valores adecuados para esta propiedad.

Para obtener más información sobre el control de intervalo dinámico, vea el artículo Web [Windows Media Audio características de códecs profesionales](/previous-versions/ms867218(v=msdn.10)).

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

 

 
