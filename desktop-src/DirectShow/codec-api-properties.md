---
description: Propiedades de la API de códec
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Propiedades de la API de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91346b6595944b8e95da5e9e43023052119e49a8b88809fce08b6fca780beba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792915"
---
# <a name="codec-api-properties"></a>Propiedades de la API de códec

-   [Propiedades comunes de audio](#common-audio-properties)
-   [Propiedades comunes del descodificador](#common-decoder-properties)
-   [Propiedades comunes del codificador](#common-encoder-properties)
-   [Propiedades del descodificador de vídeo](#video-decoder-properties)
-   [Propiedades del descodificador de audio](#audio-decoder-properties)
-   [Propiedades del codificador de vídeo](#video-encoder-properties)
-   [Propiedades del codificador de audio](#audio-encoder-properties)
-   [Propiedades del codificador de vídeo MPEG](#mpeg-video-encoder-properties)
-   [Propiedades del codificador de audio MPEG](#mpeg-audio-encoder-properties)
-   [Propiedades del descodificador de Audio Digital Dolby](#dolby-digital-audio-decoder-properties)
-   [Propiedades del codificador Dolby Digital Audio](#dolby-digital-audio-encoder-properties)
-   [Propiedades de Procesamiento de señales digitales (DSP)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Propiedades comunes de audio

Estas propiedades se aplican a codificadores de audio y descodificadores de audio.



| Propiedad                                                      | Descripción                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Obtiene la configuración del altavoz para los canales de audio de la secuencia de bits de audio. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Obtiene el número de canales de la secuencia de bits de audio.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Obtiene la velocidad de muestreo de la secuencia de bits de audio, en muestras por segundos.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Especifica si el audio está codificado en Dolby Surround.                      |



 

### <a name="common-decoder-properties"></a>Propiedades comunes del descodificador

Estas propiedades se aplican tanto a descodificadores de audio como a descodificadores de vídeo.



| Propiedad                                                            | Descripción                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Especifica el formato de entrada actual para el descodificador.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Obtiene la velocidad de bits media actual del descodificador.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Especifica el formato de salida del descodificador.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Especifica la clase Del servicio Programador de clases multimedia (MMCSS) para el subproceso decoding. |



 

### <a name="common-encoder-properties"></a>Propiedades comunes del codificador

Estas propiedades se aplican tanto a codificadores de audio como a codificadores de vídeo.



| Propiedad                                                                          | Descripción                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Especifica el esquema de codificación.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Especifica el nivel inicial del búfer de codificación.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Especifica el nivel final del búfer de codificación al final del proceso de codificación.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Especifica el tamaño del búfer utilizado durante la codificación.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Especifica el formato de destino para un codificador.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Especifica si el flujo de salida debe estructurarse para que la secuencia codificada tenga una latencia de descodificación baja. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Especifica la velocidad de bits máxima.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Especifica la velocidad de bits media.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits media.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Especifica la velocidad de bits mínima.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Especifica el número de pases de codificación que admite el codificador.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Detiene el paso de codificación actual o consulta si el paso de codificación actual es el último.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Inicia el primer paso de codificación.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Especifica el nivel de calidad para la codificación.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Especifica el equilibrio entre la calidad y la velocidad de la codificación.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Especifica el modo de control de velocidad.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Especifica si la aplicación requiere un rendimiento de codificación en tiempo real.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Especifica si el codificador descarta grupos parciales de imágenes (GOP) al final de la secuencia.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Especifica el tipo de flujo de salida generado por un multiplexor.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Especifica el número de pases de codificación completados.                                                              |



 

### <a name="video-decoder-properties"></a>Propiedades del descodificador de vídeo



| Propiedad                                                                                | Descripción                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Habilita o deshabilita la aceleración de hardware para lacodización de vídeo H.264.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Habilita o deshabilita la aceleración de hardware para la codificación de vídeo MPEG-2.            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Habilita o deshabilita la aceleración de hardware para lacodización de vídeo vc-1.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Especifica si el descodificador coloca fotogramas dentro de los que faltan fotogramas de referencia. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Obtiene o establece la velocidad de la decodificación de vídeo.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Obtiene el tamaño de la imagen descodificada, en píxeles.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Especifica cómo se entrelaza la secuencia de vídeo descodificada.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Especifica la relación de aspecto de píxeles de la secuencia de vídeo descodificada.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Especifica el modo de desinterlace de software del descodificador.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Especifica el nivel de ahorro de energía.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Habilita o deshabilita el modo de generación de miniaturas.                                  |



 

### <a name="audio-decoder-properties"></a>Propiedades del descodificador de audio



| Propiedad                                                                        | Descripción                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Especifica si un descodificador de AAC usa ecuaciones estándar mpeg-2/MPEG-4 de reducción estéreo, o bien una reducción no estándar. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Especifica si el audio de 2 canales está codificado como estéreo o mono dual.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Especifica cómo reproduce el descodificador el audio mono dual.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Habilita o deshabilita el control de intervalo dinámico en un descodificador de AAC.                                                           |



 

### <a name="video-encoder-properties"></a>Propiedades del codificador de vídeo



| Propiedad                                                                                        | Descripción                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Especifica el sistema de vídeo del contenido de origen.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Devuelve el número de fotogramas de vídeo codificados.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Devuelve la velocidad media de fotogramas del contenido del vídeo.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Devuelve el número de fotogramas de vídeo recibidos por el codificador.                                                         |
| [**AVEncVideoCBRMotionMotionOff**](avencvideocbrmotiontradeoff-property.md)                     | Especifica el equilibrio entre el movimiento y las imágenes fijas.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Especifica el tamaño de las unidades de acceso de vídeo.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Especifica qué campo se muestra primero.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Especifica el tamaño de la secuencia de vídeo cuando se descodifica.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Especifica el ancho y el alto del vídeo codificado, si el vídeo está recortado.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo está recortado.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Invierte el orden de los campos entrelazados en el vídeo de origen.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Especifica si los marcos de entrada son progresivas o entrelazadas.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Especifica el valor de la marca de marco de colocación en el encabezado GOP.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Especifica el número de marco inicial en el encabezado GOP.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Especifica el número de hora de inicio en el encabezado GOP.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Especifica el número de minuto inicial en el encabezado GOP.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Especifica el segundo número inicial en el encabezado GOP.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Especifica la resolución de la escala del vídeo de entrada.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Especifica el siting de la escala para el vídeo de entrada.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Especifica las condiciones de iluminación previstas para ver el vídeo de entrada.                                               |
| [**AVEncVideoInputColorNorange**](avencvideoinputcolornominalrange-property.md)           | Especifica el intervalo nominal del vídeo de entrada.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Especifica los valores de color principal para el vídeo de entrada.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Especifica la función de conversión de RGB a R'G'B' para el vídeo de entrada.                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Especifica la matriz de conversión del espacio de colores Y'Cb'Cr' al espacio de colores R'G'B' para el vídeo de entrada.         |
| [**AVEncVideoInverseTeledivable**](avencvideoinversetelecineenable-property.md)             | Especifica si el codificador realiza televisa inversa.                                                              |
| [**AVEncVideoInverseTelevideoThreshold**](avencvideoinversetelecinethreshold-property.md)       | Establece el umbral en el que el codificador considera redundante un campo de vídeo.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Especifica el número máximo de fotogramas entre fotogramas clave.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Especifica el número de campos que se codifican.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Especifica el número de campos que se omitirán durante la codificación.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Especifica la resolución de la escala del vídeo codificado.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Especifica el siting del objeto para el vídeo codificado.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Especifica las condiciones de iluminación previstas para ver el vídeo codificado.                                             |
| [**AVEncVideoOutputColorNorange**](avencvideooutputcolornominalrange-property.md)         | Especifica el intervalo nominal del vídeo codificado.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Especifica los valores de color principal para el vídeo codificado.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Especifica la función de conversión de RGB a R'G'B' para vídeo codificado.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Especifica la matriz de conversión del espacio de colores Y'Cb'Cr' al espacio de colores R'G'B' para el vídeo codificado.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Especifica si el codificador convierte la velocidad de fotogramas cuando la velocidad de fotogramas de salida no coincide con la velocidad de fotogramas de entrada. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Especifica cómo entrelaza el codificador el vídeo de salida.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Especifica la relación de aspecto de píxeles.                                                                                     |
| [**AVEncVideoSourceContent**](avencvideosourcefilmcontent-property.md)                     | Especifica si el origen original del vídeo de entrada era película o vídeo.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Especifica si el vídeo es monocromo (blanco y negro) o contiene color.                                        |



 

### <a name="audio-encoder-properties"></a>Propiedades del codificador de audio



| Propiedad                                                                        | Descripción                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Especifica si el audio de 2 canales se codifica como estéreo o mono dual.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Especifica si el contenido de audio contiene música o voz.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Especifica el número de muestras de audio que se codifican.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Especifica el número de muestras de audio que el codificador omitirá.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Especifica qué canal de audio se asigna al canal *N* en la secuencia de audio codificada. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Especifica la velocidad de bits media de la secuencia de audio codificada.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Devuelve el promedio de bits por segundo del audio codificado.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Devuelve el nivel medio de volumen del contenido de audio.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Devuelve el nivel de volumen más alto que estaba presente en el contenido de audio.             |



 

### <a name="mpeg-video-encoder-properties"></a>Propiedades del codificador de vídeo MPEG



| Propiedad                                                                                    | Descripción                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Especifica si el codificador agrega un código final de secuencia al final de la secuencia.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Especifica el número predeterminado de fotogramas B consecutivos entre fotogramas I y P.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Especifica si el codificador genera campos codificados o fotogramas codificados.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Especifica si el codificador genera encabezados de extensión de visualización de imagen.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Especifica si el codificador genera encabezados de extensión de imagen.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Especifica si el codificador genera encabezados de extensión de visualización de secuencia.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Especifica si el codificador genera encabezados de extensión de secuencia.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Especifica si el codificador genera encabezados de extensión escalables de secuencia.         |
| [**AVEncMPVGOPAbrir**](avencmpvgopopen-property.md)                                         | Especifica si el codificador genera GOP abiertos o GOP cerrados.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Especifica el número de GOP entre encabezados de secuencia.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Especifica el número máximo de imágenes de un encabezado GOP al siguiente encabezado GOP. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Especifica la precisión de los coeficientes de controlador de dominio.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Especifica qué tabla de codificación de longitud variable (VLC) se va a usar para codificar entropía.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Especifica el nivel MPEG-2.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Especifica el perfil MPEG-2.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Especifica si la escala del cuantificador es lineal o no lineal.                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | Especifica la matriz de cuantificación de quantization de quantization para macrobloques dentro de .                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Especifica la matriz de cuantificación de quantization para macrobloques que no están dentro de .                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Especifica la matriz de cuantificación de luma para los macrobloqueos dentro de .                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Especifica la matriz de cuantificación de luma para bloques de macro no dentro.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Especifica el patrón de examen de macroblock.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Especifica cómo se comporta el codificador cuando detecta una nueva escena.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Especifica si el codificador usa vectores de movimiento de ocultación.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>Propiedades del codificador de audio MPEG



| Propiedad                                                                                  | Descripción                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Especifica el modo de codificación de audio MPEG-1.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Especifica la configuración predeterminada para el bit de copyright.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Especifica el tipo de filtro de desacentración que se debe usar alcoding.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Especifica la capa de audio MPEG.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Especifica la configuración predeterminada para el bit original.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Establece el valor del bit de usuario privado.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Propiedades del descodificador de Audio Digital Dolby



| Propiedad                                                                      | Descripción                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Especifica el corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico.  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Especifica la potenciación de bajo nivel cuando el descodificador realiza el control de intervalo dinámico. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Especifica el modo de control de compresión.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Propiedades de Dolby Digital Audio Encoder



| Propiedad                                                                                        | Descripción                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | Especifica el tipo de conversión de análogo a digital (A/D).                                 |
| [**AVEncDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Especifica el nivel de mezcla inferior central.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Especifica si se aplica un filtro de paso bajo a los canales de entrada principales.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Especifica la marca de copyright.                                                             |
| [**AVEncDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Especifica si se aplica un filtro de paso alto de bloqueo de controlador de dominio.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Especifica el nivel de normalización del cuadro de diálogo.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Especifica si el des-énfasis digital.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Especifica el perfil de control de intervalo dinámico.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Especifica el modo de casco.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Especifica si se aplica un filtro de paso bajo al canal de efecto de baja frecuencia (LFE). |
| [**AVEncDDLoRoCenterMixLvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | Especifica el desplazamiento de nivel que se aplica al canal central para la mezclación lo/ro.     |
| [**AVEncDDLoRoSurroundMixLvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | Especifica el desplazamiento de nivel que se aplica a los canales envolventes para la mezclación lo/ro.  |
| [**AVEncDDLtRtCenterMixLvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | Especifica el desplazamiento de nivel que se aplica al canal central para la remezclación lt/rt.     |
| [**AVEncDDLtRtSurroundMixLvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | Especifica el desplazamiento de nivel que se aplica a los canales envolventes para la mezclación Lt/Rt.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Especifica la marca de secuencia de bits original.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Especifica el modo de bajada estéreo preferido.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Especifica la marca de información de producción de audio.                                          |
| [**AVEncDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Especifica el nivel de combinación.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Especifica el tipo de habitación.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Especifica la configuración de protección de sobremodulación de radiofrecuencia.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Especifica el servicio de audio.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Especifica si los canales envolventes se atenuan antes de la codificación.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Especifica si se aplica un desplazamiento de fase de 90 grados a los canales envolventes.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Especifica el nivel de combinación Rodear hacia abajo.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Especifica si la secuencia de audio está codificada en Surround EX.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Propiedades de Procesamiento de señales digitales (DSP)



| Propiedad                                                                | Descripción                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | Habilita o deshabilita la igualdad de sonoridad. |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Habilita o deshabilita el relleno del hablante.          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de códec](codec-api-reference.md)
</dt> </dl>

 

 



