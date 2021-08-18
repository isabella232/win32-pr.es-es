---
description: En este tema se describe cómo un cliente usa una Media Foundation transformación de datos (MFT) para procesar datos. El cliente es todo lo que llama directamente a métodos en MFT. Podría ser la aplicación o la Media Foundation ejecución.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Modelo básico de procesamiento de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a1edb0c5144c6e3a3e1825e637cd5d19049699ad60bbf764629c9ade7cd3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035462"
---
# <a name="basic-mft-processing-model"></a>Modelo básico de procesamiento de MFT

En este tema se describe cómo un cliente usa una Media Foundation transformación de datos (MFT) para procesar datos. El *cliente* es todo lo que llama directamente a métodos en MFT. Podría ser la aplicación o la Media Foundation ejecución.

Lea este tema si:

-   Escribir una aplicación que realiza llamadas directas a uno o varios MTA.
-   Escribir un MFT personalizado y desea comprender el comportamiento esperado de un MFT.

En este tema se describe un *modelo de procesamiento sincrónico.* En este modelo, todos los métodos de procesamiento de datos se bloquean hasta que se completan. Las MTA también pueden admitir *un modelo* asincrónico, que se describe en el tema [MfTs asincrónicos.](asynchronous-mfts.md)

-   [Modelo de procesamiento básico](#basic-processing-model)
    -   [Creación de MFT](#create-the-mft)
    -   [Obtener identificadores de flujo](#get-stream-identifiers)
    -   [Establecer tipos de medios](#set-media-types)
    -   [Obtener requisitos de búfer](#get-buffer-requirements)
    -   [Procesar datos](#process-data)
-   [Extensiones del modelo básico](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [Vaciado de un MFT](#flushing-an-mft)
-   [Purgar un MFT](#draining-an-mft)
-   [Atributos de ejemplo](#sample-attributes)
-   [Discontinuidades](#discontinuities)
-   [Cambios de formato dinámico](#dynamic-format-changes)
-   [Transmisión de eventos](#stream-events)
-   [Temas relacionados](#related-topics)

## <a name="basic-processing-model"></a>Modelo de procesamiento básico

### <a name="create-the-mft"></a>Creación de MFT

Hay varias maneras de crear un MFT:

-   Llame a [**la función MFTEnum.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
-   Llame a [**la función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
-   Si ya conoce el CLSID de MFT, simplemente llame a **CoCreateInstance**.

Algunas MTA pueden proporcionar otras opciones, como una función de creación especializada.

### <a name="get-stream-identifiers"></a>Obtener identificadores de flujo

Un MFT tiene una o varias *secuencias*. Los flujos de entrada reciben datos de entrada y los flujos de salida generan datos de salida. Secuencias no se representan como objetos distintos. En su lugar, varios métodos MFT toman identificadores de flujo como parámetros.

Algunas MTA permiten al cliente agregar o quitar flujos de entrada. Durante el streaming, un MFT puede agregar o quitar flujos de salida. (El cliente no puede agregar ni quitar flujos de salida).

1.  (Opcional). Llame [**a IMFTransform::GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) para obtener el número mínimo y máximo de secuencias que MFT puede admitir. Si el mínimo y el máximo son los mismos, MFT tiene un número fijo de secuencias.
2.  Llame [**a IMFTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) para obtener el número inicial de secuencias.
3.  Llame [**a IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) para obtener los identificadores de flujo. Si este método devuelve E NOTIMPL, significa que MFT tiene un número fijo de secuencias y los identificadores de flujo son consecutivos a \_ partir de cero.
4.  (Opcional). Si MFT no tiene un número fijo de secuencias, llame a [**IMFTransform::AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) para agregar más flujos de entrada, o [**BIEN a IMFTransform::D eleteInputStream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) para quitar flujos de entrada. (No se pueden agregar ni quitar flujos de salida).

### <a name="set-media-types"></a>Establecer tipos de medios

Para que un MFT pueda procesar datos, el cliente debe establecer un tipo de medio para cada uno de los flujos de MFT. Un MFT puede requerir que el cliente establezca los tipos de entrada antes de establecer los tipos de salida, o puede requerir el orden opuesto (tipos de salida en primer lugar). Algunas MTA no tienen un requisito en el pedido.

Un MFT puede proporcionar una lista de tipos de medios preferidos para una secuencia. Además, las MTA pueden indicar los formatos generales que admiten agregando esta información al registro.

Para establecer los tipos de medios, haga lo siguiente:

1.  (Opcional). Para cada flujo de entrada, llame [**a IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obtener la lista de tipos preferidos para esa secuencia.
    -   Si este método devuelve MF E TRANSFORM TYPE NOT SET, debe establecer primero los tipos de salida; vaya \_ al \_ paso \_ \_ \_ 3.
    -   Si el método devuelve E NOTIMPL, MFT no tiene una lista de tipos de entrada preferidos; vaya \_ al paso 2.
2.  Para cada flujo de entrada, llame [**a IMFTransform::SetInputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) establecer el tipo de entrada. Puede usar un tipo de medio del paso 1 o un tipo que describa los datos de entrada. Si alguna secuencia devuelve MF \_ E TRANSFORM TYPE NOT \_ \_ \_ \_ SET, vaya al paso 3.
3.  (Opcional). Para cada flujo de salida, llame a [**IMFTransform::GetOutputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) obtener una lista de los tipos preferidos para esa secuencia.
    -   Si este método devuelve MF E TRANSFORM TYPE NOT SET, debe establecer primero los tipos de \_ \_ \_ \_ \_ entrada; vuelva al paso 1.
    -   Si alguna secuencia devuelve E NOTIMPL, MFT no tiene una lista de tipos de salida preferidos; vaya \_ al paso 4.
4.  Para cada flujo de salida, llame [**a IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de salida. Puede usar un tipo de medio del paso 3 o un tipo que describa el formato de salida necesario.
5.  Si algún flujo de entrada no tiene un tipo de medio, vuelva al paso 1.

### <a name="get-buffer-requirements"></a>Obtener requisitos de búfer

Después de que el cliente establece los tipos de medios, debe obtener los requisitos de búfer para cada secuencia:

-   Para cada flujo de entrada, llame [**a IMFTransform::GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Para cada flujo de salida, llame [**a IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Procesar datos

Un MFT está diseñado para ser una máquina de estado confiable. No realiza ninguna llamada al cliente.

1.  Llame [**a IMFTransform::P rocessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) el mensaje [**\_ MFT MESSAGE NOTIFY BEGIN \_ \_ \_ STREAMING.**](mft-message-notify-begin-streaming.md) Este mensaje solicita al MFT que asigne los recursos que necesita durante el streaming.
2.  Llame [**a IMFTransform::P rocessInput en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) al menos un flujo de entrada para entregar una muestra de entrada a MFT.
3.  (Opcional). Llame [**a IMFTransform::GetOutputStatus para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) consultar si MFT puede generar un ejemplo de salida. Si el método devuelve S \_ OK, compruebe el *parámetro pdwFlags.* Si *pdwFlags contiene la* marca **MFT OUTPUT STATUS SAMPLE \_ \_ \_ \_ READY,** vaya al paso 4. Si *pdwFlags* es cero, vuelva al paso 2. Si el método devuelve E \_ NOTIMPL, vaya al paso 4.
4.  Llame [**a IMFTransform::P rocessOutput para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) obtener los datos de salida.
    -   Si el método devuelve **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT**, significa que MFT requiere más datos de entrada; vuelva al paso 2.
    -   Si el método devuelve **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE**, significa que el número de flujos de salida ha cambiado o que el formato de salida ha cambiado. Es posible que el cliente tenga que consultar nuevos identificadores de flujo o establecer nuevos tipos de medios. Para obtener más información, vea la documentación de [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Si todavía hay datos de entrada que procesar, vaya al paso 2. Si MFT ha consumido todos los datos de entrada disponibles, continúe con el paso 6.
6.  Llame [**a ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el [**mensaje MFT MESSAGE NOTIFY END \_ OF \_ \_ \_ \_ STREAM.**](mft-message-notify-end-of-stream.md)
7.  Llame [**a ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje DRAIN [**del comando MFT \_ MESSAGE. \_ \_**](mft-message-command-drain.md)
8.  Llame [**a ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener el resultado restante. Repita este paso hasta que el método devuelva **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT**. Este valor devuelto indica que toda la salida se ha purgado del MFT. (No trate esto como una condición de error).

La secuencia que se describe aquí mantiene el máximo de datos posible en MFT. Después de cada llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), el cliente intenta obtener la salida. Es posible que se necesiten varias muestras de entrada para generar una muestra de salida o que una sola muestra de entrada genere varios ejemplos de salida. El comportamiento óptimo para el cliente es extraer ejemplos de salida del MFT hasta que MFT requiera más entrada.

Sin embargo, el MFT debe ser capaz de controlar un orden diferente de llamadas de método por parte del cliente. Por ejemplo, el cliente podría alternar simplemente entre las llamadas a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). El MFT debe restringir la cantidad de entrada que obtiene devolviendo **MF \_ E \_ NOTACCEPTING** desde **ProcessInput** siempre que tenga algún resultado que generar.

El orden de las llamadas de método que se describen aquí no es la única secuencia válida de eventos. Por ejemplo, los pasos 3 y 4 suponen que el cliente comienza con los tipos de entrada y, a continuación, prueba los tipos de salida. El cliente también puede invertir este orden y empezar con los tipos de salida. En cualquier caso, si MFT requiere el orden opuesto, debe devolver el código de error MF \_ E TRANSFORM TYPE NOT \_ \_ \_ \_ SET.

El cliente puede llamar a métodos informativos, como [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) y [**GetOutputStreamInfo,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)en cualquier momento durante el streaming. El cliente también puede intentar cambiar los tipos de medios en cualquier momento. El MFT debe devolver un código de error si no se trata de una operación válida. En resumen, las MTA deben asumir muy poco sobre el orden de las operaciones, aparte de lo que se documenta en las propias llamadas.

En el diagrama siguiente se muestra un gráfico de flujo de los procedimientos descritos en este tema.

![diagrama de flujo que conduce desde obtener identificadores de flujo a través de bucles que establecen tipos de entrada, obtienen entrada y procesan la salida](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Extensiones para el modelo básico

Opcionalmente, un MFT puede admitir algunas extensiones para el modelo de streaming básico.

-   Secuencias de lectura diferida. Si el [**método IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve la marca **\_ MFT OUTPUT \_ STREAM \_ LAZY \_ READ** para un flujo de salida, el cliente no tiene que recopilar datos de ese flujo de salida. MFT sigue aceptando la entrada y, en algún momento, el MFT descartará los datos de salida de esa secuencia. Si todos los flujos de salida tienen esta marca, el MFT nunca producirá un error al aceptar la entrada. Un ejemplo podría ser una transformación de visualización, donde el cliente obtiene la salida solo cuando tiene ciclos de CPU de reserva para dibujar la visualización.
-   Secuencias descartables. Si el [**método GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve la marca **\_ MFT OUTPUT \_ STREAM \_ DISCARDABLE** para un flujo de salida, el cliente puede solicitar al MFT que descarte la salida, pero MFT no descartará ninguna salida a menos que se solicite. Cuando MFT alcanza su búfer de entrada máximo, el cliente debe recopilar algunos datos de salida o solicitar al MFT que descarte la salida.
-   Secuencias opcionales. Si el método [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve la marca **MFT \_ OUTPUT STREAM \_ \_ OPTIONAL** para un flujo de salida o el método [**IMFTransform::GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) devuelve la marca **MFT INPUT STREAM \_ \_ \_ OPTIONAL** para un flujo de entrada, esa secuencia es opcional. El cliente no tiene que establecer un tipo de medio en la secuencia. Si el cliente no establece el tipo, la secuencia se deselecciona. Un flujo de salida deseleccionado no genera ejemplos y el cliente no proporciona un búfer para la secuencia cuando llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un flujo de entrada no seleccionado no acepta datos de entrada. Un MFT puede marcar todos sus flujos de entrada y salida como opcionales. Sin embargo, se espera que se deba seleccionar al menos una entrada y una salida para que MFT funcione.
-   Procesamiento asincrónico. El modelo de procesamiento asincrónico se introdujo en Windows 7. Se describe en el tema [Mfts asincrónicos.](asynchronous-mfts.md)

## <a name="imf2dbuffer"></a>IMF2DBuffer

Si un MFT procesa datos de vídeo sin comprimir, debe usar la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) para manipular los búferes de ejemplo. Para obtener esta interfaz, consulte la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) en cualquier búfer de entrada o salida. No usar esta interfaz cuando está disponible puede dar lugar a copias de búfer adicionales. Para hacer un uso adecuado de esta interfaz, la transformación no debe bloquear el búfer mediante la interfaz **DEMEMEDIABuffer** cuando **ESTÁ DISPONIBLE EL BUFFER2DBuffer.**

Para obtener más información sobre el procesamiento de datos de vídeo, vea [Búferes de vídeo sin comprimir.](uncompressed-video-buffers.md)

## <a name="flushing-an-mft"></a>Vaciar un MFT

*El vaciado de* un MFT hace que MFT descarte todos sus datos de entrada. Esto puede provocar una interrupción en el flujo de salida. Normalmente, un cliente vaciaría un MFT antes de buscar un nuevo punto en el flujo de entrada o cambiar a un nuevo flujo de entrada, cuando al cliente no le interesa perder datos.

Para vaciar un MFT, llame [**a LAQTransform::P rocessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) el [**mensaje FLUSH del comando MFT \_ MESSAGE. \_ \_**](mft-message-command-flush.md)

## <a name="draining-an-mft"></a>Purgar un MFT

*Purgar* un MFT hace que MFT produzca tanta salida como sea posible a partir de los datos de entrada que ya se hayan enviado. Si MFT no puede generar un ejemplo de salida completo a partir de la entrada disponible, quitará los datos de entrada. Normalmente, un cliente purgaría un MFT cuando llegó al final de la secuencia de origen, o inmediatamente antes de un cambio de formato en la secuencia de origen. Para purgar un MFT, haga lo siguiente:

1.  Llame [**a ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el [**mensaje DE PURGA DEL COMANDO \_ \_ MFT \_ MESSAGE.**](mft-message-command-drain.md) Este mensaje notifica al MFT que debe entregar tantos datos de salida como sea posible a partir de los datos de entrada que ya se han enviado.
2.  Llame [**a ProcessOutput para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) obtener los datos de salida, hasta que el método devuelva MF E TRANSFORM NEED MORE **\_ \_ \_ \_ \_ INPUT**.

Mientras se está purgando el MFT, no aceptará más entradas.

## <a name="sample-attributes"></a>Atributos de ejemplo

Los ejemplos de entrada pueden tener atributos que se deben copiar en los ejemplos de salida correspondientes.

-   Si MFT devuelve **VARIANT \_ TRUE para** la propiedad [**MFPKEY \_ EXATTRIBUTE \_ SUPPORTED,**](mfpkey-exattribute-supported-property.md) MFT debe copiar los atributos.
-   Si la [**propiedad MFPKEY \_ EXATTRIBUTE \_ SUPPORTED**](mfpkey-exattribute-supported-property.md) es **VARIANT \_ FALSE** o no está establecida, el cliente debe copiar los atributos.

Para un MFT con una entrada y una salida, puede usar la siguiente regla general:

-   Si cada ejemplo de entrada genera exactamente un ejemplo de salida, puede permitir que el cliente copie los atributos. Deje la [**propiedad MFPKEY \_ EXATTRIBUTE \_ SUPPORTED**](mfpkey-exattribute-supported-property.md) sin conjunto.
-   Si no hay una correspondencia uno a uno entre los ejemplos de entrada y los ejemplos de salida, MFT debe determinar los atributos correctos para los ejemplos de salida. Establezca la [**propiedad MFPKEY \_ EXATTRIBUTE \_ SUPPORTED**](mfpkey-exattribute-supported-property.md) en **VARIANT \_ TRUE.**

## <a name="discontinuities"></a>Discontinuidades

Una discontinuidad es una interrupción en una secuencia de audio o vídeo. Las discontinuidades pueden deberse a la pérdida de paquetes en una conexión de red, datos de archivos dañados, un cambio de una secuencia de origen a otra o una amplia gama de otras causas. Las discontinuidades se señalizan estableciendo el atributo [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) en el primer ejemplo después de la discontinuidad. No es posible señalar una discontinuidad en medio de una muestra. Por lo tanto, los datos discontinuos se deben enviar en ejemplos independientes.

Algunas transformaciones, especialmente las que controlan datos sin comprimir, como los efectos de audio y vídeo, deben omitir las discontinuidades al procesar los datos de entrada. Por lo general, estas MTA están diseñadas para controlar los datos continuos y deben tratar los datos que reciben como continuos, incluso después de una discontinuidad.

Si un MFT omite una discontinuidad en los datos de entrada, debe establecer la marca de discontinuidad en el ejemplo de salida, si la muestra de salida tiene la misma marca de tiempo que la muestra de entrada. Sin embargo, si el ejemplo de salida tiene una marca de tiempo diferente, MFT no debe propagar la discontinuidad. (Este sería el caso en algunos ejemplos de audio, por ejemplo). Una discontinuidad en el lugar incorrecto de la secuencia es peor que ninguna discontinuidad.

La mayoría de los descodificadores no pueden omitir las discontinuidades, porque una discontinuidad afecta a la interpretación del ejemplo siguiente. Cualquier tecnología de codificación que use la compresión entre fotogramas, como MPEG-2, se incluye en esta categoría. Algunos esquemas de codificación solo usan la compresión dentro del marco, como DV y MZIPEG. Estos descodificadores pueden omitir de forma segura las discontinuidades.

Las transformaciones que responden a discontinuidades generalmente deben generar tantos datos antes de la discontinuidad como puedan y descartar el resto. El ejemplo de entrada con la marca de discontinuidad debe procesarse como si fuera la primera muestra de la secuencia. (Este comportamiento coincide con lo que se especifica para el mensaje DE PURGA [**DEL \_ COMANDO \_ MFT \_ MESSAGE).**](mft-message-command-drain.md) Sin embargo, los detalles exactos dependerán del formato multimedia.

Si un descodificador no hace nada para mitigar una discontinuidad, debe copiar la marca de discontinuidad en los datos de salida. Los demultiplexores y otras MTA que funcionan completamente con datos comprimidos deben copiar las discontinuidades en sus flujos de salida. De lo contrario, es posible que los componentes de nivel inferior no puedan descodificar los datos comprimidos correctamente. En general, casi siempre es correcto pasar discontinuidades de bajada, a menos que MFT contenga código explícito para suavizar las discontinuidades.

## <a name="dynamic-format-changes"></a>Cambios de formato dinámico

Los formatos pueden cambiar durante el streaming. Por ejemplo, la relación de aspecto puede cambiar en medio de una secuencia de vídeo.

Para obtener más información sobre cómo un MFT controla los cambios de flujo, vea [Control de cambios de flujo.](handling-stream-changes.md)

## <a name="stream-events"></a>Transmisión de eventos

Para enviar un evento a un MFT, llame [**a IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Si el método devuelve **MF S TRANSFORM DO NOT PROPAGATE \_ \_ \_ \_ \_ \_ EVENT**, MFT devolverá el evento al autor de la llamada en una llamada posterior a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Si el método devuelve cualquier otro **valor HRESULT,** MFT no devolverá el evento al cliente en **ProcessOutput**. En ese caso, el cliente es responsable de propagar el evento de bajada al siguiente componente de la canalización, si procede. Para obtener más información, [**vea IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



