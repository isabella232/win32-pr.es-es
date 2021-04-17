---
description: Especifica el perfil de codificación de vídeo en el tipo de medio de salida. Se trata de un alias del \_ atributo de perfil MF MT \_ MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716957"
---
# <a name="mf_mt_video_profile-attribute"></a>\_Atributo de \_ Perfil de vídeo MF MT \_

Especifica el perfil de codificación de vídeo en el tipo de medio de salida. Se trata de un alias del atributo de [ \_ \_ \_ perfil MF MT MPEG2](mf-mt-mpeg2-profile-attribute.md) .

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

**Codificadores H. 264:**

Los perfiles admitidos se superan para incluir [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) y **eAVEncH264VProfile \_ ConstrainedHigh**.

Los codificadores deben admitir [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) y [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para este atributo.

Esto es estático, por lo que los codificadores de vídeo deben configurarse antes de que se inicie la transmisión por secuencias. Si la aplicación establece un perfil que el codificador no admite, el codificador rechazará el tipo de medio.

Valor predeterminado recomendado: perfil [**\_ principal de eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
