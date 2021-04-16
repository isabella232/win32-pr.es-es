---
description: Propiedades de la API de códec
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Propiedades de la API de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06269591c8ddf087b83146ed72a62f4565b8340a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494644"
---
# <a name="codec-api-properties"></a>Propiedades de la API de códec

-   [Propiedades de audio comunes](#common-audio-properties)
-   [Propiedades comunes del descodificador](#common-decoder-properties)
-   [Propiedades comunes del codificador](#common-encoder-properties)
-   [Propiedades del descodificador de vídeo](#video-decoder-properties)
-   [Propiedades del descodificador de audio](#audio-decoder-properties)
-   [Propiedades del codificador de vídeo](#video-encoder-properties)
-   [Propiedades del codificador de audio](#audio-encoder-properties)
-   [Propiedades del codificador de vídeo MPEG](#mpeg-video-encoder-properties)
-   [Propiedades del codificador de audio MPEG](#mpeg-audio-encoder-properties)
-   [Propiedades del descodificador de audio Dolby digital](#dolby-digital-audio-decoder-properties)
-   [Propiedades del codificador de audio Dolby digital](#dolby-digital-audio-encoder-properties)
-   [Propiedades de procesamiento de señal digital (DSP)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Propiedades de audio comunes

Estas propiedades se aplican tanto a los codificadores de audio como a los descodificadores de audio.



| Propiedad                                                      | Descripción                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Obtiene la configuración de los altavoces para los canales de audio en el flujo de bits de audio. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Obtiene el número de canales en el flujo de bits de audio.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Obtiene la velocidad de muestra de la secuencia de bits de audio, en muestras por segundo.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Especifica si el audio se codifica en Dolby Surround.                      |



 

### <a name="common-decoder-properties"></a>Propiedades comunes del descodificador

Estas propiedades se aplican a los descodificadores de audio y descodificadores de vídeo.



| Propiedad                                                            | Descripción                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Especifica el formato de entrada actual para el descodificador.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Obtiene la velocidad de bits media actual del descodificador.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Especifica el formato de salida para el descodificador.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Especifica la clase del servicio Programador de clases multimedia (MMCSS) para el subproceso de descodificación. |



 

### <a name="common-encoder-properties"></a>Propiedades comunes del codificador

Estas propiedades se aplican a codificadores de audio y codificadores de vídeo.



| Propiedad                                                                          | Descripción                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Especifica el esquema de codificación.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Especifica el nivel inicial del búfer de codificación.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Especifica el nivel final del búfer de codificación al final del proceso de codificación.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Especifica el tamaño del búfer usado durante la codificación.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Especifica el formato de destino de un codificador.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Especifica si el flujo de salida se debe estructurar para que la secuencia codificada tenga una latencia de descodificación baja. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Especifica la velocidad de bits máxima.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Especifica la velocidad de bits media.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Especifica el intervalo de tiempo durante el que se aplica la velocidad de bits promedio.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Especifica la velocidad de bits mínima.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Especifica el número de pasos de codificación que admite el codificador.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Detiene el paso de codificación actual o consulta si la fase de codificación actual es la última.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Inicia la primera fase de codificación.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Especifica el nivel de calidad de la codificación.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Especifica el equilibrio entre la calidad y la velocidad de codificación.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Especifica el modo de control de velocidad.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Especifica si la aplicación requiere un rendimiento de codificación en tiempo real.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Especifica si el codificador descarta grupos parciales de imágenes (GOP) al final de la secuencia.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Especifica el tipo de flujo de salida generado por un multiplexor.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Especifica el número de pasos de codificación completados.                                                              |



 

### <a name="video-decoder-properties"></a>Propiedades del descodificador de vídeo



| Propiedad                                                                                | Descripción                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo H. 264.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo MPEG-2.            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo VC-1.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Especifica si el descodificador quita las tramas dentro de las que faltan fotogramas de referencia. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Obtiene o establece la velocidad de descodificación de vídeo.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Obtiene el tamaño de la imagen descodificada, en píxeles.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Especifica cómo se entrelaza la secuencia de vídeo descodificada.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Especifica la relación de aspecto de píxeles de la secuencia de vídeo descodificada.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Especifica el modo de desentrelazado de software del descodificador.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Especifica el nivel de ahorro de energía.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Habilita o deshabilita el modo de generación de miniaturas.                                  |



 

### <a name="audio-decoder-properties"></a>Propiedades del descodificador de audio



| Propiedad                                                                        | Descripción                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Especifica si un descodificador AAC usa ecuaciones downmix de estéreo estándar MPEG-2/MPEG-4, o usa un downmix no estándar. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Especifica si el audio de 2 canales se codifica como estéreo o dual mono.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Especifica cómo el descodificador Reproduce audio mono dual.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Habilita o deshabilita el control de intervalo dinámico en un descodificador AAC.                                                           |



 

### <a name="video-encoder-properties"></a>Propiedades del codificador de vídeo



| Propiedad                                                                                        | Descripción                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Especifica el sistema de vídeo del contenido de origen.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Devuelve el número de fotogramas de vídeo que se han codificado.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Devuelve la velocidad media de fotogramas del contenido del vídeo.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Devuelve el número de fotogramas de vídeo que el codificador ha recibido.                                                         |
| [**AVEncVideoCBRMotionTradeoff**](avencvideocbrmotiontradeoff-property.md)                     | Especifica el equilibrio entre las imágenes de movimiento y las imágenes fijas.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Especifica el tamaño de las unidades de acceso al vídeo.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Especifica el campo que se muestra en primer lugar.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Especifica el tamaño de la secuencia de vídeo cuando se descodifica.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Especifica el ancho y el alto del vídeo codificado, si se recorta el vídeo.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo se recorta.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Invierte el orden de los campos entrelazados en el vídeo de origen.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Especifica si los fotogramas de entrada son progresivos o entrelazados.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Especifica el valor de la marca Drop-Frame en el encabezado GOP.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Especifica el número de fotograma inicial en el encabezado GOP.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Especifica el número de hora de inicio en el encabezado GOP.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Especifica el número de minutos de inicio en el encabezado GOP.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Especifica el segundo número de inicio en el encabezado GOP.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Especifica la resolución de cromas del vídeo de entrada.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Especifica la colocación cromada para el vídeo de entrada.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Especifica las condiciones de iluminación previstas para ver el vídeo de entrada.                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | Especifica el intervalo nominal del vídeo de entrada.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Especifica el color primario del vídeo de entrada.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Especifica la función de conversión de RGB a R'G'B ' para el vídeo de entrada                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Especifica la matriz de conversión del espacio de colores de Y'Cb'Cr al espacio de colores de R'G'B para el vídeo de entrada.         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | Especifica si el codificador realiza telecine inversa.                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | Establece el umbral en el que el codificador considera que un campo de vídeo es redundante.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Especifica el número máximo de fotogramas entre fotogramas clave.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Especifica el número de campos que se van a codificar.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Especifica el número de campos que se van a omitir durante la codificación.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Especifica la resolución de cromas del vídeo codificado.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Especifica la colocación cromada para el vídeo codificado.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Especifica las condiciones de iluminación previstas para ver el vídeo codificado.                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | Especifica el intervalo nominal del vídeo codificado.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Especifica el color primario del vídeo codificado.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Especifica la función de conversión de RGB a R'G'B ' para el vídeo codificado.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Especifica la matriz de conversión del espacio de colores de Y'Cb'Cr al espacio de colores de R'G'B para el vídeo codificado.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Especifica si el codificador convierte la velocidad de fotogramas cuando la velocidad de fotogramas de salida no coincide con la velocidad de fotogramas de entrada. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Especifica cómo el codificador entrelaza el vídeo de salida.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Especifica la relación de aspecto de píxeles.                                                                                     |
| [**AVEncVideoSourceFilmContent**](avencvideosourcefilmcontent-property.md)                     | Especifica si el origen original del vídeo de entrada era película o vídeo.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Especifica si el vídeo es monocromo (blanco y negro) o contiene color.                                        |



 

### <a name="audio-encoder-properties"></a>Propiedades del codificador de audio



| Propiedad                                                                        | Descripción                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Especifica si el audio de 2 canales se codifica como estéreo o dual mono.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Especifica si el contenido de audio contiene música o voz.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Especifica el número de muestras de audio que se van a codificar.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Especifica el número de muestras de audio que va a omitir el codificador.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Especifica el canal de audio que se asigna al canal *N* en la secuencia de audio codificada. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Especifica la velocidad de bits media de la secuencia de audio codificada.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Devuelve el promedio de bits por segundo del audio codificado.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Devuelve el nivel de volumen medio del contenido de audio.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Devuelve el nivel de volumen más alto que estaba presente en el contenido de audio.             |



 

### <a name="mpeg-video-encoder-properties"></a>Propiedades del codificador de vídeo MPEG



| Propiedad                                                                                    | Descripción                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Especifica si el codificador agrega un código de fin de secuencia al final de la secuencia.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Especifica el número predeterminado de fotogramas B consecutivos entre los fotogramas I y P.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Especifica si el codificador genera campos codificados o fotogramas codificados.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Especifica si el codificador genera encabezados de extensión de presentación de imágenes.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Especifica si el codificador genera encabezados de extensión de imagen.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Especifica si el codificador genera encabezados de extensión de presentación de secuencias.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Especifica si el codificador genera encabezados de extensión de secuencia.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Especifica si el codificador genera encabezados de extensión escalables de secuencia.         |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                         | Especifica si el codificador produce GOP de apertura GOP o Closed.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Especifica el número de GOP entre los encabezados de la secuencia.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Especifica el número máximo de imágenes de un encabezado GOP al siguiente encabezado GOP. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Especifica la precisión de los coeficientes del controlador de dominio.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Especifica la tabla de codificación de longitud variable (VLC) que se va a usar para la codificación de entropía.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Especifica el nivel MPEG-2.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Especifica el perfil MPEG-2.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Especifica si la escala del cuantificador es lineal o no lineal.                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | Especifica la matriz de cuantificación de croma para intra macrobloques.                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Especifica la matriz de cuantificación de croma para macrobloques no intra.                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Especifica la matriz de cuantificación de luminancia para intra macrobloques.                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Especifica la matriz de cuantificación de luminancia para macrobloques no intra.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Especifica el patrón de examen de adaptativo macrobloque.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Especifica cómo se comporta el codificador cuando detecta una nueva escena.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Especifica si el codificador utiliza vectores de movimiento de ocultación.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>Propiedades del codificador de audio MPEG



| Propiedad                                                                                  | Descripción                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Especifica el modo de codificación de audio MPEG-1.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Especifica el valor predeterminado para el bit de copyright.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Especifica el tipo de filtro de desacentuación que se debe usar al descodificar.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Especifica la capa de audio MPEG.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Especifica el valor predeterminado para el bit original.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Establece el valor del bit de usuario privado.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Propiedades del descodificador de audio Dolby digital



| Propiedad                                                                      | Descripción                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Especifica el corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico.  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Especifica el modo de control de compresión.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Propiedades del codificador de audio Dolby digital



| Propiedad                                                                                        | Descripción                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | Especifica el tipo de conversión analógica a digital (a/D).                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Especifica el nivel central de downmix.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Especifica si se aplica un filtro de paso bajo a los canales de entrada principales.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Especifica la marca de copyright.                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Especifica si se aplica un filtro de paso alto de bloqueo de DC.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Especifica el nivel de normalización del cuadro de diálogo.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Especifica si se desacentua digitalmente.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Especifica el perfil de control de intervalo dinámico.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Especifica el modo de auricular.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Especifica si se aplica un filtro de paso bajo al canal de efecto de baja frecuencia (LFE). |
| [**AVEncDDLoRoCenterMixLvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | Especifica el cambio de nivel que se aplica al canal central para el downmixing de carga.     |
| [**AVEncDDLoRoSurroundMixLvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | Especifica el cambio de nivel que se aplica a los canales de envolvente para el downmixing de carga.  |
| [**AVEncDDLtRtCenterMixLvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | Especifica el cambio de nivel que se aplica al canal central para LT/RT downmixing.     |
| [**AVEncDDLtRtSurroundMixLvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | Especifica el cambio de nivel que se aplica a los canales de envolvente para LT/RT downmixing.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Especifica la marca fragmentada original.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Especifica el modo downmix estéreo preferido.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Especifica la marca de información de producción de audio.                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Especifica el nivel de combinación.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Especifica el tipo de habitación.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Especifica la configuración de protección de sobremodulación de RF.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Especifica el servicio de audio.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Especifica si los canales envolventes están atenuados antes de la codificación.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Especifica si se aplica un desplazamiento de fase de 90 grados a los canales envolventes.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Especifica el nivel de combinación hacia abajo.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Especifica si la secuencia de audio se codifica en el código envolvente EX.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Propiedades de procesamiento de señal digital (DSP)



| Propiedad                                                                | Descripción                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | Habilita o deshabilita la ecualización de sonoridad |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Habilita o deshabilita el relleno del altavoz          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de códecs](codec-api-reference.md)
</dt> </dl>

 

 



