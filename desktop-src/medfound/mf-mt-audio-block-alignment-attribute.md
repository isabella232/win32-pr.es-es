---
description: Alineación de bloques, en bytes, para un tipo de medio de audio. La alineación de bloques es la unidad atómica mínima de datos para el formato de audio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: MF_MT_AUDIO_BLOCK_ALIGNMENT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361158"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a>Atributo MF \_ MT \_ AUDIO BLOCK \_ \_ ALIGNMENT

Alineación de bloques, en bytes, para un tipo de medio de audio. La alineación de bloques es la unidad atómica mínima de datos para el formato de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

En el caso de los formatos de audio PCM, la alineación del bloque es igual al número de canales de audio multiplicados por el número de bytes por muestra de audio.

Este atributo corresponde al miembro **nBlockAlign** de la [**estructura DETENTEATEX.**](/previous-versions/dd757713(v=vs.85))

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 
