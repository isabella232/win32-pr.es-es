---
description: El filtro del codificador de vídeo MPEG-2 de Microsoft codifica el vídeo MPEG-2 y MPEG-1.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Codificador de vídeo MPEG-2 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c96db605586c6abf0f51537689a9365df2842c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686370"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Codificador de vídeo MPEG-2 de Microsoft

El filtro del codificador de vídeo MPEG-2 de Microsoft codifica el vídeo MPEG-2 y MPEG-1.

Para codificar y multiplexar secuencias de audio/vídeo, use el filtro del [**codificador MPEG-2 de Microsoft**](microsoft-mpeg-2-encoder.md) , que encapsula las funciones de este filtro y el filtro del [**codificador de audio MPEG-2 de Microsoft**](microsoft-mpeg-2-audio-encoder.md) .

> [!Note]  
> Este filtro no se admite en las plataformas basadas en IA-64.

 



Información de filtro

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de medios de anclaje de entrada

**MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ i420**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ IYUV**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ RGB24**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ UYVY**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ YUY2**<br/> **MEDIATYPE \_ Vídeo**, **MEDIASUBTYPE \_ YV12**<br/>

Interfaces de PIN de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de anclaje de salida

**MEDIATYPE \_ Stream**, **\_ \_ vídeo MEDIASUBTYPE MPEG2**<br/> **MEDIATYPE \_ Stream**, **\_ \_ programa MEDIASUBTYPE MPEG2**<br/> **MEDIATYPE \_ Stream**, **\_ \_ transporte MPEG2 MEDIASUBTYPE**<br/> **MEDIATYPE \_ Vídeo**, **\_ \_ vídeo MEDIASUBTYPE MPEG2**<br/>

Interfaces de clavija de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Identificador CLSID

**CLSID \_ de CMPEG2EncoderVideoDS** (declarado en wmcodecdsp. h)

Executable

msmpeg2enc.dll

[Fundament](merit.md)

**MÉRITO \_ \_ no se \_ usa**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

El codificador de vídeo MPEG-2 puede producir los siguientes tipos de resultados:

-   Flujo básico de vídeo
-   Vídeo en una secuencia de programa MPEG-2
-   Vídeo en una secuencia de transporte MPEG-2

Admite los siguientes perfiles y niveles de MPEG-2:



| Perfil        | Niveles                     | Observaciones                                            |
|----------------|----------------------------|----------------------------------------------------|
| Perfil simple | Método Main                       |                                                    |
| Perfil Main   | Bajo, principal, alto, alto-1440 |                                                    |
| Perfil alto   | Principal, alto, alto-1440      | Sin escalabilidad o compatibilidad con 4:2:2/4:4:4 (solo 4:2:0) |
| Perfil 4:2:2  | Principal, alto                 | Sin escalabilidad o compatibilidad con 4:2:2 (solo 4:2:0)       |



 

### <a name="codec-properties"></a>Propiedades de códec

