---
description: Especifica el perfil de conformidad del dispositivo para codificar archivos de formato de streaming avanzado (ASF).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257772"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>Atributo \_ TRANSCODE \_ ENCODINGPROFILE de MF

Especifica el perfil de conformidad del dispositivo para codificar archivos de formato de streaming avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Use este atributo al transcodificación a un dispositivo que admita Windows multimedia. Si se establece este atributo, el codificador usará el perfil de conformidad del dispositivo, o plantilla, para Windows códecs multimedia. Establezca el atributo en el perfil de transcodificación antes de compilar la topología de transcodificación.

El valor de este atributo puede ser cualquiera de las cadenas de plantilla de conformidad enumeradas en los temas siguientes:

-   [Plantillas de conformidad de dispositivos de audio](../wmformat/audio-device-conformance-templates.md)
-   [Plantillas de conformidad de dispositivos de vídeo](../wmformat/video-device-conformance-templates.md)

Para Windows de vídeo multimedia, el generador de topologías usa este atributo para establecer la propiedad [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) en el codificador. El codificador intentará usar la plantilla especificada para codificar el contenido. Para obtener la plantilla real, recor los nodos de la topología de transcodificación para obtener un puntero al nodo del codificador. A continuación, obtenga el valor de la [**propiedad MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) del codificador.

El generador de topologías también usa el valor de este atributo para establecer la propiedad "DeviceConformanceTemplate" en el receptor de medios de ASF.

Si se establece este atributo, el objeto de metadatos del archivo ASF siempre se genera independientemente del valor especificado por la aplicación del atributo [ \_ MF TRANSCODE SKIP METADATA \_ \_ \_ TRANSFER.](mf-transcode-skip-metadata-transfer.md)

Entre los valores típicos de este atributo se incluyen los siguientes:



| Value   | Descripción                      |
|---------|----------------------------------|
| "AP"    | Vídeo de perfil avanzado           |
| "MP"    | Vídeo del perfil principal               |
| "SP"    | Vídeo de perfil simple             |
| "MP@LL" | Perfil principal, vídeo de nivel medio |
| "L2"    | Perfil de audio, <= 160 Kbps    |



 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transcodificación de API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
