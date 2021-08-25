---
description: Los siguientes GUID definen extensiones de carga útil para secuencias de formato de sistemas avanzados (ASF).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID de extensión de carga de ASF (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6478c024d3e79b0f8035f03b6e893e2e5d0308037242f9ac3013450b57f83242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959575"
---
# <a name="asf-payload-extension-guids"></a>GUID de extensión de carga de ASF

Los siguientes GUID definen extensiones de carga útil para secuencias de formato de sistemas avanzados (ASF).



| Constante                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**MFASFSampleExtension \_ SampleDuration**</dt> </dl>         | Los datos indican la duración, en milisegundos, del ejemplo contenido en el objeto de búfer.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt> </dl> | Los datos indican si el ejemplo es un fotograma clave. Un valor de cero indica que la muestra no es un fotograma clave. Un valor distinto de cero indica que es un fotograma clave.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**MFASFSampleExtension \_ SMPTE**</dt> </dl>                                             | Los datos son un código de tiempo SMPTE.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**MFASFSampleExtension \_ FileName**</dt> </dl>                                 | Los datos de la extensión de ejemplo especifican el nombre del archivo del que se tomó el contenido del ejemplo.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**MFASFSampleExtension \_ ContentType**</dt> </dl>                     | Los datos identifican el tipo de contenido que contiene el ejemplo.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt> </dl> | Los datos indican la relación de aspecto de píxeles del contenido del ejemplo.<br/>                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> </dl>

 

 