El filtro admite las siguientes propiedades a través de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Propiedad                                                                                      | Valor predeterminado                                                          | Valores admitidos                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | Vídeo MPEG-2                                                     | **CODECAPI \_ GUID \_ AVEncMPEG1Video**<br/> **CODECAPI \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 bits                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Sin especificar                                                      | **CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified** (sin restricción de formato)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-video)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatVCD** (CD de vídeo)<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9,8 millones (9,8 Mbits/segundo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7 millones (7,0 Mbits/segundo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1:100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0:100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **eAVEncCommonRateControlMode \_ CBR**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **calidad de eAVEncCommonRateControlMode \_**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Sin especificar                                                      | eAVEncInputVideoSystem no \_ especificado<br/> eAVEncInputVideoSystem \_ PAL<br/> \_NTSC eAVEncInputVideoSystem<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0:2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Modo de marco                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0:1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 fotogramas (campos 36) para NTSC; 15 fotogramas (30 campos) en caso contrario. | 1:30; Ver comentarios                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8:10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Alto                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Método Main                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eAVEncVideoSourceScan \_ entrelazado**<br/> **\_progresiva eAVEncVideoSourceScan**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Igual que el origen                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1          | 0 o [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                                                                                                                                                         |
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

Establezca las propiedades restantes en cualquier orden. (Sin embargo, consulte la [estructura GOP](#gop-structure)).

Es posible establecer propiedades mientras se ejecuta el gráfico de filtros. Hay un retraso de al menos un GOP antes de que la nueva configuración surta efecto.

### <a name="encoder-operation"></a>Operación del codificador

Al codificar vídeo MPEG-1, el codificador establece automáticamente el código de **\_ \_ marcador de parámetros restringidos** de 1 bit en el encabezado de secuencia si se cumplen todas las restricciones.

Si es necesario, el codificador redondea las dimensiones de vídeo de entrada para que las dimensiones de vídeo de salida coincidan con los requisitos de MPEG. En el vídeo progresivo, las dimensiones de salida se redondean a un múltiplo de 16 en ancho y alto. En el caso de vídeo entrelazado, el ancho se redondea a un múltiplo de 16 y el alto se redondea a un múltiplo de 32. Esta operación de redondeo usa el relleno según sea necesario.

Si el vídeo está entrelazado, el codificador realiza la detección automática de telecine (desplegable 3:2). El vídeo de entrada puede contener pares de imagen de campo, además de fotogramas entrelazados.

El formato interno del codificador es 4:2:0 IYUV (idéntico a i420). Puede realizar la conversión de colores de los formatos de vídeo YUY2, YV12, UYVY y RGB-24.

Para restringir la fragmentada a un formato de destino (DVD o VCD), establezca la propiedad [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) . Si esta propiedad tiene un valor distinto de **GUID \_ AVEncCommonFormatUnSpecified**, el codificador limita la sintaxis MPEG a la que permite el formato de destino.

Para la codificación en directo, establezca la propiedad [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) en cero. Esto hace que el codificador optimice la velocidad.

### <a name="encoding-modes"></a>Modos de codificación

El codificador admite varios modos de codificación:

-   Velocidad de bits constante de un paso (CBR).
-   Velocidad de bits variable (VBR) basada en la calidad de un paso, con un tamaño de paso de cuantificador constante. En este modo, el codificador intenta cumplir un nivel de calidad de destino, hasta una velocidad de bits máxima.
-   VBR con restricción pico de una sola fase. En este modo, el codificador intenta alcanzar una velocidad de bits media de destino dentro de ciertos límites internos.

Para configurar el modo de codificación, establezca las siguientes propiedades:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Propiedades</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br/> <a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
<tr class="even">
<td>VBR basada en la calidad</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br/> <a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/>
<blockquote>
[!Note]<br />
En este modo, no se usan las propiedades <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> y <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> . Se supone que la velocidad de bits mínima es cero.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>VBR máxima restringida</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br/> <a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br/> <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> No se admite VBR de dos pasos.

 

### <a name="aspect-ratio"></a>Relación de aspecto

La relación de aspecto de la pantalla y la relación de aspecto de píxel (PAR) se relacionan con la fórmula siguiente:

<dl> Mostrar relación de aspecto = PAR × (ancho de imagen/alto de imagen)  
</dl>

El codificador usa esta fórmula para calcular el valor de la relación de aspecto de PEL \_ \_ para BITSTREAMS de MPEG-1 o la \_ \_ información de relación de aspecto para MPEG-2 bitstreams. (Vea ISO/IEC 11172 e ISO/IEC 138181-2, respectivamente).

El codificador intenta la siguiente configuración, en orden:

1.  Si la aplicación establece la propiedad [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) en cualquier momento antes de que se ejecute el gráfico de filtros, esta propiedad se usa para el par.
2.  De lo contrario, si los miembros **dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) son distintos de cero, estos miembros se utilizan para la relación de aspecto de la pantalla y el par se calcula a partir de la relación de aspecto de la pantalla.
3.  Si ninguno de estos valores está presente, se supone que el PAR es 1,0 y la relación de aspecto de la pantalla se calcula en consecuencia.

En el modo de codificación en directo ([**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) igual a cero), la relación de aspecto de la pantalla debe ser 4:3 o 16:9, con un valor predeterminado de 4:3. Si la relación de aspecto de presentación calculada no es 4:3 o 16:9, el codificador usa el valor 4:3.

### <a name="gop-structure"></a>GOP (estructura)

Para especificar la estructura de grupo de imágenes (GOP), establezca las siguientes propiedades en orden:

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

Según esta configuración, el codificador produce una de las siguientes estructuras GOP:



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | GOP (estructura) |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 2                                                                             | IBBPBBP...    |



 

La estructura GOP predeterminada es IBBPBBP... con un tamaño GOP de 15 fotogramas.

Si la aplicación restringe el formato de destino a DVD (a través de la propiedad [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) ) y establece la propiedad [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) en NTSC o PAL, el codificador admite los siguientes tamaños GOP:



| Sistema de vídeo | Tamaños de GOP válidos | Tamaño de GOP predeterminado |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (36 campos)   |
| PAL          | 1-15            | 15 (30 campos)   |



 

### <a name="codec-property-change-lists"></a>Listas de cambios de propiedades de códec

Al establecer el valor de una propiedad de códec se puede cambiar el intervalo válido de otra propiedad. (Por ejemplo, la restricción del formato de destino restringe la velocidad de bits promedio). Siempre que la aplicación establece una propiedad, el codificador comprueba si otras propiedades están fuera de su intervalo válido. Si es así, el codificador restablece esa propiedad en su nuevo valor predeterminado. Para recibir notificaciones cuando esto sucede, haga lo siguiente:

1.  Llame a [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) con el valor **CODECAPI \_ CHANGELISTS**.
2.  Use la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para supervisar los eventos del gráfico de filtros.
3.  Si el intervalo o el valor predeterminado de una propiedad cambia, el codificador envía un evento de [**\_ \_ evento CODECAPI de EC**](ec-codecapi-event.md) con una lista de propiedades cambiadas.

### <a name="iencoderapi-support"></a>Compatibilidad con IEncoderAPI

Por compatibilidad con versiones anteriores, el filtro admite las siguientes propiedades a través de la interfaz **IEncoderAPI** :



| Propiedad                       | Descripción                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **\_velocidad de bits ENCAPIPARAM**       | Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).         |
| **\_velocidad de bits máxima de ENCAPIPARAM \_** | Equivalente a [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md).           |
| **\_modo de velocidad de bits ENCAPIPARAM \_** | Equivalente a [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md). |



 

Al establecer la propiedad del **\_ \_ modo de velocidad de bits ENCAPIPARAM** , los valores se asignan de la siguiente manera:



| **\_modo de velocidad de bits ENCAPIPARAM \_** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **eAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | Vea la Nota.                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> Actualmente, el codificador de vídeo MPEG-2 no admite el modo de codificación de **VariableBitRateAverage** . Si establece este valor, el codificador tiene como valor predeterminado la codificación CBR (**eAVEncCommonRateControlMode \_ CBR**).

 

Al obtener la propiedad del **\_ \_ modo de velocidad de bits ENCAPIPARAM** , los valores se asignan de la siguiente manera:



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **\_modo de velocidad de bits ENCAPIPARAM \_** |
|---------------------------------------------------------------------------|--------------------------------|
| **eAVEncCommonRateControlMode \_ CBR**                                      | **ConstantBitRate**            |
| **calidad de eAVEncCommonRateControlMode \_**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Limitaciones

Actualmente, el codificador no admite ninguna de las siguientes características:

-   Generación de paquetes de flujo elemental (PES) de paquetes.
-   Conversión de velocidad de fotogramas. El flujo de entrada debe tener una velocidad de fotogramas válida para un fragmentada de MPEG-2.
-   Extensiones de velocidad de fotogramas para MPEG-2 (extensión de velocidad de **fotogramas \_ \_ \_ n**, **extensión de velocidad de fotogramas \_ \_ \_ d**).
-   Posiciones de búfer de entrada y salida (VBV) para un clip.
-   Inserción de datos de línea 21 (información de subtítulos cerrados) en el flujo elemental de vídeo.
-   Establecer el campo de **\_ código de tiempo** de 25 bits en el encabezado GOP para MPEG-2.
-   Filtro de desruido.
-   Administración de derechos digitales (DRM).

El codificador presenta una latencia de codificación de al menos un GOP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de medios de demultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
