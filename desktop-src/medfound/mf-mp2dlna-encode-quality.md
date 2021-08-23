---
description: Especifica la calidad de codificación del receptor multimedia de Digital Living Network Alliance (DLNA).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: MF_MP2DLNA_ENCODE_QUALITY atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a612dae32aabe4276ece76e7edff1aef431cc5d93f8aeaae0dbc9087620374c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973664"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>Atributo \_ MF MP2DLNA \_ ENCODE \_ QUALITY

Especifica la calidad de codificación del receptor multimedia de Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Intervalo: 0-18

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Los números más altos indican una mejor calidad de codificación. Los números más bajos indican una codificación más rápida, pero una calidad de codificación inferior. El valor predeterminado es 9.

Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




