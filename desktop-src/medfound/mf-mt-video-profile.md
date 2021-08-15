---
description: Especifica el perfil de codificación de vídeo en el tipo de medio de salida. Se trata de un alias del \_ atributo MF MT \_ MPEG2 \_ PROFILE.
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2af7c6ebbbbb78626e96385a6eda5a25c38a3ae8473fac866866248570cc48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741398"
---
# <a name="mf_mt_video_profile-attribute"></a>Atributo MF \_ MT \_ VIDEO \_ PROFILE

Especifica el perfil de codificación de vídeo en el tipo de medio de salida. Se trata de un alias del [ \_ atributo MF MT \_ MPEG2 \_ PROFILE.](mf-mt-mpeg2-profile-attribute.md)

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

**Codificadores H.264:**

Se superan los perfiles admitidos para incluir [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) y **eAVEncH264VProfile \_ ConstrainedHigh**.

Los codificadores deben admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) y [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para este atributo.

Esto es estático, por lo que los codificadores de vídeo deben configurarse antes de que se inicie el streaming. Si la aplicación establece un perfil que el codificador no admite, el codificador rechazará el tipo de medio.

Valor predeterminado recomendado: [**perfil principal \_ eAVEncH264VProfile.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
