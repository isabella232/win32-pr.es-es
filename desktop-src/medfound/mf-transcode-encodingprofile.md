---
description: Especifica el perfil de conformidad de dispositivos para la codificación de archivos de formato de transmisión avanzada (ASF).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543235"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>\_Atributo ENCODINGPROFILE de TRANSCODE MF \_

Especifica el perfil de conformidad de dispositivos para la codificación de archivos de formato de transmisión avanzada (ASF).

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Use este atributo al transcodificar en un dispositivo que admita Windows Media. Si se establece este atributo, el codificador usará el perfil de conformidad del dispositivo, o plantilla, para los códecs de Windows Media. Establezca el atributo en el perfil de transcodificación antes de compilar la topología de transcodificación.

El valor de este atributo puede ser cualquiera de las cadenas de plantilla de cumplimiento enumeradas en los temas siguientes:

-   [Plantillas de cumplimiento de dispositivos de audio](../wmformat/audio-device-conformance-templates.md)
-   [Plantillas de cumplimiento de dispositivos de vídeo](../wmformat/video-device-conformance-templates.md)

En el caso de la codificación Windows Media Video, el generador de topología usa este atributo para establecer la propiedad [**\_ DECODERCOMPLEXITYREQUESTED de MFPKEY**](mfpkey-decodercomplexityrequestedproperty.md) en el codificador. El codificador intentará usar la plantilla especificada para codificar el contenido. Para obtener la plantilla real, recorra los nodos de la topología de transcodificación para obtener un puntero al nodo del codificador. A continuación, obtenga el valor de la propiedad [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) del codificador.

El generador de topología también usa el valor de este atributo para establecer la propiedad "DeviceConformanceTemplate" en el receptor multimedia ASF.

Si se establece este atributo, el objeto de metadatos del archivo ASF siempre se genera con independencia del valor especificado por la aplicación del atributo [MF \_ Transcode \_ SKIP omitir \_ \_ transferencia de metadatos](mf-transcode-skip-metadata-transfer.md) .

Los valores típicos de este atributo incluyen los siguientes:



| Value   | Descripción                      |
|---------|----------------------------------|
| AISLAMIENTO    | Vídeo de perfil avanzado           |
| MP    | Vídeo de perfil principal               |
| DAÑADO    | Vídeo de perfil sencillo             |
| "MP@LL" | Perfil principal, vídeo de nivel medio |
| L2    | Perfil de audio, <= 160 Kbps    |



 

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

[**IMFTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
