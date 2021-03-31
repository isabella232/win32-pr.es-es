---
description: Objeto que encapsula varios DSP relacionados con la captura de voz.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP de captura de voz (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812571"
---
# <a name="voice-capture-dsp"></a>DSP de captura de voz

Objeto que encapsula varios DSP relacionados con la captura de voz.

## <a name="clsid"></a>CLSID

CLSID \_ CWMAudioAEC

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **IPropertyStore**

## <a name="properties"></a>Propiedades



| Propiedad                                                                                     | Descripción                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [MFPKEY \_ \_ índices de dispositivo WMAAECMA \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Especifica qué dispositivos de audio usa DMO para capturar y representar audio.                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifica la combinación de dispositivos de audio que la aplicación está usando actualmente.              |
| [modo de origen de MFPKEY \_ WMAAECMA \_ DMO \_ \_](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Especifica si DMO utiliza el modo de origen o el modo de filtro.                                        |
| [MFPKEY \_ WMAAECMA \_ feat \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Especifica el número de veces que DMO realiza la supresión del eco acústico (AES) en la señal residual. |
| [MFPKEY \_ WMAAECMA \_ feat \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Especifica si DMO realiza el control de ganancia automática.                                        |
| [\_clip del \_ \_ Centro \_ de MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Especifica si DMO realiza el recorte del centro.                                               |
| [\_longitud del \_ eco del funcdor de MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Especifica la duración del eco que puede controlar el algoritmo de cancelación del eco acústico (AEC).    |
| [\_tamaño de \_ \_ marco \_ del MFPKEY de WMAAECMA](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Especifica el tamaño del fotograma de audio.                                                                   |
| [MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Especifica qué viga utiliza DMO para el procesamiento de la matriz de micrófono.                                |
| [\_ \_ \_ modo MICARR MFPKEY WMAAECMA feat \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Especifica cómo DMO realiza el procesamiento de la matriz de micrófono.                                       |
| [MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Especifica si DMO realiza el preprocesamiento de la matriz de micrófono.                                |
| [\_relleno de \_ \_ ruido \_ de MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Especifica si DMO realiza el relleno de ruido.                                                 |
| [MFPKEY \_ WMAAECMA \_ feat \_](mfpkey-wmaaecma-featr-nsproperty.md)                          | Especifica si DMO realiza la supresión de ruido.                                             |
| [MFPKEY \_ WMAAECMA \_ feat \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Especifica el tipo de detección de la actividad de voz que realiza DMO.                             |
| [modo de característica de MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Permite que la aplicación invalide la configuración predeterminada en varias propiedades.                   |
| [\_ \_ \_ enlazador de ganancia de MFPKEY WMAAECMA MIC \_](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Especifica si DMO aplica el límite de ganancia de micrófono.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Especifica la geometría de la matriz de micrófono.                                                          |
| [\_ \_ métricas de calidad de MFPKEY WMAAECMA \_](mfpkey-wmaaecma-quality-metricsproperty.md)            | Recupera las métricas de calidad de AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ recuperar \_ estadísticas de TS \_](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Especifica si DMO almacena las estadísticas de marca de tiempo en el registro.                           |
| [modo de sistema de MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-system-modeproperty.md)                    | Establece el modo de procesamiento.                                                                         |



 

## <a name="remarks"></a>Observaciones

A diferencia de los demás DSP, el objeto de captura de voz encapsula varios DSP en un solo objeto y el objeto es solo un objeto DMO (no implementa [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). La captura de voz DMO incluye los siguientes componentes de DSP:

-   Cancelación del eco acústico (AEC)
-   Procesamiento de la matriz de micrófono
-   Supresión de ruido
-   Control de ganancia automática
-   Detección de actividad de voz

Las aplicaciones pueden activar y desactivar cada componente de forma individual.

La captura de voz DMO admite dos modos de funcionamiento, modo de *filtro* y modo de *origen* . En el modo de filtro, la aplicación envía muestras de audio desde el micrófono y desde la línea del altavoz hasta el DMO, y el DMO genera una salida.

En el modo de origen, la aplicación no necesita proporcionar ejemplos a DMO. En su lugar, el DMO administra todas las operaciones en los dispositivos de audio, incluida la inicialización de los dispositivos, la captura y la sincronización de las secuencias de audio, el cálculo de las marcas de tiempo y la recuperación de la geometría de la matriz de micrófono. Con el modo de origen, la aplicación simplemente configura DMO y la salida de DMO es una señal de micrófono limpia y procesada. El modo de origen es mucho más fácil de usar que el modo de filtro y se recomienda para la mayoría de las aplicaciones.

Actualmente, la captura de voz DMO solo admite la cancelación de eco acústico (AEC) de canal único, por lo que la salida de la línea de altavoz debe ser de un solo canal. Si el procesamiento de la matriz de micrófono está deshabilitado, la entrada de varios canales se dobla hacia abajo a un canal para el procesamiento de AEC. Si el procesamiento de la matriz de micrófonos y el procesamiento de AEC están habilitados, AEC se realiza en cada elemento de micrófono antes del procesamiento de la matriz de micrófono.

### <a name="microphone-array-processing"></a>Procesamiento de la matriz de micrófono

Una matriz de micrófonos es un conjunto de micrófonos muy colocados. Las matrices de micrófonos logran una mejor direccional que un micrófono único, ya que las ondas acústicas llegan a cada micrófono en un momento ligeramente diferente. Para obtener más información acerca de las matrices de micrófono, consulte los artículos web [compatibilidad con matrices de micrófono en Windows Vista](/windows-hardware/design/component-guidelines/audio) y [cómo compilar y usar matrices de micrófonos para Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Uso del DSP de captura de voz

Para usar la captura de voz DSP, realice los pasos siguientes.

### <a name="1-initialize-the-dmo"></a>1. inicializar DMO

Cree la función de captura de voz DMO llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID **CLSID \_ CWMAudioAEC**. La captura de voz DSDP expone solo las interfaces [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) y [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , por lo que solo se puede usar como DMO.

DMO tiene como valor predeterminado el modo de origen. Para seleccionar el modo de filtro, establezca la propiedad [MFPKEY \_ WMAAECMA \_ DMO \_ source \_ mode](mfpkey-wmaaecma-dmo-source-modeproperty.md) en **Variant \_ false**.

A continuación, configure las propiedades internas de DMO mediante la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . La única propiedad que debe establecer una aplicación es la propiedad de [ \_ \_ \_ modo del sistema MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md) . Esta propiedad configura la canalización de procesamiento dentro de DMO. Las demás propiedades son opcionales.

### <a name="2-set-the-input-and-output-formats"></a>2. establecer los formatos de entrada y salida

Si usa DMO en modo de filtro, establezca el formato de entrada mediante una llamada a [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). El formato de entrada puede ser prácticamente cualquier PCM sin comprimir o tipo de audio de punto flotante de IEEE válido. Si el formato de entrada no coincide con el formato de salida, DMO realiza automáticamente la conversión de velocidad de muestra.

Si usa DMO en modo de origen, no establezca el formato de entrada. DMO configura automáticamente el formato de entrada basado en los dispositivos de audio.

En cualquier modo, establezca el formato de salida llamando a [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). DMO puede aceptar los siguientes formatos de salida:

-   SubType: **MEDIASUBTYPE \_ PCM** o **MEDIASUBTYPE \_ IEEE \_ float**
-   Bloque de formato: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Muestras por segundo: 8.000; 11.025; 16.000; o 22.050
-   Canales: 1 para el modo de solo AEC, 2 o 4 para el procesamiento de la matriz de micrófonos
-   Bits por muestra: 16

El código siguiente establece el tipo de salida en audio PCM de canal único de 16 bits:


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. procesar datos

Antes de procesar los datos, se recomienda llamar a [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Este método asigna los recursos utilizados internamente por DMO. Llame a **AllocateStreamingResources** después de los pasos indicados anteriormente, no antes. Si no llama a este método, DMO asigna automáticamente los recursos cuando se inicia el procesamiento de datos.

Si usa DMO en modo de filtro, debe pasar los datos de entrada a DMO mediante una llamada a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). Los datos de audio del micrófono van a la secuencia 0 y los datos de audio de la línea del altavoz van a la secuencia 1. Si usa DMO en modo de origen, no es necesario llamar a **ProcessInput**.

Para obtener los datos de salida del DSP, realice los pasos siguientes:

1.  Cree un objeto de búfer para almacenar los datos de salida. El objeto de búfer debe implementar la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . El tamaño del búfer depende de los requisitos de la aplicación. La asignación de un búfer mayor puede reducir las posibilidades de que se produzcan problemas.
2.  Declare una estructura de búfer de datos de salida de DMO y establezca el miembro **pBuffer** para que apunte al objeto de búfer. [**\_ \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)
3.  Pase la estructura de búfer de datos de salida de DMO al método [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) . [**\_ \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)
4.  Continúe llamando a este método siempre que el DMO tenga datos de salida. El DSP indica que tiene más resultados estableciendo la marca de **datos de salida de DMO \_ \_ \_ BUFFERF \_ incompleta** en el miembro **dwStatus** de la estructura de [**búfer de datos de salida de DMO \_ \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
