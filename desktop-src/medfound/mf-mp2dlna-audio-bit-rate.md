---
description: Especifica la velocidad máxima de bits de audio para el receptor multimedia de Digital Living Network Alliance (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: MF_MP2DLNA_AUDIO_BIT_RATE atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474170"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>Atributo \_ MF MP2DLNA \_ AUDIO BIT \_ \_ RATE

Especifica la velocidad máxima de bits de audio para el receptor multimedia de Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es la velocidad de bits máxima de destino para la secuencia de audio codificada, en bits por segundo. El valor debe ser una de las velocidades de bits permitidas para el audio MPEG-2 de nivel 2 para DLNA. El valor predeterminado es 192000 (192 Kbps).

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




