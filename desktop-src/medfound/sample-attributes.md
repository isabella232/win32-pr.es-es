---
description: Atributos de ejemplo
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Atributos de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1329946c36b1b7454deb76a25247985d9dcfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543814"
---
# <a name="sample-attributes"></a>Atributos de ejemplo

Los siguientes atributos se aplican a los [ejemplos de medios](media-samples.md). Para obtener los atributos de un ejemplo multimedia, use la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Atributo                                                                                                      | Descripción                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Especifica si un ejemplo multimedia contiene un fotograma de vídeo 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Especifica el ámbito del campo de un fotograma de vídeo entrelazado.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | La cámara extrinsics para el ejemplo.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | El almacén de [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para todos los metadatos relacionados con la canalización de captura.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Indica si un ejemplo de vídeo es un fotograma clave.                                                                                                                                                                                                   |
| [ID. de contenido de MFSampleExtension \_ \_](mfsampleextension-content-keyid.md)                                       | Establece el identificador de clave para el ejemplo.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Especifica si un fotograma de vídeo desentrelazado se ha derivado del campo superior o del campo inferior.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | Marca de tiempo del controlador de dispositivo.                                                                                                                                                                                                             |
| [**Discontinuidad de MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md)                          | Especifica si un ejemplo multimedia es el primer ejemplo después de un intervalo en la secuencia.                                                                                                                                                                    |
| [MFSampleExtension \_ cifrado \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Especifica el tamaño del bloque de bytes cifrado para el cifrado del modelo basado en el ejemplo.                                                                                                                                                                       |
| [MFSampleExtension \_ cifrado \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Especifica el esquema de protección para los ejemplos cifrados.                                                                                                                                                                                             |
| [MFSampleExtension \_ cifrado \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Especifica el identificador de un ejemplo cifrado.                                                                                                                                                                                                           |
| [MFSampleExtension \_ cifrado \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | Especifica el tamaño de bloque de bytes sin cifrar (sin cifrar) para el cifrado del modelo basado en el ejemplo.                                                                                                                                                           |
| [MFSampleExtension \_ cifrado \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Establece la asignación de submuestra para el ejemplo que indica los bytes claros y cifrados de los datos de ejemplo.                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | Especifica si un fotograma de vídeo está dañado.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Obtiene un objeto de tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contiene objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contienen unidades de capa de abstracción de red (NALUs) e información de mejora adicional (SEI) reenviadas por un descodificador. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Especifica el tipo NALU o SEI de una unidad asociada a un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) en una colección [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) .                                                    |
| [**MFSampleExtension \_ entrelazado**](mfsampleextension-interlaced-attribute.md)                                | Indica si un fotograma de vídeo está entrelazado o progresivo.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Especifica la información de marco de referencia a largo plazo (LTR) y se devuelve en el ejemplo de salida.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Este atributo devuelve la diferencia absoluta media (MAD) en todos los bloques de macros del plano Y.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Especifica los límites de carga de un marco. Esto se aplica a los ejemplos cifrados.                                                                                                                                                                   |
| [Fotominiatura MFSampleExtension \_](mfsampleextension-photothumbnail.md)                                      | Contiene la miniatura de la fotografía de un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Contiene el [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que describe el tipo de formato de imagen contenido en el atributo de [ \_ fotominiatura MFSampleExtension](mfsampleextension-photothumbnail.md) .                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | La cámara pinhole intrínseco para el ejemplo.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Especifica si se va a repetir el primer campo en un marco entrelazado.                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | Especifica si un ejemplo de vídeo contiene un solo campo o dos campos intercalados                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | Valor en Nits que especifica la luminancia de iluminación global de destino del fotograma de vídeo asociado.                                                                                                                                           |
| [**\_Token MFSampleExtension**](mfsampleextension-token-attribute.md)                                          | Contiene un puntero al token que se proporcionó al método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Especifica el parámetro de cuantificación (QP) que se usó para codificar un ejemplo de vídeo.                                                                                                                                                                  |



 

No todas las muestras de medios contienen todos los atributos que se muestran aquí. En algunos casos, un atributo solo se aplica a determinados tipos de datos. Por ejemplo, algunos atributos solo se aplican a los ejemplos de vídeo y no deben aparecer en las muestras de audio. En otros casos, el atributo tiene un valor predeterminado que se aplica si no se establece el atributo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> </dl>

 

 



