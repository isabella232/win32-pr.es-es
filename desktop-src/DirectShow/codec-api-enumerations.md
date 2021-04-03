---
description: Enumeraciones de API de códecs
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Enumeraciones de API de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c97da1fe45aba1d81e7036fa7ba6e75fc225a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997841"
---
# <a name="codec-api-enumerations"></a>Enumeraciones de API de códecs



| Enumeración                                                                              | Descripción                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Especifica la configuración de los altavoces para los canales de audio en el flujo de bits de audio.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Especifica si el audio se codifica en Dolby Surround.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Especifica si un descodificador AAC utiliza ecuaciones de downmix estéreo estándar MPEG-2/MPEG-4.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Especifica si la secuencia de audio de entrada es estéreo o dual mono.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Especifica cómo el descodificador Reproduce audio mono dual.                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Especifica el modo de control de compresión para una secuencia de audio Dolby AC-3.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Especifica si un descodificador AAC realiza un control de intervalo dinámico.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Especifica cómo se entrelaza la secuencia de vídeo descodificada.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Especifica un modo de desentrelazado de software del descodificador de vídeo.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Especifica el nivel de ahorro de energía de un descodificador de vídeo.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Especifica si la ecualización de sonoridad está habilitada en un descodificador de audio o en un procesador de señal digital (DSP). |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Especifica si el relleno del altavoz está habilitado en un descodificador de audio o en un DSP.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Especifica si el audio de 2 canales se codifica como estéreo o dual mono.                                      |
| [**Enumeración eAVEncAudioInputContent**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Especifica si el contenido de audio contiene música o voz.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Especifica el modo de control de velocidad.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Especifica si el codificador descarta grupos parciales de imágenes (GOP) al final de la secuencia.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Especifica el tipo de conversión analógica a digital (a/D) para una secuencia de audio Dolby digital.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Especifica el perfil de control de intervalo dinámico en una secuencia de audio Dolby digital.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Especifica el modo de auricular para una secuencia de audio Dolby digital.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Especifica el modo downmix estéreo preferido para una secuencia de audio Dolby digital.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Especifica el tipo de habitación de una secuencia de audio Dolby digital.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Especifica el servicio de audio incluido en una secuencia de audio Dolby digital.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Especifica si una secuencia de audio Dolby Digital está codificada en Dolby Digital Surround EX.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Especifica el intervalo nominal para un origen de vídeo.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Especifica el modo de codificación de audio MPEG.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Especifica el tipo de filtro de desacentuación que se debe usar al descodificar.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Especifica la capa de audio MPEG.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Especifica si el codificador genera campos codificados o fotogramas codificados.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Especifica la tabla de codificación de longitud variable (VLC) que se va a usar para la codificación de entropía.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Especifica el perfil MPEG-2.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Especifica el perfil MPEG-2.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Especifica si la escala del cuantificador es lineal o no lineal.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Especifica el patrón de examen de adaptativo macrobloque.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Especifica cómo se comporta el codificador cuando detecta una nueva escena.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Especifica el tipo de flujo de salida generado por un multiplexor.                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Especifica la resolución de croma.                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Especifica la colocación cromada.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Especifica las condiciones de iluminación previstas para ver un origen de vídeo.                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Especifica el intervalo nominal para un origen de vídeo.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Especifica los primarios de color del vídeo.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Especifica la función de conversión de R'G'B ' a RGB.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Especifica la matriz de conversión del espacio de colores de Y'Cb'Cr al espacio de colores de R'G'B.                  |
| [**eAVEncVideoFilmContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Especifica si el origen original del vídeo de entrada era película o vídeo.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Especifica si el codificador convierte la velocidad de fotogramas.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Especifica cómo el codificador entrelaza el vídeo de salida.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Especifica si los fotogramas de entrada de un codificador son progresivos o entrelazados.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Especifica la velocidad de descodificación de vídeo.                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de códecs](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
