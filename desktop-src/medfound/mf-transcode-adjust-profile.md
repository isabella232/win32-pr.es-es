---
description: Marcas de perfil que definen la configuración de secuencia para la topología de transcodificación. Las marcas se definen en la enumeración MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ FLAGS.
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb25f4df47d281ddb0e359d98e8a411cb3abb365b479388e9b7ae107e786703c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739473"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>Atributo \_ MF TRANSCODE \_ ADJUST \_ PROFILE

Marcas de perfil que definen la configuración de secuencia para la topología de transcodificación. Las marcas se definen en la enumeración [**MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ FLAGS.**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags)

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer este atributo en el nivel de contenedor en el perfil de transcodificación. Si se establece este atributo, la función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) cambia los atributos de secuencia durante la creación de la topología, en función de la marca especificada. Por ejemplo, si la aplicación especifica la marca **MF \_ TRANSCODE \_ ADJUST PROFILE \_ \_ DEFAULT,** la configuración de flujo especificada por la aplicación se usa para crear el perfil.

Para la secuencia de vídeo, la velocidad de fotogramas se actualiza en función del origen multimedia. Si la aplicación no especifica el modo entrelazado, el perfil se actualiza para usar marcos progresivas de forma predeterminada.

Si la aplicación especifica la marca **MF \_ TRANSCODE \_ ADJUST PROFILE USE \_ SOURCE \_ \_ \_ ATTRIBUTES** , los atributos de secuencia que faltan se copian del origen del medio de entrada a la configuración de secuencia del perfil de transcodificación.

La constante GUID de este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




