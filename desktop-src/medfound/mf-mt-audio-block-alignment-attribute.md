---
description: Alineación de bloques, en bytes, para un tipo de medio de audio. La alineación de bloques es la unidad atómica mínima de datos para el formato de audio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: MF_MT_AUDIO_BLOCK_ALIGNMENT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5985485313bda76221a9a45dc4a6aa9f257884766398dce8a9301401d49ea2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113895"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a>Atributo MF \_ MT \_ AUDIO BLOCK \_ \_ ALIGNMENT

Alineación de bloques, en bytes, para un tipo de medio de audio. La alineación de bloques es la unidad atómica mínima de datos para el formato de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

En el caso de los formatos de audio PCM, la alineación del bloque es igual al número de canales de audio multiplicado por el número de bytes por muestra de audio.

Este atributo corresponde al miembro **nBlockAlign** de la [**estructura DETENTEATEX.**](/previous-versions/dd757713(v=vs.85))

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 
