---
description: En este tema se describe el procesamiento asincrónico de datos para transformaciones de Media Foundation (MFTs).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: MFTs asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a16950cf431eff16f2befb382a77910c49ccb2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705428"
---
# <a name="asynchronous-mfts"></a>MFTs asincrónico

En este tema se describe el procesamiento asincrónico de datos para transformaciones de Media Foundation (MFTs).

> [!Note]  
> Este tema se aplica a Windows 7 o posterior.

 

-   [Acerca de MFTs asincrónicos](#about-asynchronous-mfts)
-   [Requisitos generales](#general-requirements)
-   [Eventos](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Purgando](#draining)
-   [Vaciar](#flushing)
-   [Marcadores](#markers)
-   [Cambiar formato](#format-changes)
-   [Atributos](#attributes)
-   [Desbloqueo de MFTs asincrónicos](#unlocking-asynchronous-mfts)
-   [Apagar el MFT](#shutting-down-the-mft)
-   [Registro y enumeración](#registration-and-enumeration)
-   [Temas relacionados](#related-topics)

## <a name="about-asynchronous-mfts"></a>Acerca de MFTs asincrónicos

Cuando MFTs se introdujeron en Windows Vista, la API se diseñó para el procesamiento de datos *sincrónicos* . En ese modelo, la MFT siempre está esperando para obtener la entrada o en espera para producir la salida.

Considere un descodificador de vídeo típico. Para obtener un fotograma descodificado, el cliente llama a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Si el descodificador tiene suficientes datos para descodificar un fotograma, **ProcessOutput** se bloquea mientras la MFT descodifica el marco. De lo contrario, **ProcessOutput** devuelve **MF_E_TRANSFORM_NEED_MORE_INPUT**, que indica que el cliente debe llamar a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Este modelo funciona bien si el descodificador realiza todas las operaciones de descodificación en un subproceso. Pero supongamos que el descodificador usa varios subprocesos para descodificar fotogramas en paralelo. Para obtener el mejor rendimiento, el descodificador debe recibir una nueva entrada cada vez que un subproceso de descodificación se quede inactivo. Pero la velocidad a la que los subprocesos completan las operaciones de descodificación no se alinearán exactamente con las llamadas del cliente a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput), lo que da lugar a subprocesos que esperan el trabajo.

Windows 7 incluye un procesamiento *asincrónico* basado en eventos para MFTs. En este modelo, cada vez que la MFT necesita entrada o tiene salida, envía un evento al cliente.

## <a name="general-requirements"></a>Requisitos generales

En este tema se describe cómo difieren los MFTs asincrónicos del MFT sincrónico. Excepto donde se indica en este tema, los dos modelos de procesamiento son los mismos. (En concreto, la negociación de formato es la misma).

Un MFT asincrónico debe implementar las interfaces siguientes:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Events

Un MFT asincrónico usa los siguientes eventos para indicar su estado de procesamiento de datos:



| Evento                                                    | Descripción                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Se envía cuando la MFT puede aceptar más entradas.                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | Se envía cuando la MFT tiene salida.                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | Se envía cuando se completa una operación de purga. Vea [purgado](#draining). |
| [METransformMarker](metransformmarker.md)               | Se envía cuando un marcador es un proceso. Vea [marcadores](#markers).           |



 

Estos eventos se envían fuera de banda. Es importante comprender la diferencia entre los eventos en banda y fuera de banda en el contexto de una MFT.

El diseño de la MFT original admite eventos *en banda* . Un evento en banda contiene información sobre el flujo de datos, como información sobre un cambio de formato. El cliente envía eventos en banda a la MFT llamando a [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). MFT puede enviar eventos en banda de vuelta al cliente en el método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . (En concreto, los eventos se transmiten en el miembro **pEvents** de la estructura [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) ).

Una MFT envía eventos fuera de banda a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) como se indica a continuación:

1.  MFT implementa la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) , tal y como se describe en [generadores de eventos multimedia](media-event-generators.md).
2.  El cliente llama a **IUnknown:: QueryInterface** en el MFT para la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Una MFT asincrónica debe exponer esta interfaz. Los MFTs sincrónicos no deben exponer esta interfaz.
3.  El cliente llama a [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) y [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para recibir eventos fuera de banda de MFT.

## <a name="processinput"></a>ProcessInput

El método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) se modifica de la siguiente manera:

1.  Cuando se inicia el streaming, el cliente envía el mensaje de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
2.  Durante el streaming, MFT solicita datos mediante el envío de un evento [METransformNeedInput](metransformneedinput.md) . Los datos del evento son el identificador del flujo.
3.  Para cada evento [METransformNeedInput](metransformneedinput.md) , el cliente llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para la secuencia especificada.
4.  Al final del streaming, el cliente puede llamar a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .

Notas de implementación:

-   La MFT no debe enviar ningún evento [METransformNeedInput](metransformneedinput.md) hasta que reciba el mensaje de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) .
-   Durante el streaming, MFT puede enviar eventos [METransformNeedInput](metransformneedinput.md) en cualquier momento.
-   La MFT debe mantener un recuento de eventos de [METransformNeedInput](metransformneedinput.md) pendientes. Cualquier llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) que no corresponda a un evento METransformNeedInput debe devolver **MF_E_NOTACCEPTING**.
-   Cuando el MFT recibe el mensaje de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) , restablece el número de eventos pendientes de [METransformNeedInput](metransformneedinput.md) en cero.
-   La MFT no debe enviar ningún evento de [METransformNeedInput](metransformneedinput.md) después de recibir el mensaje de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) .
-   Si se llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) antes de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) o después de [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), el método debe devolver **MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

El método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) se modifica de la siguiente manera:

1.  Cada vez que la MFT tiene salida, envía un evento [METransformHaveOutput](metransformhaveoutput.md) .
2.  Para cada evento [METransformHaveOutput](metransformhaveoutput.md) , el cliente llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Notas de implementación:

-   Si el cliente llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en cualquier otro momento, el método devuelve **E_UNEXPECTED**.
-   Una MFT asincrónica nunca debe devolver **MF_E_TRANSFORM_NEED_MORE_INPUT** del método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) . Si la MFT requiere más entrada, envía un evento [METransformNeedInput](metransformneedinput.md) .

## <a name="draining"></a>Purgando

La purga de una MFT hace que la MFT genere tantas salidas como sea posible desde cualquier dato de entrada que ya se haya enviado. La purga de una MFT asincrónica funciona de la siguiente manera:

1.  El cliente envía el mensaje de [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) .
2.  La MFT sigue enviando eventos [METransformHaveOutput](metransformhaveoutput.md) hasta que no tiene más datos para procesar. No envía eventos [METransformNeedInput](metransformneedinput.md) durante este tiempo.
3.  Después de que el MFT envíe el último evento [METransformHaveOutput](metransformhaveoutput.md) , envía un evento [METransformDrainComplete](metransformdraincomplete.md) .

Una vez completada la purga, el MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) del cliente.

## <a name="flushing"></a>Vaciar

El cliente puede vaciar la MFT enviando el mensaje de [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) . La MFT quita todos los ejemplos de entrada y salida que contiene.

MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje de [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) del cliente.

## <a name="markers"></a>Marcadores

El cliente puede marcar un punto en la secuencia enviando el mensaje de [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) . La MFT responde de la siguiente manera:

1.  La MFT genera tantos ejemplos de salida como los datos de entrada existentes, y envía un evento [METransformHaveOutput](metransformhaveoutput.md) para cada ejemplo de salida.
2.  Una vez generada la salida, el MFT envía un evento [METransformMarker](metransformmarker.md) . Este evento se debe enviar después de todos los eventos [METransformHaveOutput](metransformhaveoutput.md) .

Por ejemplo, supongamos que un descodificador tiene suficientes datos de entrada para generar cuatro ejemplos de salida. Si el cliente envía el mensaje de [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) , la MFT pondrá en cola cuatro eventos [METransformHaveOutput](metransformhaveoutput.md) (uno por ejemplo de salida), seguidos de un evento [METransformMarker](metransformmarker.md) .

El mensaje de marcador es similar al mensaje de purga. Sin embargo, una purga se considera una interrupción en la secuencia, mientras que un marcador no lo es. Los marcadores de purga y tienen las siguientes diferencias.

Purgando

-   Durante la purga, el MFT no envía eventos [METransformNeedInput](metransformneedinput.md) .
-   La MFT descarta los datos de entrada que no se pueden usar para crear un ejemplo de salida.
-   Algunos MFTs producen un "tail" al final de los datos. Por ejemplo, los efectos de audio como reverberación o eco generan datos adicionales después de que los datos de entrada se hayan detenido. Una MFT que genera una cola debe hacerlo al final de una operación de purga.
-   Una vez finalizada la purga de MFT, marca el siguiente ejemplo de salida con el atributo [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) para indicar una discontinuidad en la secuencia.

Dor

-   La MFT sigue enviando eventos [METransformNeedInput](metransformneedinput.md) antes de enviar el evento de marcador.
-   MFT no descarta ningún dato de entrada. Si hay datos parciales, se deben procesar después del punto de marcador.
-   La MFT no produce una cola en el punto de marcador.
-   La MFT no establece la marca de discontinuidad después del punto de marcador.

## <a name="format-changes"></a>Cambiar formato

Un MFT asincrónico debe admitir los cambios de formato dinámico, tal y como se describe en [control de los cambios de flujo](handling-stream-changes.md).

## <a name="attributes"></a>Atributos

Un MFT asincrónico debe implementar el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para devolver un almacén de atributos válido. Los siguientes atributos se aplican a MFTs asincrónico:



| Atributo                                                                                    | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | MFT debe establecer este atributo en **true** (1). El cliente puede consultar este atributo para detectar si la MFT es asincrónica. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | MFT debe establecer este atributo en **true** (1). El cliente puede suponer que este atributo está establecido.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Desbloqueo de MFTs asincrónicos

Los MFTs asincrónicos no son compatibles con el modelo de procesamiento de datos de MFT original. Para evitar que los MFTs asincrónicos interrumpan las aplicaciones existentes, se define el mecanismo siguiente:

<dl> El cliente llama a <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform:: GetAttributes</a> en la MFT.  
El cliente consulta para este <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> atributo. En el caso de una MFT asincrónica, el valor de este atributo es **true**.  
Para desbloquear la MFT, el cliente debe establecer el atributo <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> en **true**.  
</dl>

Hasta que el cliente desbloquee la MFT, todos los métodos de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) deben devolver **MF_E_TRANSFORM_ASYNC_LOCKED**, con las siguientes excepciones:

