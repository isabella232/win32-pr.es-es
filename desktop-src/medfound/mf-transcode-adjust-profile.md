---
description: Marcas de perfil que definen la configuración de la secuencia para la topología de transcodificación. Las marcas se definen en la \_ enumeración MF Transcode \_ ADJUST \_ Profile \_ Flags.
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687056"
---
# <a name="mf_transcode_adjust_profile-attribute"></a>Atributo de Perfil de ajuste de \_ TRANSCODIFICACIÓN MF \_ \_

Marcas de perfil que definen la configuración de la secuencia para la topología de transcodificación. Las marcas se definen en la enumeración [**MF \_ Transcode \_ ADJUST \_ Profile \_ Flags**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer este atributo en el nivel de contenedor en el perfil de transcodificación. Si se establece este atributo, la función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) cambia los atributos de la secuencia durante la compilación de la topología, en función de la marca especificada. Por ejemplo, si la aplicación especifica la marca **MF \_ Transcode \_ ADJUST \_ Profile \_ predeterminada** , se utiliza la configuración de la secuencia especificada por la aplicación para crear el perfil.

En el flujo de vídeo, la velocidad de fotogramas se actualiza en función del origen de los medios. Si la aplicación no especifica el modo entrelazado, el perfil se actualiza para utilizar fotogramas progresivos de forma predeterminada.

Si la aplicación especifica la marca **MF \_ Transcode \_ ADJUST \_ Profile \_ use \_ source \_ attributes** , los atributos de secuencia que faltan se copian desde el origen de medios de entrada a la configuración de la secuencia en el perfil de transcodificación.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[API de transcodificación](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




