---
description: Objeto que encapsula varios DSP relacionados con la captura de voz.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP de captura de voz (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252489"
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
| [ÍNDICES DE DISPOSITIVO \_ MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Especifica qué dispositivos de audio usa DMO para capturar y representar audio.                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifica la combinación de dispositivos de audio que la aplicación está usando actualmente.              |
| [MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Especifica si el DMO usa el modo de origen o el modo de filtro.                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Especifica cuántas veces el DMO realiza la supresión de eco acústico (AES) en la señal residual. |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Especifica si el DMO realiza el control de ganancia automático.                                        |
| [CLIP DEL CENTRO MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Especifica si el DMO realiza el recorte central.                                               |
| [LONGITUD DE ECO DE MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Especifica la duración del eco que el algoritmo de cancelación de eco acústico (AEC) puede controlar.    |
| [TAMAÑO DEL MARCO MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Especifica el tamaño del marco de audio.                                                                   |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ BEAM](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Especifica qué haz usa el DMO para el procesamiento de la matriz de micrófonos.                                |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Especifica cómo el usuario DMO procesamiento de la matriz de micrófonos.                                       |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Especifica si el DMO preprocesamiento de la matriz de micrófonos.                                |
| [RELLENO DE RUIDO DE MFPKEY \_ WMAAECMA \_ FEATR \_ \_](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Especifica si el DMO realiza el relleno de ruido.                                                 |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | Especifica si el DMO realiza la supresión de ruido.                                             |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Especifica el tipo de detección de actividad de voz que DMO realiza.                             |
| [MODO DE CARACTERÍSTICA \_ MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Permite que la aplicación invalide la configuración predeterminada en varias propiedades.                   |
| [MFPKEY \_ WMAAECMA \_ MIC \_ GAIN \_ BOUNDER](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Especifica si el DMO aplica el límite de ganancia de micrófono.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Especifica la geometría de la matriz de micrófonos.                                                          |
| [MÉTRICAS DE CALIDAD DE MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-quality-metricsproperty.md)            | Recupera las métricas de calidad de AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Especifica si el DMO almacena las estadísticas de marca de tiempo en el Registro.                           |
| [MODO DEL SISTEMA \_ MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-system-modeproperty.md)                    | Establece el modo de procesamiento.                                                                         |



 

## <a name="remarks"></a>Observaciones

A diferencia de los otros DSP, el objeto de captura de voz encapsula varios DSP en un solo objeto y el objeto es un objeto DMO solo (no implementa [**LATRANSFORMDETRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). La captura de DMO incluye los siguientes componentes de DSP:

-   Cancelación de eco acústico (AEC)
-   Procesamiento de la matriz de micrófonos
-   Supresión de ruido
-   Control automático de ganancia
-   Detección de actividad de voz

Las aplicaciones pueden activar y desactivar cada componente individualmente.

La captura de DMO admite dos modos de operación, *el modo de* filtro y el modo *de* origen. En el modo de filtro, la aplicación envía muestras de audio desde el micrófono y desde la línea del hablante al DMO, y el DMO genera la salida.

En el modo de origen, la aplicación no necesita entregar ejemplos al DMO. En su lugar, el DMO administra todas las operaciones en los dispositivos de audio, incluida la inicialización de los dispositivos, la captura y sincronización de las secuencias de audio, el cálculo de marcas de tiempo y la recuperación de la geometría de la matriz de micrófonos. Con el modo de origen, la aplicación simplemente configura el DMO y la salida del DMO es una señal de micrófono limpia y procesada. El modo de origen es significativamente más fácil de usar que el modo de filtro y se recomienda para la mayoría de las aplicaciones.

Actualmente, la captura de DMO solo admite la cancelación de eco acústico de canal único (AEC), por lo que la salida de la línea del hablante debe ser de un solo canal. Si el procesamiento de la matriz de micrófonos está deshabilitado, la entrada multicanal se plega a un canal para el procesamiento de AEC. Si el procesamiento de la matriz de micrófonos y el procesamiento de AEC están habilitados, AEC se realiza en cada elemento de micrófono antes del procesamiento de la matriz de micrófonos.

### <a name="microphone-array-processing"></a>Procesamiento de la matriz de micrófonos

Una matriz de micrófonos es un conjunto de micrófonos estrechamente posicionados. Las matrices de micrófonos logran una mejor direccionalidad que un solo micrófono, ya que las ondas acústicas llegan a cada micrófono en un momento ligeramente diferente. Para obtener más información sobre las matrices de micrófonos, vea los artículos web Microphone Array Support in Windows Vista (Compatibilidad con matrices de micrófonos en [Windows Vista)](/windows-hardware/design/component-guidelines/audio) y How to Build and Use Microphone Arrays for Windows Vista (Cómo compilar y usar matrices de [micrófonos para Windows Vista).](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)

### <a name="using-the-voice-capture-dsp"></a>Uso del DSP de captura de voz

Para usar el DSP de captura de voz, realice los pasos siguientes.

### <a name="1-initialize-the-dmo"></a>1. Inicialice el DMO

Cree la captura de DMO mediante una llamada [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con **CLSID \_ CLSID CWMAudioAEC**. El DSDP de captura de voz solo expone las interfaces [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e [**IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) por lo que solo se puede usar como DMO.

El DMO predeterminado es el modo de origen. Para seleccionar el modo de filtro, establezca la propiedad [ \_ MFPKEY WMAAECMA \_ DMO SOURCE \_ \_ MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md) en **VARIANT \_ FALSE.**

A continuación, configure las propiedades internas del DMO mediante la [**interfaz IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) La única propiedad que debe establecer una aplicación es [la propiedad MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE.](mfpkey-wmaaecma-system-modeproperty.md) Esta propiedad configura la canalización de procesamiento dentro del DMO. Las demás propiedades son opcionales.

### <a name="2-set-the-input-and-output-formats"></a>2. Establecer los formatos de entrada y salida

Si usa la clase DMO en modo de filtro, establezca el formato de entrada mediante una llamada a [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). El formato de entrada puede ser casi cualquier tipo de audio de punto flotante IEEE o PCM sin comprimir válido. Si el formato de entrada no coincide con el formato de salida, DMO realiza automáticamente la conversión de frecuencia de muestreo.

Si usa la opción DMO en modo de origen, no establezca el formato de entrada. El DMO configura automáticamente el formato de entrada en función de los dispositivos de audio.

En cualquier modo, establezca el formato de salida mediante una [**llamada a IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). El DMO puede aceptar los siguientes formatos de salida:

-   Subtipo: **MEDIASUBTYPE \_ PCM** o **MEDIASUBTYPE \_ IEEE \_ FLOAT**
-   Bloque de formato: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEATEX**](/previous-versions/dd757713(v=vs.85))
-   Ejemplos por segundo: 8000; 11,025; 16,000; o 22 050
-   Canales: 1 para el modo solo AEC, 2 o 4 para el procesamiento de la matriz de micrófonos
-   Bits por ejemplo: 16

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



### <a name="3-process-data"></a>3. Procesar datos

Antes de procesar los datos, se recomienda llamar a [**IMediaObject::AllocateStreamingResources.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) Este método asigna los recursos utilizados internamente por el DMO. Llame **a AllocateStreamingResources** después de los pasos enumerados anteriormente, no antes. Si no llama a este método, el DMO asigna automáticamente los recursos cuando se inicia el procesamiento de datos.

Si usa el DMO en modo de filtro, debe pasar los datos de entrada al DMO llamando a [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). Los datos de audio del micrófono van a la secuencia 0 y los datos de audio de la línea del hablante van al flujo 1. Si usa el DMO en modo de origen, no es necesario llamar a **ProcessInput**.

Para obtener los datos de salida del DSP, realice los pasos siguientes:

1.  Cree un objeto de búfer para contener los datos de salida. El objeto de búfer debe implementar la [**interfaz IMediaBuffer.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) El tamaño del búfer depende de los requisitos de la aplicación. La asignación de un búfer mayor puede reducir las posibilidades de que se produzcan problemas.
2.  Declare una [**DMO \_ OUTPUT DATA \_ \_ BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) y establezca el **miembro pBuffer** para que apunte al objeto de búfer.
3.  Pase la [**DMO \_ OUTPUT DATA \_ \_ BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) al método [**IMediaObject::P rocessOutput.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)
4.  Continúe con la llamada a este método mientras el DMO tenga datos de salida. El DSP indica que tiene más salida estableciendo la marca **\_ DMO OUTPUT DATA \_ \_ BUFFERF \_ INCOMPLETE** en el miembro **dwStatus** de la estructura [**DMO OUTPUT DATA \_ \_ \_ BUFFER.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
