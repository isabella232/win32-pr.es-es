---
description: El descodificador de vídeo Media Foundation H.265 es una transformación de Media Foundation que admite la descodificación de contenido H.265/HEVC en formato anexo B y se puede usar en la reproducción de archivos mp4 y m2ts.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Descodificador de vídeo H.265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c764353e04da0113b51c4efb0d39fad02c84b98859e154d24866229c3a524385
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777205"
---
# <a name="h265--hevc-video-decoder"></a>Descodificador de vídeo H.265/HEVC

El descodificador de vídeo Media Foundation H.265 es una transformación de [Media Foundation](media-foundation-transforms.md) que admite la descodificación de contenido H.265/HEVC en formato anexo B y se puede usar en la reproducción de archivos mp4 y m2ts.

El descodificador de vídeo H.265 expone las interfaces siguientes.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (compatible con Windows 8)
-   [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Para crear una instancia del descodificador, llame a la [**función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) [**o MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

## <a name="input-types"></a>Tipos de entrada

El tipo de entrada debe contener al menos los dos atributos siguientes:



| Atributo                                                 | Descripción                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md) | **VÍDEO \_ MFMediaType**                                                                        |
| [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ HEVC](video-subtype-guids.md) o MFVideoFormat \_ HEVC \_ ES |



 

El primer subtipo multimedia, MFVideoFormat HEVC, indica que los ejemplos multimedia llevan la secuencia de bits H.265 con códigos de inicio y que la secuencia tiene \_ SPS o PPS intercalados. Se supone que hay un fotograma por muestra.

El subtipo multimedia MFVideoFormat HEVC ES indica que las muestras multimedia llevan una secuencia de bits \_ H.265 elemental, donde cada muestra puede contener una imagen parcial, varias imágenes, algunas imágenes más una imagen \_ parcial.

Los tipos de medios de entrada no pueden cambiar dinámicamente entre dos tipos. El descodificador puede detectar cambios en el formato de salida en vuelo en función de la sintaxis básica del flujo (relación de aspecto, dimensión, marcas de interlace, información de colorimetría) y desencadenar los cambios de tipo de medio de salida correspondientes.

Para el tipo de medio de entrada, el descodificador espera que el origen establezca el perfil correcto. Por ejemplo, si el contenido va a ser de 10 bits, el tipo de medio de entrada debe especificar el perfil como Main10.

## <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes subtipos de salida:

-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ P010**

Para obtener más información sobre estos subtipos, vea [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Transformar atributos

El descodificador H.265 implementa el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Las aplicaciones pueden usar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                                       | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                     | Habilita o deshabilita el modo de decodificación de baja latencia.                                                                                |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                           | Establece el número de subprocesos de trabajo utilizados por el descodificador.                                                                        |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Habilita o deshabilita el modo de generación de miniaturas.                                                                                |
| [MF \_ NALU \_ LENGTH \_ SET](mf-nalu-length-set.md)                                                 | Indica que la información de longitud de NALU se enviará como blob con cada ejemplo de H.265 comprimido.                              |
| [INFORMACIÓN \_ DE LONGITUD DE MF NALU \_ \_](mf-nalu-length-information.md)                                 | Indica las longitudes de las NALUs en el ejemplo. Se trata de un BLOB MF que se establece en muestras de entrada comprimidas en el descodificador H.265. |
| [NÚMERO \_ MÍNIMO DE MUESTRAS DE SALIDA \_ \_ \_ DE \_ MF SA](mf-sa-minimum-output-sample-count.md)                 | Especifica el número máximo de muestras de salida.                                                                               |



 

El descodificador H.265 admite la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi) Esta interfaz proporciona una API alternativa para establecer las siguientes propiedades de códec.

-   [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>Restricciones de formato

El descodificador admite los siguientes formatos:



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfiles y niveles    | Perfiles Main, Main Still Picture y Main10                                                                                                                                                                                                                        |
| Formatos de traslación     | 4:2:0 (4:2:0)                                                                                                                                                                                                                                                         |
| Resolución mínima | 48 × 48 píxeles                                                                                                                                                                                                                                                       |
| Resolución máxima | 4096 × 2304 píxeles<br/> La resolución máxima garantizada para la aceleración dxva es de 1920 × 1088 píxeles; en resoluciones más altas, lacodización se realiza con DXVA, si es compatible con el hardware subyacente; de lo contrario, lacodización se realiza con software.<br/> |
| Dxva               | El descodificador admite DX11 y DX12 DXVA, pero no DXVA versión 2 ni DXVA versión 1.                                                                                                                                                                                                         |



 

Los datos de entrada deben cumplir el anexo B de ITU-T H.265 \| ISO/IEC 23008-2. Los datos deben incluir los códigos de inicio. El descodificador omite los bytes hasta que encuentra un conjunto de parámetros de secuencia (SPS) válido y un conjunto de parámetros de imagen (PPS) en la secuencia de bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
