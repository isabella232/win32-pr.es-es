---
description: Velocidad de errores de datos, en errores de bits por segundo, para un tipo de medio de vídeo.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: MF_MT_AVG_BIT_ERROR_RATE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360458"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a>Atributo AVG \_ \_ BIT ERROR RATE \_ \_ \_ de MF MT

Velocidad de errores de datos, en errores de bits por segundo, para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo corresponde al miembro **dwBitErrorRate** de las estructuras [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
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

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 
