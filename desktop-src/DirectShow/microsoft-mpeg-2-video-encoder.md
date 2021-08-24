---
description: El filtro Microsoft MPEG-2 Video Encoder codifica vídeo MPEG-2 y MPEG-1.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Codificador de vídeo Microsoft MPEG-2 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7b70b9a754aefda3158ae355eb84c24b71b7e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474721"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Codificador de vídeo Microsoft MPEG-2

El filtro Microsoft MPEG-2 Video Encoder codifica vídeo MPEG-2 y MPEG-1.

Para codificar y multiplexar secuencias de audio y vídeo, use el filtro Codificador [**MPEG-2**](microsoft-mpeg-2-encoder.md) de Microsoft, que encapsula las funciones de este filtro y del filtro [**Microsoft MPEG-2 Audio Encoder.**](microsoft-mpeg-2-audio-encoder.md)

> [!Note]  
> Este filtro no se admite en plataformas basadas en IA-64.

 



Filtrar información

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de medios de pin de entrada

**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ I420**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ IYUV**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ RGB24**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ UYVY**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ YUY2**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ YV12**<br/>

Interfaces de pin de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de pin de salida

**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/> **MEDIATYPE \_ Vídeo**, **VÍDEO \_ MPEG2 \_ DE MEDIASUBTYPE**<br/>

Interfaces de pin de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2EncoderVideoDS** (declarado en wmcodecdsp.h)

Executable

msmpeg2enc.dll

[Mérito](merit.md)

**NO USE EL VALOR DE NO \_ \_ \_ USE.**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Comentarios

El codificador de vídeo MPEG-2 puede generar los siguientes tipos de salida:

-   Secuencia elemental de vídeo
-   Vídeo en una secuencia de programa MPEG-2
-   Vídeo en una secuencia de transporte MPEG-2

Admite los siguientes perfiles y niveles MPEG-2:



| Perfil        | Niveles                     | Comentarios                                            |
|----------------|----------------------------|----------------------------------------------------|
| Perfil simple | Método Main                       |                                                    |
| Perfil Main   | Baja, Principal, Alta, Alta-1440 |                                                    |
| Perfil alto   | Main, High, High-1440      | Sin escalabilidad o compatibilidad con 4:2:2/4:4:4 (solo 4:2:0) |
| Perfil 4:2:2  | Main, High                 | Sin escalabilidad ni compatibilidad con 4:2:2 (solo 4:2:0)       |



 

### <a name="codec-properties"></a>Propiedades del códec

El filtro admite las siguientes propiedades a través [**de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Propiedad                                                                                      | Valor predeterminado                                                          | Valores admitidos                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | Vídeo MPEG-2                                                     | **CODECAPI \_ GUID \_ AVEncMPEG1Video**<br/> **CODECAPI \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Sin especificar                                                      | **CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified** (sin restricción de formato)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-Video)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatVCD** (CD de vídeo (VCD))<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9800000 (9,8 Mbits/segundo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7000000 (7,0 Mbits/segundo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1 — 100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0 — 100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **CBR eAVEncCommonRateControlMode \_**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **Calidad de eAVEncCommonRateControlMode \_**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Sin especificar                                                      | eAVEncInputVideoSystem \_ Sin especificar<br/> eAVEncInputVideoSystem \_ PAL<br/> eAVEncInputVideoSystem \_ INPUT<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0 — 2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Modo de fotograma                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0 — 1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 fotogramas (36 campos) para HRS; 15 fotogramas (30 campos) en caso contrario. | 1 — 30; vea Comentarios                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8 — 10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Alto                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Método Main                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eAVEncVideoSourceScan \_ entrelazado**<br/> **eAVEncVideoSourceScan \_ Progresiva**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNorange**](avencvideoinputcolornominalrange-property.md)         | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize:**](avencmpvgopsize-property.md) 1          | 0 o [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) : 1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | Debe ser igual que la velocidad de fotogramas de entrada.                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | Igual que la entrada                                                    | **eAVEncVideoOutputScan \_ SameAsInput**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

Se recomienda establecer las propiedades en el orden siguiente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

