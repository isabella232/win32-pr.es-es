---
description: En este tema se describe el procesamiento asincrónico de datos Media Foundation transformaciones (MTA).
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: MFT asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cab2ef683ef22fd22a911c045a1a744f1c0d561b3e8e66d46ca2cf6c6f0ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959525"
---
# <a name="asynchronous-mfts"></a>MFT asincrónicas

En este tema se describe el procesamiento asincrónico de datos Media Foundation transformaciones (MTA).

> [!Note]  
> Este tema se aplica a Windows 7 o posterior.

 

-   [Acerca de las MTO asincrónicas](#about-asynchronous-mfts)
-   [Requisitos generales](#general-requirements)
-   [Eventos](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Purgando](#draining)
-   [Lavado](#flushing)
-   [Marcadores](#markers)
-   [Cambios de formato](#format-changes)
-   [Atributos](#attributes)
-   [Desbloqueo de MTA asincrónicas](#unlocking-asynchronous-mfts)
-   [Apagar el MFT](#shutting-down-the-mft)
-   [Registro y enumeración](#registration-and-enumeration)
-   [Temas relacionados](#related-topics)

## <a name="about-asynchronous-mfts"></a>Acerca de las MTO asincrónicas

Cuando se introdujeron las MTA en Windows Vista, la API se diseñó para el *procesamiento de datos sincrónico.* En ese modelo, el MFT siempre está esperando para obtener la entrada o esperando para generar la salida.

Considere un descodificador de vídeo típico. Para obtener un marco descodificado, el cliente llama [**a IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Si el descodificador tiene suficientes datos para descodificar un fotograma, **ProcessOutput** se bloquea mientras MFT descodifica el fotograma. De lo contrario, **ProcessOutput** **devuelve MF_E_TRANSFORM_NEED_MORE_INPUT**, lo que indica que el cliente debe llamar a [**ASETransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

Este modelo funciona bien si el descodificador realiza todas sus operaciones de descodificación en un subproceso. Pero supongamos que el descodificador usa varios subprocesos para descodificar fotogramas en paralelo. Para obtener el mejor rendimiento, el descodificador debe recibir una entrada nueva cada vez que un subproceso de descodificación se queda inactivo. Pero la velocidad a la que los subprocesos completan las operaciones de descodización no se alineará exactamente con las llamadas del cliente a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)lo que da lugar a subprocesos que esperan trabajo.

Windows 7 presenta el procesamiento asincrónico *controlado* por eventos para MTA. En este modelo, cada vez que MFT necesita entrada o tiene salida, envía un evento al cliente.

## <a name="general-requirements"></a>Requisitos generales

En este tema se describe cómo difieren las MFT asincrónicas de MFT sincrónica. Excepto donde se indica en este tema, los dos modelos de procesamiento son los mismos. (En concreto, la negociación de formato es la misma).

Un MFT asincrónico debe implementar las interfaces siguientes:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Eventos

Un MFT asincrónico usa los siguientes eventos para indicar su estado de procesamiento de datos:



| Evento                                                    | Descripción                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Se envía cuando MFT puede aceptar más entradas.                          |
| [METransformTransformTransformOutput](metransformhaveoutput.md)       | Se envía cuando MFT tiene salida.                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | Se envía cuando se completa una operación de purga. Vea [Purgar](#draining). |
| [METransformMarker](metransformmarker.md)               | Se envía cuando se procesa un marcador. Vea [Marcadores](#markers).           |



 

Estos eventos se envían fuera de banda. Es importante comprender la diferencia entre los eventos en banda y fuera de banda en el contexto de un MFT.

El diseño original de MFT admite *eventos en* banda. Un evento en banda contiene información sobre el flujo de datos, como información sobre un cambio de formato. El cliente envía eventos en banda a MFT mediante una llamada [**a IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). MFT puede devolver eventos en banda al cliente en el [**método ProcessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) (En concreto, los eventos se transmiten en el **miembro pEvents** de la [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) estructura).

Un MFT envía eventos fuera de banda a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) como se muestra a continuación:

1.  MFT implementa la interfaz [**IMFMediaEventGenerator,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) como se describe en [Generadores de eventos multimedia](media-event-generators.md).
2.  El cliente llama **a IUnknown::QueryInterface en** el MFT para la interfaz [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Un MFT asincrónico debe exponer esta interfaz. Las MTA sincrónicas no deben exponer esta interfaz.
3.  El cliente llama [**a IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) y [**ASEMEDIAEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para recibir eventos fuera de banda de MFT.

## <a name="processinput"></a>ProcessInput

El [**método IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) se modifica de la siguiente manera:

1.  Cuando se inicia el streaming, el cliente envía el [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) mensaje.
2.  Durante el streaming, MFT solicita datos mediante el envío de [un evento METransformNeedInput.](metransformneedinput.md) Los datos del evento son el identificador de flujo.
3.  Para cada [evento METransformNeedInput,](metransformneedinput.md) el cliente llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para la secuencia especificada.
4.  Al final del streaming, el cliente puede llamar a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) mensaje.

Notas de implementación:

-   El MFT no debe enviar ningún [evento METransformNeedInput](metransformneedinput.md) hasta que reciba el [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) mensaje.
-   Durante el streaming, MFT puede enviar [eventos METransformNeedInput](metransformneedinput.md) en cualquier momento.
-   El MFT debe mantener un recuento de eventos [METransformNeedInput pendientes.](metransformneedinput.md) Cualquier llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) que no se corresponda con un evento METransformNeedInput debe **devolver MF_E_NOTACCEPTING**.
-   Cuando el MFT recibe el [**MFT_MESSAGE_NOTIFY_END_OF_STREAM,**](mft-message-notify-end-of-stream.md) restablece el recuento de eventos [METransformNeedInput](metransformneedinput.md) pendientes en cero.
-   El MFT no debe enviar ningún [evento METransformNeedInput](metransformneedinput.md) después de recibir el [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) mensaje.
-   Si [**se llama a ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) antes [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) o después [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md), el método debe **devolver MF_E_NOTACCEPTING**.

## <a name="processoutput"></a>ProcessOutput

El [**método IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) se modifica de la siguiente manera:

1.  Cada vez que MFT tiene salida, envía un [evento METransformTransformTransformOutput.](metransformhaveoutput.md)
2.  Para cada [evento METransformTransformTransformOutput,](metransformhaveoutput.md) el cliente llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Notas de implementación:

-   Si el cliente llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en cualquier otro momento, el método devuelve **E_UNEXPECTED**.
-   Un MFT asincrónico nunca debe devolver **MF_E_TRANSFORM_NEED_MORE_INPUT** del [**método ProcessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Si MFT requiere más entrada, envía un [evento METransformNeedInput.](metransformneedinput.md)

## <a name="draining"></a>Purgando

Purgar un MFT hace que MFT produzca tanta salida como sea posible a partir de los datos de entrada que ya se hayan enviado. Purgar un MFT asincrónico funciona de la siguiente manera:

1.  El cliente envía el [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) mensaje.
2.  MFT continúa enviando [eventos METransformTransformTransformOutput](metransformhaveoutput.md) hasta que no tiene más datos para procesar. No envía eventos [METransformNeedInput](metransformneedinput.md) durante este tiempo.
3.  Una vez que MFT envía el último [evento METransformTransformTransformOutput,](metransformhaveoutput.md) envía un [evento METransformDrainComplete.](metransformdraincomplete.md)

Una vez completada la purga, MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un [**mensaje MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) del cliente.

## <a name="flushing"></a>Lavado

El cliente puede vaciar el MFT mediante el [**envío**](mft-message-command-flush.md) MFT_MESSAGE_COMMAND_FLUSH mensaje. El MFT quita todos los ejemplos de entrada y salida que está manteniendo.

El MFT no envía otro [evento METransformNeedInput](metransformneedinput.md) hasta que recibe un [**mensaje MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) del cliente.

## <a name="markers"></a>Marcadores

El cliente puede marcar un punto en la secuencia mediante el envío del [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) mensaje. El MFT responde de la siguiente manera:

1.  El MFT genera tantos ejemplos de salida como sea posible a partir de los datos de entrada existentes, enviando un [evento METransformTransformTransformOutput](metransformhaveoutput.md) para cada ejemplo de salida.
2.  Una vez generada toda la salida, MFT envía un [evento METransformMarker.](metransformmarker.md) Este evento debe enviarse después de todos los [eventos METransformTransformTransformOutput.](metransformhaveoutput.md)

Por ejemplo, supongamos que un descodificador tiene suficientes datos de entrada para generar cuatro muestras de salida. Si el cliente envía el [**MFT_MESSAGE_COMMAND_MARKER,**](mft-message-command-marker.md) MFT pondrá en cola cuatro eventos [METransformTransformTransformOutput](metransformhaveoutput.md) (uno por ejemplo de salida), seguidos de un [evento METransformMarker.](metransformmarker.md)

El mensaje de marcador es similar al mensaje de purga. Sin embargo, una purga se considera una interrupción en la secuencia, mientras que un marcador no lo es. El purgado y los marcadores tienen las siguientes diferencias.

Drenaje:

-   Mientras se purga, MFT no envía [eventos METransformNeedInput.](metransformneedinput.md)
-   El MFT descarta los datos de entrada que no se pueden usar para crear un ejemplo de salida.
-   Algunas MTA generan una "cola" al final de los datos. Por ejemplo, los efectos de audio, como la reverberación o el eco, generan datos adicionales después de que se detengan los datos de entrada. Un MFT que genera una cola debe hacerlo al final de una operación de purga.
-   Una vez que MFT ha terminado de purgar, marca el siguiente ejemplo de salida con el atributo [**MFSampleExtension_Discontinuity,**](mfsampleextension-discontinuity-attribute.md) para indicar una discontinuidad en la secuencia.

Marcador:

-   MFT continúa enviando eventos [METransformNeedInput](metransformneedinput.md) antes de enviar el evento de marcador.
-   El MFT no descarta ningún dato de entrada. Si hay datos parciales, se deben procesar después del punto de marcador.
-   El MFT no genera una cola en el punto de marcador.
-   El MFT no establece la marca de discontinuidad después del punto de marcador.

## <a name="format-changes"></a>Cambios de formato

Un MFT asincrónico debe admitir cambios de formato dinámico, como se describe en [Control de cambios de flujo.](handling-stream-changes.md)

## <a name="attributes"></a>Atributos

Un MFT asincrónico debe implementar el [**método IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para devolver un almacén de atributos válido. Los atributos siguientes se aplican a las MTA asincrónicas:



| Atributo                                                                                    | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | El MFT debe establecer este atributo en **TRUE** (1). El cliente puede consultar este atributo para detectar si MFT es asincrónico. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | El MFT debe establecer este atributo en **TRUE** (1). El cliente puede suponer que este atributo está establecido.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Desbloqueo de MTA asincrónicos

Las MTA asincrónicas no son compatibles con el modelo de procesamiento de datos MFT original. Para evitar que las MTA asincrónicas rompa las aplicaciones existentes, se define el mecanismo siguiente:

<dl> El cliente llama <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">a IMFTransform::GetAttributes</a> en MFT.  
El cliente consulta para este <a href="mf-transform-async.md">atributo MF_TRANSFORM_ASYNC.</a> Para un MFT asincrónico, el valor de este atributo es **TRUE.**  
Para desbloquear el MFT, el cliente debe establecer el <a href="mf-transform-async-unlock.md">atributo MF_TRANSFORM_ASYNC_UNLOCK</a> en **TRUE.**  
</dl>

Hasta que el cliente desbloquee MFT, todos los métodos [**DETRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) deben **devolver** MF_E_TRANSFORM_ASYNC_LOCKED , con las siguientes excepciones:

-   [**MFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (todos los MFT asincrónicos)
-   [**MFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (todos los MFT asincrónicos)
-   [**IMFTransform::GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (solo codificadores)
-   [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (solo codificadores)
-   [**MFTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (todos los MFT asincrónicos)
-   [**MFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (todos los MFT asincrónicos)

El código siguiente muestra cómo desbloquear un MFT asincrónico:


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

Las MTA asincrónicas deben implementar la [**interfaz DE APAGADO DE MFS.**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

-   [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown): MFT debe apagar su cola de eventos. Si usa la cola de eventos estándar, llame [**a IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Opcionalmente, MFT puede liberar otros recursos. El cliente no debe usar el MFT después de llamar a **Shutdown**.
-   [**GetShutdownStatus:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus)después de llamar a [**Shutdown,**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) MFT debe devolver el valor **MFSHUTDOWN_COMPLETED** en el *parámetro pStatus.* No debe devolver el **valor** MFSHUTDOWN_INITIATED .

## <a name="registration-and-enumeration"></a>Registro y enumeración

Para registrar un MFT asincrónico, llame a la [**función MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) y **establezca la MFT_ENUM_FLAG_ASYNCMFT** en el parámetro *Flags.* (Anteriormente, esta marca estaba reservada).

Para enumerar las MFT asincrónicas, llame a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) y **establezca la MFT_ENUM_FLAG_ASYNCMFT** en el parámetro *Flags.* Por compatibilidad con versiones anteriores, [**la función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) no enumera los MFTT asincrónicos. De lo contrario, la instalación de un MFT asincrónico en el equipo del usuario podría interrumpir las aplicaciones existentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



