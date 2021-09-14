---
description: Especifica el perfil MPEG-2 o H.264 en un tipo de medio de vídeo.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: MF_MT_MPEG2_PROFILE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269148"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a>Atributo \_ MF MT \_ MPEG2 \_ PROFILE

Especifica el perfil MPEG-2 o H.264 en un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Para el vídeo MPEG-2, el valor de este atributo es un miembro de la [**enumeración AM \_ MPEG2Profile.**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile)

Para el vídeo H.264, el valor es miembro de la enumeración [**eAVEncH264VProfile.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile)

Este atributo corresponde al miembro **dwProfile** de la [**estructura MPEG2VIDEOINFO.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)

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

 

 