Establezca las propiedades restantes en cualquier orden. (Sin embargo, vea [ESTRUCTURA DE GOP).](#gop-structure)

Es posible establecer propiedades mientras se ejecuta el gráfico de filtros. Hay un retraso de al menos un GOP antes de que la nueva configuración suba efecto.

### <a name="encoder-operation"></a>Operación del codificador

Al codificar vídeo MPEG-1, el codificador establece automáticamente el código de marca de parámetros restringidos de 1 bit en el encabezado de secuencia si se cumplen todas las restricciones. **\_ \_**

Si es necesario, el codificador redondea las dimensiones de vídeo de entrada para que las dimensiones de vídeo de salida coincidan con los requisitos de MPEG. En el caso del vídeo progresiva, las dimensiones de salida se redondea hasta un múltiplo de 16 tanto en ancho como en alto. En el caso del vídeo entrelazado, el ancho se redondea hasta un múltiplo de 16 y el alto se redondea hasta un múltiplo de 32. Esta operación de redondeo usa el relleno según sea necesario.

Si el vídeo está entrelazado, el codificador realiza la detección automática de teleconferencia (3:2 de extracción). El vídeo de entrada puede contener pares de imágenes de campo, además de marcos entrelazados.

El formato interno del codificador es 4:2:0 IYUV (idéntico a I420). Puede realizar la conversión de color de los formatos de vídeo YUY2, YV12, UYVY y RGB-24.

Para restringir la secuencia de bits a un formato de destino (DVD o VCD), establezca la [**propiedad AVEncCommonFormatConstraint.**](avenccommonformatconstraint-property.md) Si esta propiedad tiene un valor distinto de **\_ GUID AVEncCommonFormatUnSpecified,** el codificador limita la sintaxis MPEG a la permitida por el formato de destino.

Para la codificación en vivo, establezca la propiedad [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) en cero. Esto hace que el codificador optimice la velocidad.

### <a name="encoding-modes"></a>Modos de codificación

El codificador admite varios modos de codificación:

-   Velocidad de bits constante de un paso (CBR).
-   Velocidad de bits variable basada en la calidad de un solo paso (VBR), mediante un tamaño de paso de cuantificador constante. En este modo, el codificador intenta cumplir un nivel de calidad de destino, hasta una velocidad de bits máxima.
-   VBR con restricción máxima de un solo paso. En este modo, el codificador intenta lograr una velocidad de bits media objetivo dentro de determinados límites internos.

Para configurar el modo de codificación, establezca las siguientes propiedades:




| Modo | Propiedades | 
|------|------------|
| CBR | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br /><a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br /><a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br /> | 
| VBR basado en calidad | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br /><a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br /><a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br /><blockquote>[!Note]<br />En este modo, no se usan las propiedades <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> y <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate.</strong></a> Se supone que la velocidad de bits mínima es cero.</blockquote><br /> | 
| VBR con restricciones máximas | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br /><a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br /><a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br /><a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br /><a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br /> | 




 

> [!Note]  
> No se admite VBR de dos pases.

 

### <a name="aspect-ratio"></a>Relación de aspecto

La relación de aspecto de presentación y la relación de aspecto de píxeles (PAR) están relacionadas con la fórmula siguiente:

<dl> Relación de aspecto de presentación = par × (ancho de imagen/alto de imagen)  
</dl>

El codificador usa esta fórmula para calcular el valor de la relación de aspecto de las secuencias de bits MPEG-1 o la información de relación de aspecto para las secuencias de \_ \_ bits \_ \_ MPEG-2. (Vea ISO/IEC 11172 e ISO/IEC 138181-2, respectivamente).

El codificador prueba la siguiente configuración, en orden:

1.  Si la aplicación establece la propiedad [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) en cualquier momento antes de que se ejecute el gráfico de filtros, esta propiedad se usa para el PAR.
2.  De lo contrario, si los miembros **dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) son distintos de cero, estos miembros se usan para la relación de aspecto de presentación y el PAR se calcula a partir de la relación de aspecto de presentación.
3.  Si ninguno de estos valores está presente, se supone que el PAR es 1,0 y la relación de aspecto de la presentación se calcula en consecuencia.

En el modo de codificación en vivo [**(AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) igual a cero), la relación de aspecto de la presentación debe ser 4:3 o 16:9, con un valor predeterminado de 4:3. Si la relación de aspecto de presentación calculada no es 4:3 ni 16:9, el codificador usa el valor 4:3.

### <a name="gop-structure"></a>Estructura de GOP

Para especificar la estructura del grupo de imágenes (GOP), establezca las siguientes propiedades en orden:

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

