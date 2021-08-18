---
description: Especifica la velocidad máxima de bits de audio para el receptor multimedia de Digital Living Network Alliance (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: MF_MP2DLNA_AUDIO_BIT_RATE atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed622a2f826e061dc4b909eec09490974fe83a7ac850cd0fcdfcede0abd578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104771"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>Atributo \_ MF MP2DLNA \_ AUDIO BIT \_ \_ RATE

Especifica la velocidad máxima de bits de audio para el receptor multimedia de Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es la velocidad de bits máxima de destino para la secuencia de audio codificada, en bits por segundo. El valor debe ser una de las velocidades de bits permitidas para el audio MPEG-2 de nivel 2 para DLNA. El valor predeterminado es 192000 (192 Kbps).

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios para la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




