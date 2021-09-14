---
description: Enumeraciones de codec API
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Enumeraciones de codec API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c97da1fe45aba1d81e7036fa7ba6e75fc225a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070080"
---
# <a name="codec-api-enumerations"></a>Enumeraciones de codec API



| Enumeración                                                                              | Descripción                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Especifica la configuración del altavoz para los canales de audio en la secuencia de bits de audio.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Especifica si el audio está codificado en Dolby Surround.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Especifica si un descodificador de AAC usa ecuaciones estándar mpeg-2/MPEG-4 de reducción de mezcla estéreo.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Especifica si la secuencia de audio de entrada es estéreo o mono dual.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Especifica cómo el descodificador reproduce el audio mono dual.                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Especifica el modo de control de compresión para una secuencia de audio Dolby AC-3.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Especifica si un descodificador de AAC realiza el control de intervalo dinámico.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Especifica cómo se entrelaza la secuencia de vídeo descodificada.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Especifica el modo de desinterlace de software de un descodificador de vídeo.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Especifica el nivel de ahorro de energía de un descodificador de vídeo.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Especifica si la ecualización de sonoridad está habilitada en un descodificador de audio o un procesador de señales digitales (DSP). |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Especifica si el relleno del altavoz está habilitado en un descodificador de audio o DSP.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Especifica si el audio de 2 canales se codifica como estéreo o mono dual.                                      |
| [**eAVEncAudioInputContent (Enumeración)**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Especifica si el contenido de audio contiene música o voz.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Especifica el modo de control de velocidad.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Especifica si el codificador descarta grupos parciales de imágenes (GOP) al final de la secuencia.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Especifica el tipo de conversión de analog-to-digital (A/D) para una secuencia de audio Dolby Digital.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Especifica el perfil de control de intervalo dinámico en una secuencia de audio Dolby Digital.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Especifica el modo de casco para una secuencia de audio Dolby Digital.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Especifica el modo de mezcla abajo estéreo preferido para una secuencia de audio Dolby Digital.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Especifica el tipo de sala para una secuencia de audio Dolby Digital.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Especifica el servicio de audio contenido en una secuencia de audio Dolby Digital.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Especifica si una secuencia de audio Dolby Digital está codificada en Dolby Digital Surround EX.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Especifica el intervalo nominal de un origen de vídeo.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Especifica el modo de codificación de audio MPEG.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Especifica el tipo de filtro de desacentración que se debe usar alcoding.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Especifica la capa de audio MPEG.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Especifica si el codificador genera campos codificados o fotogramas codificados.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Especifica qué tabla de codificación de longitud variable (VLC) se va a usar para codificar entropía.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Especifica el perfil MPEG-2.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Especifica el perfil MPEG-2.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Especifica si la escala del cuantificador es lineal o no lineal.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Especifica el patrón de examen de macroblock.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Especifica cómo se comporta el codificador cuando detecta una nueva escena.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Especifica el tipo de flujo de salida generado por un multiplexor.                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Especifica la resolución de conflictos.                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Especifica la siting del siting del objeto.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Especifica las condiciones de iluminación previstas para ver un origen de vídeo.                                    |
| [**eAVEncVideoColorNorange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Especifica el intervalo nominal de un origen de vídeo.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Especifica los colores principal del vídeo.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Especifica la función de conversión de R'G'B' a RGB.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Especifica la matriz de conversión del espacio de colores Y'Cb'Cr' al espacio de colores R'G'B'.                  |
| [**eAVEncVideoContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Especifica si el origen original del vídeo de entrada era película o vídeo.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Especifica si el codificador convierte la velocidad de fotogramas.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Especifica cómo el codificador entrelaza el vídeo de salida.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Especifica si los fotogramas de entrada de un codificador son progresivas o entrelazadas.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Especifica la velocidad de la decodificación de vídeo.                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de códec](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
