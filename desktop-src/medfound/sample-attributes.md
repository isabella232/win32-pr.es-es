---
description: Atributos de ejemplo
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Atributos de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56593978a411b314e6e988c031ee36869c4ea44212fd7f154e3ba18478400b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776985"
---
# <a name="sample-attributes"></a>Atributos de ejemplo

Los atributos siguientes se aplican a [los ejemplos de medios](media-samples.md). Para obtener los atributos de un ejemplo multimedia, use la [**interfazATTRIBUTEs.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)



| Atributo                                                                                                      | Descripción                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Especifica si un ejemplo multimedia contiene un fotograma de vídeo 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Especifica la dominación de campo para un fotograma de vídeo entrelazado.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | Extrínsecos de la cámara para el ejemplo.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | [**EL almacén DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para todos los metadatos relacionados con la canalización de captura.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Indica si un ejemplo de vídeo es un fotograma clave.                                                                                                                                                                                                   |
| [MFSampleExtension \_ Content \_ KeyID](mfsampleextension-content-keyid.md)                                       | Establece el identificador de clave del ejemplo.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Especifica si se ha derivado un fotograma de vídeo desenlazado del campo superior o inferior.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | Marca de tiempo del controlador del dispositivo.                                                                                                                                                                                                             |
| [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md)                          | Especifica si un ejemplo multimedia es el primer ejemplo después de un intervalo en la secuencia.                                                                                                                                                                    |
| [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Especifica el tamaño del bloque de bytes cifrado para el cifrado de patrones basado en muestras.                                                                                                                                                                       |
| [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Especifica el esquema de protección para las muestras cifradas.                                                                                                                                                                                             |
| [MFSampleExtension \_ Encryption \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Especifica el identificador de un ejemplo cifrado.                                                                                                                                                                                                           |
| [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | Especifica el tamaño de bloque de bytes sin cifrar (no cifrado) para el cifrado de patrones basado en muestras.                                                                                                                                                           |
| [SubSampleExtension \_ Encryption \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Establece la asignación de sub sample para el ejemplo que indica los bytes claros y cifrados en los datos de ejemplo.                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | Especifica si un fotograma de vídeo está dañado.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Obtiene un objeto de tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contiene objetos [**RECORDSETSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contienen unidades de capa de abstracción de red (NALUs) y unidades de información de mejora complementaria (SEI) reenviadas por un descodificador. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Especifica el tipo, NALU o SEI, de una unidad adjuntada a [**UN ELEMENTOSAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) en una [colección MFSampleExtension \_ ForwardedDecodeUnits.](mfsampleextension-forwardeddecodeunits.md)                                                    |
| [**MFSampleExtension \_ entrelazada**](mfsampleextension-interlaced-attribute.md)                                | Indica si un fotograma de vídeo está entrelazado o progresiva.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Especifica la información del marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Este atributo devuelve la diferencia absoluta media (MAD) entre todos los bloques de macros del plano Y.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Especifica los límites de carga de un marco. Esto se aplica a los ejemplos cifrados.                                                                                                                                                                   |
| [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)                                      | Contiene la miniatura de la foto de [**un elemento DESEMPLOTESample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Contiene [**EL VALOR DE LA PROPIEDADMEDIATYPE,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que describe el tipo de formato de imagen contenido en el [atributo MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | Intrínsecos de la cámara del pinhole para el ejemplo.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Especifica si se debe repetir el primer campo en un marco entrelazado.                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | Especifica si un ejemplo de vídeo contiene un solo campo o dos campos intercalados.                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | Valor de Nits que especifica la luminosidad de retroiluminación global de destino para el fotograma de vídeo asociado.                                                                                                                                           |
| [**MFSampleExtension \_ Token**](mfsampleextension-token-attribute.md)                                          | Contiene un puntero al token que se proporcionó al [**método IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Especifica el parámetro de cuantificación (QP) que se usó para codificar un ejemplo de vídeo.                                                                                                                                                                  |



 

No todos los ejemplos de medios contienen todos los atributos enumerados aquí. En algunos casos, un atributo solo se aplica a determinados tipos de datos. Por ejemplo, algunos atributos solo se aplican a ejemplos de vídeo y no deben aparecer en ejemplos de audio. En otros casos, el atributo tiene un valor predeterminado que se aplica si el atributo no está establecido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> </dl>

 

 