En función de esta configuración, el codificador genera una de las siguientes estructuras de GOP:



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | Estructura de GOP |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                         | 2                                                                             | IBBPBBP...    |



 

La estructura predeterminada de GOP es IBBPBBP... con un tamaño de GOP de 15 fotogramas.

Si la aplicación restringe el formato de destino a DVD (a través de la propiedad [**AVEncCommonFormatConstraint)**](avenccommonformatconstraint-property.md) y establece la propiedad [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) en CLUS o PAL, el codificador admite los siguientes tamaños de GOP:



| Sistema de vídeo | Tamaños de GOP válidos | Tamaño predeterminado de GOP |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (36 campos)   |
| PAL          | 1-15            | 15 (30 campos)   |



 

### <a name="codec-property-change-lists"></a>Listas de cambios de propiedades de códec

Establecer el valor de una propiedad de códec puede cambiar el intervalo válido de otra propiedad. (Por ejemplo, restringir el formato de destino restringe la velocidad de bits media). Cada vez que la aplicación establece una propiedad, el codificador comprueba si alguna otra propiedad ahora está fuera de su intervalo válido. Si es así, el codificador restablece esa propiedad a su nuevo valor predeterminado. Para recibir notificaciones cuando esto ocurra, haga lo siguiente:

1.  Llame [**a ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) con el valor **CODECAPI \_ CHANGELISTS**.
2.  Use la [**interfaz IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para supervisar eventos del gráfico de filtros.
3.  Si cambia el intervalo o el valor predeterminado de una propiedad, el codificador envía un evento [**\_ EC CODECAPI \_ EVENT**](ec-codecapi-event.md) con una lista de propiedades modificadas.

### <a name="iencoderapi-support"></a>Compatibilidad con IEncoderAPI

Por compatibilidad con versiones anteriores, el filtro admite las siguientes propiedades a través de la **interfaz IEncoderAPI:**



| Propiedad                       | Descripción                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **VELOCIDAD DE BITS DE ENCAPIPARAM \_**       | Equivalente a [**AVEncCommonMeanBitRate.**](avenccommonmeanbitrate-property.md)         |
| **VELOCIDAD DE BITS MÁXIMA DE ENCAPIPARAM \_ \_** | Equivalente a [**AVEncCommonMaxBitRate.**](avenccommonmaxbitrate-property.md)           |
| **MODO DE VELOCIDAD DE BITS ENCAPIPARAM \_ \_** | Equivalente a [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md). |



 

Al establecer la **propiedad ENCAPIPARAM \_ BITRATE \_ MODE,** los valores se asignan de la siguiente manera:



| **MODO DE VELOCIDAD DE BITS ENCAPIPARAM \_ \_** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **CBR eAVEncCommonRateControlMode \_**                                      |
| **VariableBitRateAverage**     | Vea la Nota.                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> Actualmente, el codificador de vídeo MPEG-2 no admite el modo de codificación **VariableBitRateAverage.** Si establece este valor, el codificador tiene como valor predeterminado la codificación CBR (**eAVEncCommonRateControlMode \_ CBR**).

 

Al obtener la **propiedad ENCAPIPARAM \_ BITRATE \_ MODE,** los valores se asignan de la siguiente manera:



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **MODO DE VELOCIDAD DE BITS ENCAPIPARAM \_ \_** |
|---------------------------------------------------------------------------|--------------------------------|
| **CBR eAVEncCommonRateControlMode \_**                                      | **ConstantBitRate**            |
| **Calidad de eAVEncCommonRateControlMode \_**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Limitaciones

Actualmente, el codificador no admite ninguna de las siguientes características:

-   Generación de paquetes de flujo básico en paquetes (PES).
-   Conversión de velocidad de fotogramas. El flujo de entrada debe tener una velocidad de fotogramas válida para una secuencia de bits MPEG-2.
-   Extensiones de velocidad de fotogramas para MPEG-2 (extensión de velocidad **\_ de \_ \_ fotogramas n**, extensión de velocidad de **\_ \_ \_ fotogramas d**).
-   Posiciones del búfer de entrada/salida (VBV) para un clip.
-   Inserción de datos de línea 21 (información de subtítulos) en la secuencia elemental de vídeo.
-   Establecer el campo de código de tiempo de 25 bits en el encabezado GOP para MPEG-2. **\_**
-   Filtro de Denoise.
-   Administración de derechos digitales (DRM).

El codificador introduce una latencia de codificación de al menos un GOP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de demultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
