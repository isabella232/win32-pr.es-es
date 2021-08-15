---
description: Especifica el nivel medio de volumen del contenido de audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7d3575b81ca878c610aed95ca25f73fa94c292ec16f9245a72a3a9515198c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973244"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>Propiedad MFPKEY \_ WMADRC \_ AVGREF

Especifica el nivel medio de volumen del contenido de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Puede obtener este valor del codificador después de procesar el contenido. Este valor también se puede establecer en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [ \_ MFPKEY WMADEC \_ DRCMODE.](mfpkey-wmadec-drcmodeproperty.md)

Para obtener más información sobre el control de intervalo dinámico, vea el artículo web [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