-   [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (todos los MFTs asincrónicos)
-   [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (todos los MFTs asincrónicos)
-   [**IMFTransform:: GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (solo codificadores)
-   [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (solo codificadores)
-   [**IMFTransform:: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (todos los MFTs asincrónicos)
-   [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (todos los MFTs asincrónicos)

En el código siguiente se muestra cómo desbloquear una MFT asincrónica:


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>Apagar el MFT

Los MFTs asincrónicos deben implementar la interfaz [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) .

-   [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown): la MFT debe apagar su cola de eventos. Si usa la cola de eventos estándar, llame a [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Opcionalmente, el MFT puede liberar otros recursos. El cliente no debe usar MFT después de llamar a **Shutdown**.
-   [**GetShutdownStatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus): una vez llamado el [**cierre**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) , el MFT debe devolver el valor **MFSHUTDOWN_COMPLETED** en el parámetro *pStatus* . No debe devolver el valor **MFSHUTDOWN_INITIATED**.

## <a name="registration-and-enumeration"></a>Registro y enumeración

Para registrar un MFT asincrónico, llame a la función [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) y establezca la marca **MFT_ENUM_FLAG_ASYNCMFT** en el parámetro *Flags* . (Anteriormente se ha reservado esta marca).

Para enumerar MFTs asincrónicos, llame a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) y establezca la marca **MFT_ENUM_FLAG_ASYNCMFT** en el parámetro *Flags* . Por compatibilidad con versiones anteriores, la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) no enumera MFTs asincrónico. De lo contrario, la instalación de un MFT asíncrono en el equipo del usuario podría interrumpir las aplicaciones existentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



