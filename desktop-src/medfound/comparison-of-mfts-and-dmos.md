---
description: Media Foundation transformaciones (MTO) son una evolución del modelo de transformación introducido por primera vez con Objetos multimedia DirectX (DMO).
ms.assetid: 4e8c3ec9-6ffa-4858-a4ea-8ef8ccaf9253
title: Comparación de MFT y DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e145effed095fb22f6bfeb07cbee23ab3d30836a404f36a2bad4b9fbeb1dd81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958985"
---
# <a name="comparison-of-mfts-and-dmos"></a>Comparación de MFT y DMO

Media Foundation transformaciones (MTO) son una evolución del modelo de transformación introducido por primera vez con Objetos multimedia DirectX (DMO). En este tema se resumen las principales formas en que las MTO difieren de las DDO. Lea este tema si ya está familiarizado con las interfaces de DMO o si desea convertir una DMO existente en un MFT.

Este tema contiene las siguientes secciones:

-   [Número de Secuencias](#number-of-streams)
-   [Negociación de formato](#format-negotiation)
-   [Streaming](#streaming)
    -   [Asignación de recursos](#allocating-resources)
    -   [Procesamiento de datos](#processing-data)
    -   [Lavado](#flushing)
    -   [Discontinuidades de secuencias](#stream-discontinuities)
-   [Diferencias varias](#miscellaneous-differences)
-   [Marcas](#flags)
    -   [Marcas ProcessInput](#processinput-flags)
    -   [ProcessOutput Flags](#processoutput-flags)
    -   [Marcas GetInputStatus](#getinputstatus-flags)
    -   [Marcas GetOutputStatus](#getoutputstatus-flags)
    -   [Marcas GetInputStreamInfo](#getinputstreaminfo-flags)
    -   [Marcas GetOutputStreamInfo](#getoutputstreaminfo-flags)
    -   [Marcas SetInputType/SetOutputType](#setinputtypesetoutputtype-flags)
-   [Códigos de error](#error-codes)
-   [Creación de objetos DMO/MFT híbridos](#creating-hybrid-dmomft-objects)
-   [Temas relacionados](#related-topics)

## <a name="number-of-streams"></a>Número de Secuencias

Un DMO tiene un número fijo de secuencias, mientras que un MFT puede admitir un número dinámico de secuencias. El cliente puede agregar flujos de entrada y MFT puede agregar nuevos flujos de salida durante el procesamiento. Sin embargo, no es necesario que las MFT admitan flujos dinámicos. Un MFT puede tener un número fijo de secuencias, al igual que un DMO.

Los métodos siguientes se usan para admitir flujos dinámicos en un MFT:

-   [**IMFTransform::AddInputStreams**](/windows/win32/api/mftransform/nf-mftransform-imftransform-addinputstreams)
-   [**IMFTransform::D eleteInputStream**](/windows/win32/api/mftransform/nf-mftransform-imftransform-deleteinputstream)
-   [**IMFTransform::GetStreamIDs**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamids)
-   [**IMFTransform::GetStreamLimits**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getstreamlimits)

Además, el [**método IMFTransform::P rocessOutput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) define el comportamiento para agregar o quitar flujos de salida.

Dado que las DDO tienen secuencias fijas, las secuencias de un DMO se identifican mediante valores de índice de base cero. Por otro lado, las MTA usan identificadores de flujo que no se corresponden necesariamente con los valores de índice. Esto se debe a que el número de secuencias en un MFT puede cambiar. Por ejemplo, se podría quitar el flujo 0, dejando el flujo 1 como la primera secuencia. Sin embargo, un MFT con un número fijo de secuencias debe observar la misma convención que las DDO y usar valores de índice para los identificadores de flujo.

## <a name="format-negotiation"></a>Negociación de formato

Las mft usan la [**interfaz DEFMEDIAType**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) para describir los tipos de medios. De lo contrario, la negociación de formato con MTO funciona con los mismos principios básicos que con las DDO. En la tabla siguiente se enumeran los métodos de negociación de formato para las DDO y los métodos correspondientes para las MTO.



| DMO método                                                                        | Método MFT                                                                          |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**IMediaObject::GetInputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputcurrenttype)   | [**IMFTransform::GetInputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)       |
| [**IMediaObject::GetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputmaxlatency)     | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo)         | [**IMFTransform::GetInputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)         |
| [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)                 | [**IMFTransform::GetInputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)   |
| [**IMediaObject::GetOutputCurrentType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputcurrenttype) | [**IMFTransform::GetOutputCurrentType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)     |
| [**IMediaObject::GetOutputSizeInfo**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo)       | [**IMFTransform::GetOutputStreamInfo**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)       |
| [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)               | [**IMFTransform::GetOutputAvailableType**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) |



 

## <a name="streaming"></a>Streaming

Al igual que las DTO, las MTA procesan los datos a través de llamadas a [**los**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) métodos [**ProcessInput y ProcessOutput.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Estas son las principales diferencias entre los procesos DMO y MFT al transmitir datos.

### <a name="allocating-resources"></a>Asignación de recursos

Las MTO no tienen los [**métodos IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) e [**IMediaObject::FreeStreamingResources usados**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-freestreamingresources) con DDO. Para controlar la asignación y desasignación de recursos de forma eficaz, un MFT puede responder a los mensajes siguientes en el método [**IMFTransform::P rocessMessage:**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage)

-   [**NOTIFICACIÓN DE MENSAJE DE MFT \_ \_ BEGIN \_ \_ STREAMING**](mft-message-notify-begin-streaming.md)
-   [**MFT \_ MESSAGE \_ NOTIFY \_ START \_ OF \_ STREAM**](mft-message-notify-start-of-stream.md)

Además, el cliente puede indicar el inicio y el final de una secuencia llamando a [**ProcessMessage**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) con los siguientes mensajes:

-   [**MFT \_ MESSAGE \_ NOTIFY \_ END \_ OF \_ STREAM**](mft-message-notify-end-of-stream.md)
-   [**MFT \_ MESSAGE \_ NOTIFY \_ END \_ STREAMING**](mft-message-notify-end-streaming.md)

Estos dos mensajes no tienen ninguna DMO equivalente.

### <a name="processing-data"></a>Procesamiento de datos

Las MTA usan ejemplos de medios para contener datos de entrada y salida. Los ejemplos multimedia exponen [**la interfaz DE PRUEBASEJEJEMPLOS**](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) y contienen los datos siguientes:

-   Marca de tiempo y duración.
-   Atributos que contienen información por ejemplo. Para obtener una lista de atributos, vea [Atributos de ejemplo.](sample-attributes.md)
-   Cero o más búferes multimedia. Cada búfer multimedia expone la [**interfaz DEMEMEDIABuffer.**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)

La [**interfaz DEMEMEDIABuffer**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) es similar a la interfaz DMO **IMediaBuffer.** Para acceder al búfer de memoria subyacente, llame [**a IMFMediaBuffer::Lock**](/windows/win32/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Este método es aproximadamente equivalente a [**IMediaBuffer::GetBufferAndLength para**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getbufferandlength) DDO.

En el caso de los datos de vídeo sin comprimir, un búfer multimedia también puede admitir la [**interfaz IMF2DBuffer.**](/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer) Un MFT que procese vídeo sin comprimir (ya sea como entrada o salida) debe estar preparado para usar la interfaz **IMF2DBuffer** si el búfer lo expone. Para obtener más información, vea [Búferes de vídeo sin comprimir.](uncompressed-video-buffers.md)

Media Foundation proporciona algunas implementaciones estándar [**deBUFFERMediaBuffer,**](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer)por lo que generalmente no es necesario escribir su propia implementación. Para crear un búfer DMO a partir de un búfer Media Foundation, llame a [**MFCreateLegacyMediaBufferOnMFMediaBuffer**](/windows/win32/api/mfapi/nf-mfapi-mfcreatelegacymediabufferonmfmediabuffer).

### <a name="flushing"></a>Lavado

Las MFT no tienen un [**método Flush.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-flush) Para vaciar un MFT, llame [**a LAQTransform::P rocessMessage con**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) el [**mensaje FLUSH del comando MFT \_ MESSAGE. \_ \_**](mft-message-command-flush.md)

### <a name="stream-discontinuities"></a>Discontinuidades de secuencias

Las MFT no tienen un [**método Discontinuity.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-discontinuity) Para indicar una discontinuidad en una secuencia, establezca el atributo [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) en el ejemplo de entrada.

## <a name="miscellaneous-differences"></a>Diferencias varias

Estas son algunas diferencias menores adicionales entre las MTO y las DDO.

-   No hay equivalentes de MFT para los siguientes DMO métodos:
    -   [**IMediaObject::Lock**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-lock)
    -   [**IMediaObject::SetInputMaxLatency**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputmaxlatency)
-   Las MTO no son necesarias para admitir la agregación.
-   Las MTA admiten una operación denominada *purgar*. El propósito de purgar es procesar los datos que permanecen en la MF, sin proporcionar más datos de entrada al MFT (por ejemplo, al final de la secuencia). Para purgar un MFT, llame [**a LAQTransform::P rocessMessage con**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processmessage) el mensaje DE PURGA [**DEL COMANDO \_ \_ MFT \_ MESSAGE.**](mft-message-command-drain.md) Para obtener más información, vea [Basic MFT Processing Model](basic-mft-processing-model.md).
-   Las MFT pueden tener atributos, incluidos los atributos por secuencia. Use los métodos siguientes para obtener los atributos de un MFT:

    -   [**IMFTransform::GetAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getattributes)
    -   [**IMFTransform::GetInputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)
    -   [**IMFTransform::GetOutputStreamAttributes**](/windows/win32/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)

-   Las MTA pueden procesar eventos. Para enviar un evento a un MFT, llame [**a IMFTransform::P rocessEvent**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processevent). Un MFT puede enviar un evento al cliente a través del [**método ProcessOutput.**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processoutput) Para obtener más información, vea [Basic MFT Processing Model](basic-mft-processing-model.md).

## <a name="flags"></a>Marcas

En las tablas siguientes se muestran las DMO y sus equivalentes de MFT. Cada vez que DMO marca se asigna directamente a una marca MFT, ambas marcas tienen el mismo valor numérico. Sin embargo, algunas DMO marcas no tienen equivalentes de MFT exactos y viceversa.

### <a name="processinput-flags"></a>Marcas ProcessInput

DMO: [**\_ DMO \_ enumeración INPUT \_ DATA BUFFER \_ \_ FLAGS.**](/previous-versions/windows/embedded/aa451599(v=msdn.10))

MFT: no hay enumeración equivalente.



| DMO marca                                  | Marca MFT                                                                                                                                      |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO PUNTO \_ DE SINCRONIZACIÓN DE BÚFER DE DATOS DE \_ \_ ENTRADA**  | No hay ninguna marca equivalente. En su lugar, establezca [**el atributo MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) en el ejemplo. |
| **\_DMO TIEMPO \_ DE BÚFER DE DATOS DE \_ \_ ENTRADAF**       | No hay ninguna marca equivalente. En su lugar, llame [**aSAMPLESample::SetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampletime) en el ejemplo.                                  |
| **\_DMO INPUT \_ DATA \_ BUFFERF \_ TIMELENGTH** | No hay ninguna marca equivalente. En su lugar, llame [**aSAMPLESample::SetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) en el ejemplo.                          |



 

### <a name="processoutput-flags"></a>ProcessOutput Flags

DDO: [**\_ DMO \_ enumeración PROCESS \_ OUTPUT \_ FLAGS.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_process_output_flags)

MFT: [**\_ enumeración \_ MFT PROCESS \_ OUTPUT \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags)



| DMO marca                                            | Marca MFT                                            |
|-----------------------------------------------------|-----------------------------------------------------|
| **\_DMO DESCARTE \_ DE SALIDA DE PROCESO CUANDO NO HAY \_ \_ \_ \_ BÚFER** | **DESCARTE DE SALIDA DEL PROCESO DE MFT \_ \_ CUANDO NO HAY \_ \_ \_ \_ BÚFER** |



 

DMO: DMO [**\_ \_ enumeración OUTPUT \_ DATA BUFFER \_ \_ FLAGS.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags)


MFT: [**\_ enumeración MFT \_ OUTPUT DATA BUFFER \_ \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_data_buffer_flags)



| DMO marca                                   | Marca MFT                                                                                                                                            |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DMO PUNTO \_ DE SINCRONIZACIÓN DE BÚFER DE DATOS DE \_ \_ SALIDA**  | No hay ninguna marca equivalente. En su lugar, compruebe el [**atributo MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) en el ejemplo. |
| **\_DMO TIEMPO DE \_ \_ BUFFERF DE DATOS \_ DE SALIDA**       | No hay ninguna marca equivalente. En su lugar, llame [**aSAMPLESample::GetSampleTime**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime) en el ejemplo.                                        |
| **\_DMO BUFFERF \_ DE DATOS DE SALIDA \_ \_ TIMELENGTH** | No hay ninguna marca equivalente. En su lugar, llame [**aSAMPLESample::GetSampleDuration**](/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampleduration) en el ejemplo.                                |
| **\_DMO BUFFERF \_ DE DATOS DE SALIDA \_ \_ INCOMPLETO** | **BÚFER DE DATOS DE SALIDA DE MFT \_ \_ \_ \_ INCOMPLETO**                                                                                                           |
| No hay ninguna marca equivalente.                        | **CAMBIO DE FORMATO \_ DEL BÚFER DE DATOS DE SALIDA \_ \_ \_ DE \_ MFT**                                                                                                       |
| No hay ninguna marca equivalente.                        | **FIN DEL FLUJO DE \_ BÚFER DE DATOS DE SALIDA \_ \_ \_ DE \_ MFT**                                                                                                          |
| No hay ninguna marca equivalente.                        | **BÚFER DE DATOS DE SALIDA DE MFT \_ \_ SIN \_ \_ \_ EJEMPLO**                                                                                                           |



 

### <a name="getinputstatus-flags"></a>Marcas GetInputStatus

DMO: **\_ DMO \_ enumeración INPUT \_ STATUS \_ FLAGS.**

MFT: [**\_ enumeración \_ MFT INPUT \_ STATUS \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_status_flags)



| DMO marca                              | Marca MFT                             |
|---------------------------------------|--------------------------------------|
| **\_DMO INPUT \_ STATUSF \_ ACCEPT \_ DATA** | **ACEPTACIÓN \_ DE DATOS EN EL ESTADO DE ENTRADA \_ \_ DE \_ MFT** |



 

### <a name="getoutputstatus-flags"></a>Marcas GetOutputStatus

DDO: no hay enumeración equivalente.

MFT: [**\_ enumeración \_ MFT OUTPUT \_ STATUS \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_status_flags)



| DMO marca            | Marca MFT                               |
|---------------------|----------------------------------------|
| No hay ninguna marca equivalente. | **EJEMPLO DE ESTADO DE SALIDA DE MFT \_ \_ \_ \_ LISTO** |



 

### <a name="getinputstreaminfo-flags"></a>Marcas GetInputStreamInfo

DMO: DMO [**\_ \_ enumeración INPUT \_ STREAM INFO \_ \_ FLAGS.**](/previous-versions/windows/embedded/aa451600(v=msdn.10))

MFT: [**\_ enumeración \_ MFT INPUT \_ STREAM INFO \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_input_stream_info_flags)



| DMO marca                                             | Marca MFT                                            |
|------------------------------------------------------|-----------------------------------------------------|
| **\_DMO EJEMPLOS \_ COMPLETOS DE STREAMF \_ DE \_ ENTRADA**              | **EJEMPLOS \_ COMPLETOS DE FLUJO \_ DE ENTRADA \_ DE \_ MFT**              |
| **\_DMO EJEMPLO \_ ÚNICO DE STREAMF DE ENTRADA \_ POR \_ \_ \_ BÚFER** | **EJEMPLO ÚNICO DE FLUJO DE ENTRADA DE MFT \_ \_ POR \_ \_ \_ \_ BÚFER** |
| **\_DMO TAMAÑO \_ DE MUESTRA FIJO DE STREAMF DE \_ \_ \_ ENTRADA**         | **TAMAÑO FIJO DE MUESTRA DEL FLUJO DE ENTRADA \_ \_ \_ DE \_ \_ MFT**         |
| **\_DMO INPUT \_ STREAMF \_ CONTIENE \_ BÚFERES**              | **EL FLUJO DE ENTRADA DE MFT \_ \_ CONTIENE \_ \_ BÚFERES**              |
| No hay ninguna marca equivalente.                                  | **EL FLUJO DE ENTRADA DE MFT \_ \_ NO AGREGA \_ \_ \_ ADDREF**           |
| No hay ninguna marca equivalente.                                  | **SECUENCIA DE ENTRADA DE MFT \_ \_ \_ EXTRAÍBLE**                   |
| No hay ninguna marca equivalente.                                  | **FLUJO DE ENTRADA DE MFT \_ \_ \_ OPCIONAL**                    |



 

### <a name="getoutputstreaminfo-flags"></a>Marcas GetOutputStreamInfo

DMO: DMO [**\_ \_ enumeración OUTPUT \_ STREAM INFO \_ \_ FLAGS.**](/previous-versions/ms806053(v=msdn.10))

MFT: [**\_ enumeración \_ MFT OUTPUT \_ STREAM INFO \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_output_stream_info_flags)



| DMO marca                                              | Marca MFT                                             |
|-------------------------------------------------------|------------------------------------------------------|
| **\_DMO EJEMPLOS \_ COMPLETOS DE STREAMF \_ DE \_ SALIDA**              | **EJEMPLOS \_ COMPLETOS DEL \_ FLUJO DE SALIDA \_ DE \_ MFT**              |
| **\_DMO EJEMPLO \_ ÚNICO DE STREAMF DE SALIDA \_ POR \_ \_ \_ BÚFER** | **EJEMPLO ÚNICO DE SECUENCIA DE SALIDA DE MFT \_ \_ POR \_ \_ \_ \_ BÚFER** |
| **\_DMO TAMAÑO \_ DE MUESTRA FIJO DE STREAMF DE \_ \_ \_ SALIDA**         | **TAMAÑO FIJO DE MUESTRA DEL FLUJO DE \_ \_ SALIDA DE \_ \_ \_ MFT**         |
| **\_DMO OUTPUT \_ STREAMF \_ DISCARDABLE**                 | **SECUENCIA DE SALIDA DE MFT \_ \_ \_ DESCARTABLE**                 |
| **\_DMO STREAMF \_ DE SALIDA \_ OPCIONAL**                    | **FLUJO DE SALIDA DE MFT \_ \_ \_ OPCIONAL**                    |
| No hay ninguna marca equivalente.                                   | **EL FLUJO DE SALIDA DE MFT \_ \_ PROPORCIONA \_ \_ EJEMPLOS**           |
| No hay ninguna marca equivalente.                                   | **EL FLUJO DE SALIDA DE MFT \_ \_ PUEDE PROPORCIONAR \_ \_ \_ EJEMPLOS**       |
| No hay ninguna marca equivalente.                                   | **LECTURA \_ \_ DIFERIDA DEL FLUJO DE \_ SALIDA DE \_ MFT**                  |
| No hay ninguna marca equivalente.                                   | **SECUENCIA DE SALIDA DE MFT \_ \_ \_ EXTRAÍBLE**                   |



 

### <a name="setinputtypesetoutputtype-flags"></a>Marcas SetInputType/SetOutputType

DMO: [**\_ DMO \_ enumeración SET \_ TYPE \_ FLAGS.**](/previous-versions/windows/desktop/api/Mediaobj/ne-mediaobj-_dmo_set_type_flags)

MFT: [**\_ enumeración MFT \_ SET TYPE \_ \_ FLAGS.**](/windows/win32/api/mftransform/ne-mftransform-_mft_set_type_flags)



| DMO marca                        | Marca MFT                                                                             |
|---------------------------------|--------------------------------------------------------------------------------------|
| **\_DMO SET \_ TYPEF \_ TEST \_ ONLY** | **SOLO PRUEBA \_ DE TIPO DE CONJUNTO DE \_ \_ \_ MFT**                                                       |
| **\_DMO SET \_ TYPEF \_ CLEAR**      | No hay ninguna marca equivalente. En su lugar, establezca el tipo de medio **en NULL** para borrar el tipo de medio. |



 

## <a name="error-codes"></a>Códigos de error

En la tabla siguiente se muestra cómo asignar DMO de error a códigos de error de MFT. Un objeto MFT/DMO híbrido debe devolver los códigos de error DMO de los métodos [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) y los códigos de error MFT de [**los métodos DETRANSFORMTransform.**](/windows/win32/api/mftransform/nn-mftransform-imftransform) Los DMO de error se definen en el archivo de encabezado MediaErr.h. Los códigos de error de MFT se definen en el archivo de encabezado mferror.h.



| DMO código de error                  | Código de error de MFT                       |
|---------------------------------|--------------------------------------|
| **\_DMO E \_ INVALIDTYPE**         | **MF \_ E \_ INVALIDTYPE**               |
| **\_DMO E \_ INVALIDSTREAMINDEX**  | **MF \_ E \_ INVALIDSTREAMNUMBER**       |
| **\_DMO E \_ NOTACCEPTING**        | **NOTACCEPTING DE MF \_ E \_**              |
| **\_DMO E \_ NO \_ MÁS \_ ELEMENTOS**     | **MF \_ E \_ NO \_ MORE \_ TYPES**           |
| **\_DMO TIPO \_ E \_ NO \_ ACEPTADO** | **MF \_ E \_ INVALIDMEDIATYPE**          |
| **\_DMO E \_ TYPE \_ NOT \_ SET**      | **TIPO \_ DE TRANSFORMACIÓN MF E NO \_ \_ \_ \_ ESTABLECIDO** |



 

## <a name="creating-hybrid-dmomft-objects"></a>Creación de objetos DMO/MFT híbridos

La [**interfaz DETRANSFORM se**](/windows/win32/api/mftransform/nn-mftransform-imftransform) basa de forma flexible en [**IMediaObject,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)que es la interfaz principal de objetos multimedia (DDO) de DirectX. Es posible crear objetos que exponen ambas interfaces. Sin embargo, esto puede provocar colisiones de nomenclatura, ya que las interfaces tienen algunos métodos que comparten el mismo nombre. Puede resolver este problema de una de estas dos maneras:

Solución 1: incluya la siguiente línea en la parte superior de cualquier archivo .cpp que contenga funciones MFT:

``` syntax
#define MFT_UNIQUE_METHOD_NAMES
```

Esto cambia la declaración de la interfaz [**DETRANSFORMTRANSFORM**](/windows/win32/api/mftransform/nn-mftransform-imftransform) para que la mayoría de los nombres de método tienen como prefijo "MFT". Por lo tanto, [**IMFTransform::P rocessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) se convierte en **IMFTransform::MFTProcessInput**, mientras [**que IMediaObject::P rocessInput mantiene**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) su nombre original. Esta técnica es más útil si va a convertir un DMO existente en un DMO/MFT híbrido. Puede agregar los nuevos métodos MFT sin cambiar los DMO métodos.

Solución 2: Use la sintaxis de C++ para eliminar la ambigüedad de los nombres heredados de más de una interfaz. Por ejemplo, declare la versión de MFT de [**ProcessInput**](/windows/win32/api/mftransform/nf-mftransform-imftransform-processinput) de la siguiente manera:

``` syntax
CMyHybridObject::IMFTransform::ProcessInput(...)
```

Declare la DMO de [**ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) de la siguiente forma:

``` syntax
CMyHybridObject::IMediaObject::ProcessInput(...)
```

Si realiza una llamada interna a un método dentro del objeto , puede usar esta sintaxis, pero si lo hace, invalidará el estado virtual del método. Una mejor manera de realizar llamadas desde dentro del objeto es la siguiente:

``` syntax
hr = ((IMediaObject*)this)->ProcessInput(...)
```

De este modo, si deriva otra clase de **CMyHybridObject** e invalida el método CMyHybridObject::IMediaObject::P rocessInput, se llama al método virtual correcto. Las DMO se documentan en la documentación DirectShow SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 
