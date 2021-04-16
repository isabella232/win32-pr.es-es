---
description: El descodificador de vídeo H. 265 Media Foundation es una transformación de Media Foundation que admite la descodificación del contenido H. 265/HEVC en el formato del Anexo B y se puede usar en la reproducción de archivos MP4 y M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Descodificador de vídeo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543622"
---
# <a name="h265--hevc-video-decoder"></a>Descodificador de vídeo H. 265/HEVC

El descodificador de vídeo H. 265 Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que admite la descodificación del contenido H. 265/HEVC en el formato del Anexo B y se puede usar en la reproducción de archivos MP4 y M2TS.

El descodificador de vídeo H. 265 expone las siguientes interfaces.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (compatible con Windows 8)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Para crear una instancia del descodificador, llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

## <a name="input-types"></a>Tipos de entrada

El tipo de entrada debe contener al menos los dos atributos siguientes:



| Atributo                                                 | Descripción                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | **Vídeo de MFMediaType \_**                                                                        |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ HEVC](video-subtype-guids.md) o MFVideoFormat \_ HEVC \_ es |



 

El primer subtipo de medio, MFVideoFormat \_ HEVC, indica que los ejemplos multimedia llevan H. 265 fragmentada con códigos de inicio y que el flujo tiene SP/PPS entrelazado. Supone un fotograma por muestra.

El subtipo de medio MFVideoFormat \_ HEVC \_ es para indicar que los ejemplos de medios transportan la elemental H. 265 fragmentada, donde cada ejemplo puede contener una imagen parcial, varias imágenes, algunas imágenes más una imagen parcial.

Los tipos de medios de entrada no pueden cambiar dinámicamente entre dos tipos. El descodificador puede detectar cambios en el formato de salida en curso en función de la sintaxis de secuencia elemental (relación de aspecto, dimensión, marcas entrelazadas e información de base de datos) y desencadenar los cambios de tipo de medio de salida correspondientes.

En el caso del tipo de medio de entrada, el descodificador espera que el origen establezca el perfil correcto. Por ejemplo, si el contenido va a ser 10 bits, el tipo de medio de entrada debe especificar el perfil como Main10.

## <a name="output-types"></a>Tipos de salida

El descodificador admite los siguientes subtipos de salida:

-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ P010**

Para obtener más información sobre estos subtipos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="transform-attributes"></a>Atributos de transformación

El descodificador H. 265 implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.



| Atributo                                                                                       | Descripción                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                     | Habilita o deshabilita el modo de descodificación de latencia baja.                                                                                |
| [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                           | Establece el número de subprocesos de trabajo utilizados por el descodificador.                                                                        |
| [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Habilita o deshabilita el modo de generación de miniaturas.                                                                                |
| [\_conjunto de \_ longitud MF Nalu \_](mf-nalu-length-set.md)                                                 | Indica que la información de longitud de NALU se enviará como un BLOB con cada ejemplo H. 265 comprimido.                              |
| [\_información de \_ longitud de Nalu MF \_](mf-nalu-length-information.md)                                 | Indica las longitudes de NALUs en el ejemplo. Se trata de un BLOB MF que se establece en los ejemplos de entrada comprimidos en el descodificador H. 265. |
| [recuento de \_ \_ ejemplo de salida mínima de SA de \_ \_ MF \_](mf-sa-minimum-output-sample-count.md)                 | Especifica el número máximo de ejemplos de salida.                                                                               |



 

El descodificador H. 265 admite la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Esta interfaz proporciona una API alternativate para configurar las siguientes propiedades de códec.

-   [CODECAPI \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)
-   [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a>Restricciones de formato

El descodificador admite los siguientes formatos:



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perfiles/niveles    | Perfiles principal, principal y de Main10                                                                                                                                                                                                                        |
| Formatos de croma     | croma 4:2:0                                                                                                                                                                                                                                                         |
| Resolución mínima | 48 × 48 píxeles                                                                                                                                                                                                                                                       |
| Resolución máxima | 4096 × 2304 píxeles<br/> La resolución máxima garantizada para la aceleración de DXVA es 1920 × 1088 píxeles; con resoluciones más altas, la descodificación se realiza con DXVA, si es compatible con el hardware subyacente; de lo contrario, la descodificación se realiza con el software.<br/> |
| DXVA               | El descodificador admite DX11 y DX12 DXVA, pero no la versión 2 de DXVA o la versión 1 de DXVA.                                                                                                                                                                                                         |



 

Los datos de entrada deben ajustarse al Anexo B de ITU-T H. 265 \| ISO/IEC 23008-2. Los datos deben incluir los códigos de inicio. El descodificador omite los bytes hasta que encuentra un conjunto de parámetros de secuencia (SPS) y un conjunto de parámetros de imagen (PPS) válidos en el flujo de bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
