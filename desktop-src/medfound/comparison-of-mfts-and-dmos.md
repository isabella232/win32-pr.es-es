---
description: Media Foundation transformaciones (MFTs) son una evolución del modelo de transformación que se presentó por primera vez con los objetos multimedia de DirectX (DMOs).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Comparación de MFT y DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e76e128ece1609f25e053486dbb6bcf4578161c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080325"
---
# <a name="comparison-of-mfts-and-dmos"></a>Comparación de MFT y DMO

Media Foundation transformaciones (MFTs) son una evolución del modelo de transformación que se presentó por primera vez con los objetos multimedia de DirectX (DMOs). En este tema se resumen las principales formas en las que MFTs es diferente de DMOs. Lea este tema si ya está familiarizado con las interfaces de DMO o si desea convertir una DMO existente en una MFT.

Este tema contiene las siguientes secciones:

-   [Número de flujos](#number-of-streams)
-   [Negociación de formato](#format-negotiation)
-   [Streaming](#streaming)
    -   [Asignación de recursos](#allocating-resources)
    -   [Procesamiento de datos](#processing-data)
    -   [Vaciar](#flushing)
    -   [Flujos de interrupción](#stream-discontinuities)
-   [Diferencias varias](#miscellaneous-differences)
-   [Marcas](#flags)
    -   [Marcas de ProcessInput](#processinput-flags)
    -   [Marcas de ProcessOutput](#processoutput-flags)
    -   [Marcas de GetInputStatus](#getinputstatus-flags)
    -   [Marcas de GetOutputStatus](#getoutputstatus-flags)
    -   [Marcas de GetInputStreamInfo](#getinputstreaminfo-flags)
    -   [Marcas de GetOutputStreamInfo](#getoutputstreaminfo-flags)
    -   [Marcas SetInputType/SetOutputType](#setinputtypesetoutputtype-flags)
-   [Códigos de error](#error-codes)
-   [Crear objetos híbridos DMO/MFT](#creating-hybrid-dmomft-objects)
-   [Temas relacionados](#related-topics)

## <a name="number-of-streams"></a>Número de flujos

Un DMO tiene un número fijo de secuencias, mientras que una MFT puede admitir un número dinámico de flujos. El cliente puede Agregar flujos de entrada y el MFT puede agregar nuevos flujos de salida durante el procesamiento. Sin embargo, no es necesario MFTs para admitir secuencias dinámicas. Una MFT puede tener un número fijo de secuencias, al igual que un DMO.

Los métodos siguientes se usan para admitir secuencias dinámicas en una MFT:

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Además, el método [**IMFTransform::P rocessoutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) define el comportamiento para agregar o quitar flujos de salida.

Dado que DMOs tienen secuencias fijas, las secuencias en un DMO se identifican mediante valores de índice de base cero. MFTs, por otro lado, use identificadores de secuencia que no correspondan necesariamente con valores de índice. Esto se debe a que el número de secuencias de una MFT podría cambiar. Por ejemplo, la secuencia 0 podría quitarse, lo que dejaría el flujo 1 como la primera secuencia. Sin embargo, una MFT con un número fijo de flujos debe observar la misma Convención que DMOs y usar valores de índice para los identificadores de flujo.

## <a name="format-negotiation"></a>Negociación de formato

MFTs use la interfaz [**IMFMediaType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) para describir los tipos de medios. De lo contrario, la negociación de formato con MFTs funciona en los mismos principios básicos que con DMOs. En la tabla siguiente se enumeran los métodos de negociación de formato para DMOs y los métodos correspondientes para MFTs.



| DMO (método)                                                                        | Método MFT                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Como DMOs, MFTs procesa los datos a través de llamadas a métodos [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Estas son las principales diferencias entre los procesos de DMO y MFT al transmitir datos.

### <a name="allocating-resources"></a>Asignación de recursos

MFTs no tienen los métodos [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) y [**IMediaObject:: FreeStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) que se usan con DMOs. Para controlar la asignación y desasignación de recursos de forma eficaz, una MFT puede responder a los mensajes siguientes en el método [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) :

-   [**la \_ notificación del mensaje de MFT \_ comienza el \_ \_ streaming**](mft-message-notify-begin-streaming.md)
-   [**el \_ mensaje \_ de MFT notifica el \_ Inicio \_ de la \_ secuencia**](mft-message-notify-start-of-stream.md)

Además, el cliente puede indicar el inicio y el final de una secuencia mediante una llamada a [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con los mensajes siguientes:

-   [**\_ \_ \_ final \_ de notificación de mensaje de \_ MFT**](mft-message-notify-end-of-stream.md)
-   [**\_fin de \_ notificación de mensaje \_ de MFT \_**](mft-message-notify-end-streaming.md)

Estos dos mensajes no tienen un equivalente de DMO exacto.

### <a name="processing-data"></a>Procesamiento de datos

MFTs usar ejemplos de medios para contener datos de entrada y salida. Los ejemplos de medios exponen la interfaz [**IMFSample**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) y contienen los datos siguientes:

-   Marca de tiempo y duración.
-   Atributos que contienen información por muestra. Para obtener una lista de atributos, consulte [atributos de ejemplo](sample-attributes.md).
-   Cero o más búferes multimedia. Cada búfer multimedia expone la interfaz [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) .

La interfaz [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) es similar a la interfaz **IMediaBuffer** de DMO. Para tener acceso al búfer de memoria subyacente, llame a [**IMFMediaBuffer:: Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Este método es aproximadamente equivalente a [**IMediaBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) para DMOs.

En el caso de los datos de vídeo sin comprimir, un búfer multimedia también podría admitir la interfaz [**IMF2DBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) . Un MFT que procese vídeo sin comprimir (ya sea como entrada o salida) debe estar preparado para usar la interfaz **IMF2DBuffer** si el búfer lo expone. Para obtener más información, consulte [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).

Media Foundation proporciona algunas implementaciones estándar de [**IMFMediaBuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer), por lo que generalmente no es necesario escribir su propia implementación. Para crear un búfer de DMO desde un búfer de Media Foundation, llame a [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Vaciar

MFTs no tienen un método de [**vaciado**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) . Para vaciar una MFT, llame a [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de [**\_ \_ \_ vaciado del comando del mensaje de MFT**](mft-message-command-flush.md) .

### <a name="stream-discontinuities"></a>Flujos de interrupción

MFTs no tienen un método de [**discontinuidad**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) . Para indicar una discontinuidad en una secuencia, establezca el [**atributo \_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) en la muestra de entrada.

## <a name="miscellaneous-differences"></a>Diferencias varias

Estas son algunas diferencias secundarias adicionales entre MFTs y DMOs.

-   No hay equivalentes de MFT para los siguientes métodos de DMO:
    -   [**IMediaObject:: Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   No es necesario MFTs para admitir la agregación.
-   MFTs admite una operación denominada *draining*. El propósito de la purga es procesar los datos que permanecen en el MF, sin proporcionar más datos de entrada a la MFT (por ejemplo, al final de la secuencia). Para purgar un MFT, llame a [**IMFTransform::P rocessmessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de [**agotamiento del comando de mensaje de MFT \_ \_ \_**](mft-message-command-drain.md) . Para obtener más información, vea [modelo de procesamiento de MFT básico](basic-mft-processing-model.md).
-   MFTs puede tener atributos, incluidos los atributos por secuencia. Use los métodos siguientes para obtener los atributos de una MFT:

    -   [**IMFTransform:: GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   MFTs puede procesar eventos. Para enviar un evento a un MFT, llame a [**IMFTransform::P rocessevent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Una MFT puede enviar un evento al cliente mediante el método [**ProcessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) . Para obtener más información, vea [modelo de procesamiento de MFT básico](basic-mft-processing-model.md).

## <a name="flags"></a>Marcas

En las tablas siguientes se enumeran las distintas marcas de DMO y sus equivalentes de MFT. Cada vez que una marca de DMO se asigna directamente a una marca de MFT, ambas marcas tienen el mismo valor numérico. Sin embargo, algunas marcas de DMO no tienen equivalentes de MFT exactos y viceversa.

### <a name="processinput-flags"></a>Marcas de ProcessInput

DMOs: DMO enumeración de [**\_ \_ marcas de búfer de \_ datos \_ \_ de entrada**](/previous-versions/windows/embedded/aa451599(v=msdn.10)) .

MFTs: no hay enumeración equivalente.



| Marca de DMO                                  | Marca de MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **SYNCPOINT de datos de entrada de DMO \_ \_ \_ BUFFERF \_**  | No hay ninguna marca equivalente. En su lugar, establezca el atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) en el ejemplo. |
| **\_hora de \_ BUFFERF de datos de entrada de DMO \_ \_**       | No hay ninguna marca equivalente. En su lugar, llame a [**IMFSample:: SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) en el ejemplo.                                  |
| **TIMELENGTH de datos de entrada de DMO \_ \_ \_ BUFFERF \_** | No hay ninguna marca equivalente. En su lugar, llame a [**IMFSample:: SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) en el ejemplo.                          |



 

### <a name="processoutput-flags"></a>Marcas de ProcessOutput

DMOs: la enumeración de [**\_ \_ marcas de \_ salida \_ del proceso DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags) .

MFTs: enumeración de [**\_ \_ marcas de \_ salida \_ del proceso MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags) .



| Marca de DMO                                            | Marca de MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **salida del proceso de DMO \_ \_ \_ descartada \_ cuando \_ no hay ningún \_ búfer** | **salida del proceso de MFT \_ \_ \_ descartar \_ cuando \_ no hay ningún \_ búfer** |



 

DMOs: la enumeración de [**\_ \_ marcas de búfer de datos de salida \_ \_ \_ de DMO**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags) .


MFTs: enumeración de [**\_ \_ marcas de búfer de datos de salida \_ \_ \_ de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags) .



| Marca de DMO                                   | Marca de MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **datos de salida de DMO \_ \_ \_ BUFFERF \_ SYNCPOINT**  | No hay ninguna marca equivalente. En su lugar, busque el atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) en el ejemplo. |
| **\_hora de \_ BUFFERF de datos de salida de DMO \_ \_**       | No hay ninguna marca equivalente. En su lugar, llame a [**IMFSample:: GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) en el ejemplo.                                        |
| **datos de salida de DMO \_ \_ \_ BUFFERF \_ TIMELENGTH** | No hay ninguna marca equivalente. En su lugar, llame a [**IMFSample:: GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) en el ejemplo.                                |
| **datos de salida de DMO \_ \_ \_ BUFFERF \_ incompletos** | **búfer de datos de salida de MFT \_ \_ \_ \_ incompleto**                                                                                                           |
| No hay ninguna marca equivalente.                        | **\_cambio de \_ formato de búfer de datos de salida de \_ \_ MFT \_**                                                                                                       |
| No hay ninguna marca equivalente.                        | **\_final de \_ flujo de búfer de datos de salida de \_ \_ MFT \_**                                                                                                          |
| No hay ninguna marca equivalente.                        | **búfer de datos de salida de MFT \_ \_ \_ \_ sin \_ ejemplo**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Marcas de GetInputStatus

DMOs: la enumeración de **\_ \_ marcas de \_ estado \_ de entrada de DMO** .

MFTs: enumeración de [**\_ \_ marcas de \_ estado \_ de entrada de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags) .



| Marca de DMO                              | Marca de MFT                             |
|---------------------------------------|--------------------------------------|
| **\_datos de \_ aceptación de STATUSF de entrada de DMO \_ \_** | **Estado de entrada de MFT \_ \_ \_ Accept \_ Data** |



 

### <a name="getoutputstatus-flags"></a>Marcas de GetOutputStatus

DMOs: no hay enumeración equivalente.

MFTs: enumeración de [**\_ \_ marcas de \_ estado \_ de salida de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags) .



| Marca de DMO            | Marca de MFT                               |
|---------------------|----------------------------------------|
| No hay ninguna marca equivalente. | **ejemplo de estado de salida de MFT \_ \_ \_ \_ listo** |



 

### <a name="getinputstreaminfo-flags"></a>Marcas de GetInputStreamInfo

DMOs: la enumeración de [**\_ \_ marcas de información de flujo de entrada \_ \_ \_ de DMO**](/previous-versions/windows/embedded/aa451600(v=msdn.10)) .

MFTs: enumeración de [**\_ \_ marcas de información de flujo de entrada \_ \_ \_ de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags) .



| Marca de DMO                                             | Marca de MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_ \_ muestras completas de STREAMF de entrada de \_ DMO \_**              | **\_ \_ ejemplos completos de flujo de entrada de \_ MFT \_**              |
| **\_ejemplo de entrada de un único STREAMF de entrada de DMO \_ \_ \_ \_ por \_ búfer** | **ejemplo de flujo de entrada de MFT \_ \_ \_ único \_ \_ por \_ búfer** |
| **\_tamaño de \_ \_ ejemplo fijo \_ de STREAMF de entrada de \_ DMO**         | **\_tamaño de \_ \_ muestra fijo \_ del flujo de entrada de \_ MFT**         |
| **STREAMF de entrada de DMO \_ \_ \_ contiene \_ búferes**              | **el \_ flujo de entrada de MFT \_ \_ contiene \_ búferes**              |
| No hay ninguna marca equivalente.                                  | **el flujo de entrada de MFT no \_ \_ \_ realiza \_ \_ ADDREF**           |
| No hay ninguna marca equivalente.                                  | **flujo de entrada de MFT \_ \_ \_ extraíble**                   |
| No hay ninguna marca equivalente.                                  | **secuencia de entrada de MFT \_ \_ \_ opcional**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Marcas de GetOutputStreamInfo

DMOs: la enumeración de [**\_ \_ marcas de información de flujo de salida \_ \_ \_ de DMO**](/previous-versions/ms806053(v=msdn.10)) .

MFTs: enumeración de [**\_ \_ marcas de información de flujo de salida \_ \_ \_ de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags) .



| Marca de DMO                                              | Marca de MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_ \_ ejemplos completos de STREAMF de salida de \_ DMO \_**              | **\_ \_ muestras completas del flujo de salida de \_ MFT \_**              |
| **STREAMF de salida de DMO de \_ \_ \_ un solo \_ ejemplo \_ por \_ búfer** | **ejemplo de flujo de salida de MFT \_ \_ \_ único \_ \_ por \_ búfer** |
| **\_tamaño de \_ \_ ejemplo fijo \_ \_ de salida de DMO STREAMF**         | **\_tamaño de \_ \_ muestra fijo \_ del flujo de salida de \_ MFT**         |
| **STREAMF de salida de DMO \_ \_ \_ descartable**                 | **flujo de salida de MFT \_ \_ \_ descartable**                 |
| **STREAMF de salida de DMO \_ \_ \_ opcional**                    | **secuencia de salida de MFT \_ \_ \_ opcional**                    |
| No hay ninguna marca equivalente.                                   | **el \_ flujo de salida de MFT \_ \_ proporciona \_ ejemplos**           |
| No hay ninguna marca equivalente.                                   | **el \_ flujo de salida de MFT \_ \_ puede \_ proporcionar \_ ejemplos**       |
| No hay ninguna marca equivalente.                                   | **\_ \_ \_ lectura diferida de flujo de salida de MFT \_**                  |
| No hay ninguna marca equivalente.                                   | **flujo de salida de MFT \_ \_ \_ extraíble**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Marcas SetInputType/SetOutputType

DMOs: [**\_ DMO \_ set \_ Type \_ Flags**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags) (enumeración).

MFTs: enumeración de [**\_ \_ \_ \_ marcas de tipo de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags) .



| Marca de DMO                        | Marca de MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **DMO \_ set \_ TYPEF \_ \_ solo prueba** | **tipo de conjunto de MFT \_ \_ \_ \_ solo prueba**                                                       |
| **DMO \_ set \_ TYPEF \_ Clear**      | No hay ninguna marca equivalente. En su lugar, establezca el tipo de medio en **null** para borrar el tipo de medio. |



 

## <a name="error-codes"></a>Códigos de error

En la tabla siguiente se muestra cómo asignar códigos de error de DMO a códigos de error de MFT. Un objeto MFT/DMO híbrido debe devolver los códigos de error de DMO de los métodos [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) y los códigos de error de MFT de los métodos [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) . Los códigos de error de DMO se definen en el archivo de encabezado MediaErr. h. Los códigos de error de MFT se definen en el archivo de encabezado mferror. h.



| Código de error de DMO                  | Código de error de MFT                       |
|---------------------------------|--------------------------------------|
| **DMO \_ E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **DMO \_ E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **DMO \_ E \_ NOTACCEPTING**        | **MF \_ E \_ NOTACCEPTING**              |
| **DMO \_ E \_ no hay \_ más \_ elementos**     | **MF \_ E \_ no hay \_ más \_ tipos**           |
| **\_no se \_ \_ \_ aceptó el tipo de DMO E** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_no se \_ \_ ha \_ establecido el tipo DMO E**      | **\_no se \_ \_ \_ ha establecido el tipo de transformación MF E \_** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Crear objetos híbridos DMO/MFT

La interfaz [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) se basa de forma flexible en [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject), que es la interfaz principal de los objetos multimedia de DirectX (DMOs). Es posible crear objetos que expongan ambas interfaces. Sin embargo, esto puede provocar conflictos de nomenclatura, ya que las interfaces tienen algunos métodos que comparten el mismo nombre. Puede resolver este problema de una de las dos maneras siguientes:

Solución 1: incluya la siguiente línea en la parte superior de cualquier archivo. cpp que contenga las funciones de MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Esto cambia la declaración de la interfaz [**IMFTransform**](/windows/win32/api/mftransform/nn-mftransform-imftransform) para que la mayoría de los nombres de método tengan el prefijo "MFT". Por lo tanto, [**IMFTransform::P rocessinput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) se convierte en **IMFTransform:: MFTProcessInput**, mientras que [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) mantiene su nombre original. Esta técnica es muy útil si va a convertir una DMO existente en una DMO/MFT híbrida. Puede Agregar los nuevos métodos de MFT sin cambiar los métodos de DMO.

Solución 2: Use la sintaxis de C++ para eliminar la ambigüedad de los nombres que se heredan de más de una interfaz. Por ejemplo, declare la versión de MFT de [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) como se indica a continuación:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Declare la versión de DMO de [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) como la siguiente:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Si realiza una llamada interna a un método dentro del objeto, puede usar esta sintaxis, pero si lo hace, se invalidará el estado virtual del método. Una manera mejor de realizar llamadas desde dentro del objeto es la siguiente:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

De este modo, si deriva otra clase de **CMyHybridObject** e invalida el método CMyHybridObject:: IMediaObject::P rocessinput, se llama al método virtual correcto. Las interfaces de DMO se documentan en la documentación del SDK de DirectShow.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 
