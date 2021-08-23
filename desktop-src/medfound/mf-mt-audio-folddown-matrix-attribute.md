---
description: Especifica cómo un descodificador de audio debe transformar el audio multicanal en una salida estéreo. Este proceso también se denomina plegado.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: MF_MT_AUDIO_FOLDDOWN_MATRIX atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46763f3a32999136993cd3237da9c6cbcdd1d1addb5f6d9041555ac747a6d655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714665"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>Atributo MF \_ MT \_ AUDIO \_ FOLDDOWN \_ MATRIX

Especifica cómo un descodificador de audio debe transformar el audio multicanal en una salida estéreo. Este proceso también se denomina *plegado.*

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los tipos de medios de audio.

El valor de este atributo es una [**estructura MFFOLDDOWN \_ MATRIX.**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




