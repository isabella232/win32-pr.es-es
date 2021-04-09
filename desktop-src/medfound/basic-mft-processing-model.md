---
description: En este tema se describe cómo un cliente utiliza una transformación de Media Foundation (MFT) para procesar los datos. El cliente es todo lo que llama directamente a los métodos de la MFT. Puede tratarse de la aplicación o la Media Foundation canalización.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Modelo básico de procesamiento de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca54df6d9765aaf54456c3d9dc4461a82a93d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080333"
---
# <a name="basic-mft-processing-model"></a>Modelo básico de procesamiento de MFT

En este tema se describe cómo un cliente utiliza una transformación de Media Foundation (MFT) para procesar los datos. El *cliente* es todo lo que llama directamente a los métodos de la MFT. Puede tratarse de la aplicación o la Media Foundation canalización.

Lea este tema si está:

-   Escritura de una aplicación que realiza llamadas directas a uno o varios MFTs.
-   Escribir una MFT personalizada y desea comprender el comportamiento esperado de una MFT.

En este tema se describe un modelo de procesamiento *sincrónico* . En este modelo, todos los métodos de procesamiento de datos se bloquean hasta que se completan. MFTs también puede admitir un modelo *asincrónico* , que se describe en el tema [MFTs asincrónico](asynchronous-mfts.md).

-   [Modelo de procesamiento básico](#basic-processing-model)
    -   [Crear la MFT](#create-the-mft)
    -   [Obtener los identificadores de secuencia](#get-stream-identifiers)
    -   [Establecer tipos de medios](#set-media-types)
    -   [Obtener los requisitos de búfer](#get-buffer-requirements)
    -   [Procesar datos](#process-data)
-   [Extensiones para el modelo básico](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [Vaciar un MFT](#flushing-an-mft)
-   [Purga de un MFT](#draining-an-mft)
-   [Atributos de ejemplo](#sample-attributes)
-   [Discontinuidades](#discontinuities)
-   [Cambios en el formato dinámico](#dynamic-format-changes)
-   [Eventos de secuencia](#stream-events)
-   [Temas relacionados](#related-topics)

## <a name="basic-processing-model"></a>Modelo de procesamiento básico

### <a name="create-the-mft"></a>Crear la MFT

Hay varias maneras de crear una MFT:

-   Llame a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .
-   Llame a la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Si ya conoce el CLSID de MFT, simplemente llame a **CoCreateInstance**.

Algunos MFTs pueden proporcionar otras opciones, como una función de creación especializada.

### <a name="get-stream-identifiers"></a>Obtener los identificadores de secuencia

Una MFT tiene una o más *secuencias*. Los flujos de entrada reciben datos de entrada y los flujos de salida generan datos de salida. Las secuencias no se representan como objetos distintos. En su lugar, varios métodos de MFT toman los identificadores de secuencia como parámetros.

Algunos MFTs permiten al cliente agregar o quitar flujos de entrada. Durante el streaming, una MFT puede Agregar o quitar flujos de salida. (El cliente no puede Agregar o quitar flujos de salida).

1.  (Opcional). Llame a [**IMFTransform:: GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) para obtener el número mínimo y máximo de secuencias que puede admitir la MFT. Si los valores mínimo y máximo son los mismos, el MFT tiene un número fijo de secuencias.
2.  Llame a [**IMFTransform:: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) para obtener el número inicial de secuencias.
3.  Llame a [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) para obtener los identificadores de flujo. Si este método devuelve E \_ NOTIMPL, significa que la MFT tiene un número fijo de secuencias, y los identificadores de secuencia son consecutivos a partir de cero.
4.  (Opcional). Si MFT no tiene un número fijo de flujos, llame a [**IMFTransform:: AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) para agregar más flujos de entrada o [**IMFTransform::D eleteinputstream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) para quitar flujos de entrada. (No se pueden agregar o quitar secuencias de salida).

### <a name="set-media-types"></a>Establecer tipos de medios

Para que un MFT pueda procesar los datos, el cliente debe establecer un tipo de medio para cada una de las secuencias de la MFT. Una MFT puede requerir que el cliente establezca los tipos de entrada antes de establecer los tipos de salida, o podría requerir el orden opuesto (los tipos de salida primero). Algunos MFTs no tienen un requisito en el orden.

Una MFT puede proporcionar una lista de los tipos de medios preferidos para un flujo. Además, MFTs puede indicar los formatos generales que admiten agregando esta información al registro.

Para establecer los tipos de medios, haga lo siguiente:

1.  (Opcional). Para cada flujo de entrada, llame a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obtener la lista de tipos preferidos para esa secuencia.
    -   Si este método devuelve \_ \_ el tipo de transformación MF E \_ \_ no \_ establecido, debe establecer primero los tipos de salida; vaya al paso 3.
    -   Si el método devuelve E \_ NOTIMPL, la MFT no tiene una lista de tipos de entrada preferidos. vaya al paso 2.
2.  Para cada flujo de entrada, llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el tipo de entrada. Puede usar un tipo de medio del paso 1, o un tipo que describa los datos de entrada. Si algún flujo devuelve el \_ \_ tipo de transformación MF E \_ \_ no \_ establecido, vaya al paso 3.
3.  (Opcional). Para cada flujo de salida, llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener una lista de los tipos preferidos para esa secuencia.
    -   Si este método devuelve \_ \_ el tipo de transformación MF E \_ \_ no \_ establecido, debe establecer los tipos de entrada en primer lugar; vuelva al paso 1.
    -   Si algún flujo devuelve E \_ NOTIMPL, la MFT no tiene una lista de tipos de salida preferidos. vaya al paso 4.
4.  Para cada flujo de salida, llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de salida. Puede usar un tipo de medio del paso 3 o un tipo que describa el formato de salida necesario.
5.  Si algún flujo de entrada no tiene un tipo de medio, vuelva al paso 1.

### <a name="get-buffer-requirements"></a>Obtener los requisitos de búfer

Después de que el cliente establezca los tipos de medios, debe obtener los requisitos de búfer para cada flujo:

-   Para cada flujo de entrada, llame a [**IMFTransform:: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Para cada flujo de salida, llame a [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Procesar datos

Una MFT está diseñada para ser un equipo de estado de confianza. No vuelve a realizar ninguna llamada al cliente.

1.  Llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con [**el \_ mensaje \_ de \_ Inicio Notify Begin \_ streaming**](mft-message-notify-begin-streaming.md) . Este mensaje solicita a la MFT que asigne los recursos que necesita durante el streaming.
2.  Llame a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) en al menos un flujo de entrada para proporcionar un ejemplo de entrada a la MFT.
3.  (Opcional). Llame a [**IMFTransform:: GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) para consultar si el MFT puede generar un ejemplo de salida. Si el método devuelve S \_ correcto, compruebe el parámetro *pdwFlags* . Si *pdwFlags* contiene el **indicador \_ ejemplo de estado de salida de MFT \_ \_ \_ listo** , vaya al paso 4. Si *pdwFlags* es cero, vuelva al paso 2. Si el método devuelve E \_ NOTIMPL, vaya al paso 4.
4.  Llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener los datos de salida.
    -   Si el método devuelve **la \_ transformación MF E \_ \_ necesita \_ más \_** información, significa que la MFT requiere más datos de entrada. Vuelva al paso 2.
    -   Si el método devuelve **el \_ \_ cambio de \_ flujo \_ de transformación MF E**, significa que el número de flujos de salida ha cambiado o el formato de salida ha cambiado. Es posible que el cliente necesite consultar nuevos identificadores de secuencia o establecer nuevos tipos de medios. Para obtener más información, consulte la documentación de [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Si todavía hay datos de entrada para procesar, vaya al paso 2. Si la MFT ha consumido todos los datos de entrada disponibles, continúe en el paso 6.
6.  Llame a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con [**el \_ mensaje \_ de MFT notificación del \_ final \_ del mensaje de la \_ secuencia**](mft-message-notify-end-of-stream.md) .
7.  Llame a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de agotamiento del comando de mensaje de [**MFT \_ \_ \_**](mft-message-command-drain.md) .
8.  Llame a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener el resultado restante. Repita este paso hasta que el método devuelva la **\_ transformación MF E \_ \_ necesite \_ más \_ datos**. Este valor devuelto indica que toda la salida se ha purgado de la MFT. (No lo trate como una condición de error).

La secuencia que se describe aquí mantiene la menor cantidad posible de datos en la MFT. Después de cada llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), el cliente intenta obtener la salida. Pueden ser necesarios varios ejemplos de entrada para generar un ejemplo de salida, o un único ejemplo de entrada puede generar varios ejemplos de salida. El comportamiento óptimo para el cliente es extraer ejemplos de salida de la MFT hasta que la MFT requiera más entrada.

Sin embargo, el MFT debe ser capaz de controlar un orden diferente de llamadas a métodos por parte del cliente. Por ejemplo, el cliente podría simplemente alternar entre las llamadas a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). La MFT debe restringir la cantidad de entradas que obtiene al devolver **MF \_ E \_ NOTACCEPTING** de **ProcessInput** siempre que tenga una salida para generar.

El orden de las llamadas a métodos que se describen aquí no es la única secuencia válida de eventos. Por ejemplo, los pasos 3 y 4 suponen que el cliente se inicia con los tipos de entrada y, a continuación, prueba los tipos de salida. El cliente también puede invertir este orden e iniciar con los tipos de salida. En cualquier caso, si la MFT requiere el orden contrario, debe devolver el tipo de transformación MF \_ E \_ \_ \_ no \_ establecido.

El cliente puede llamar a métodos informativos, como [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) y [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo), en cualquier momento durante el streaming. El cliente también puede intentar cambiar los tipos de medios en cualquier momento. La MFT debe devolver un código de error si no se trata de una operación válida. En Resumen, MFTs debe asumir muy poco el orden de las operaciones, aparte de lo que se documenta en las propias llamadas.

En el diagrama siguiente se muestra un gráfico de flujo de los procedimientos descritos en este tema.

![diagrama de flujo que conduce de obtener identificadores de flujo mediante bucles que establecen tipos de entrada, obtienen entradas y procesan los resultados.](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Extensiones para el modelo básico

Opcionalmente, una MFT puede admitir algunas extensiones para el modelo básico de streaming.

-   Secuencias de lectura diferida. Si el método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve la marca de **\_ \_ \_ \_ lectura diferida del flujo de salida de MFT** para un flujo de salida, el cliente no tiene que recopilar datos de ese flujo de salida. La MFT continúa aceptando la entrada y, en algún momento, la MFT descartará los datos de salida de la secuencia. Si todos los flujos de salida tienen esta marca, la MFT nunca no aceptará la entrada. Un ejemplo podría ser una transformación de visualización, donde el cliente obtiene la salida solo cuando tiene ciclos de CPU de reserva para dibujar la visualización.
-   Flujos descartables. Si el método [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve la marca de **\_ salida \_ \_ descartable** de la MFT para un flujo de salida, el cliente puede solicitar a la MFT que descarte la salida, pero la MFT no descartará ningún resultado a menos que se solicite. Cuando el MFT alcanza su búfer de entrada máximo, el cliente debe recopilar algunos datos de salida o solicitar a la MFT que descarte la salida.
-   Secuencias opcionales. Si el método [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve la **marca \_ \_ \_ opcional del flujo de salida de MFT** para un flujo de salida, o el método [**IMFTransform:: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) devuelve la marca **\_ \_ \_ opcional del flujo de entrada de MFT** para un flujo de entrada, esa secuencia es opcional. El cliente no tiene que establecer un tipo de medio en la secuencia. Si el cliente no establece el tipo, se anula la selección de la secuencia. Un flujo de salida no seleccionado no produce ejemplos y el cliente no proporciona un búfer para la secuencia cuando llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un flujo de entrada anulada no acepta datos de entrada. Una MFT puede marcar todos los flujos de entrada y salida como opcionales. Sin embargo, se espera que se seleccione al menos una entrada y una salida para que el MFT funcione.
-   Procesamiento asincrónico. El modelo de procesamiento asincrónico se presentó en Windows 7. Se describe en el tema [MFTs asincrónico](asynchronous-mfts.md).

## <a name="imf2dbuffer"></a>IMF2DBuffer

Si una MFT procesa datos de vídeo sin comprimir, debe usar la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) para manipular los búferes de ejemplo. Para obtener esta interfaz, consulte la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) en cualquier búfer de entrada o salida. Si no se usa esta interfaz cuando está disponible, pueden producirse copias de búfer adicionales. Para hacer un uso correcto de esta interfaz, la transformación no debe bloquear el búfer mediante la interfaz **IMFMediaBuffer** cuando **IMF2DBuffer** esté disponible.

Para obtener más información acerca del procesamiento de datos de vídeo, consulte [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).

## <a name="flushing-an-mft"></a>Vaciar un MFT

*Vaciar* una MFT hace que la MFT descarte todos los datos de entrada. Esto puede producir una interrupción en el flujo de salida. Un cliente normalmente vaciaría una MFT antes de buscar un nuevo punto en el flujo de entrada o cambiar a un nuevo flujo de entrada, cuando el cliente no se preocupa de perder datos.

Para vaciar una MFT, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de [**\_ \_ \_ vaciado del comando del mensaje de MFT**](mft-message-command-flush.md) .

## <a name="draining-an-mft"></a>Purga de un MFT

La *purga* de una MFT hace que la MFT genere tantas salidas como sea posible desde cualquier dato de entrada que ya se haya enviado. Si el MFT no puede generar un ejemplo de salida completo a partir de la entrada disponible, quitará los datos de entrada. Un cliente normalmente agotaría un MFT cuando llegó al final de la secuencia de origen, o inmediatamente antes de un cambio de formato en el flujo de origen. Para purgar un MFT, haga lo siguiente:

1.  Llame a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de agotamiento del comando de mensaje de [**MFT \_ \_ \_**](mft-message-command-drain.md) . Este mensaje notifica a la MFT que debe proporcionar tantos datos de salida como los datos de entrada que ya se han enviado.
2.  Llame a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener los datos de salida, hasta que el método devuelva la **\_ transformación MF E \_ \_ necesite \_ más \_ entrada**.

Mientras se está purgando la MFT, no aceptará más entradas.

## <a name="sample-attributes"></a>Atributos de ejemplo

Los ejemplos de entrada pueden tener atributos que se deben copiar en los ejemplos de salida correspondientes.

-   Si MFT devuelve **Variant \_ true** para la propiedad [**MFPKEY \_ exattribute \_ Supported**](mfpkey-exattribute-supported-property.md) , el MFT debe copiar los atributos.
-   Si la propiedad [**MFPKEY \_ exattribute \_ Supported**](mfpkey-exattribute-supported-property.md) es **Variant \_ false** o no está establecida, el cliente debe copiar los atributos.

En el caso de una MFT con una entrada y una salida, puede usar la siguiente regla general:

-   Si cada ejemplo de entrada produce exactamente un ejemplo de salida, puede permitir que el cliente copie los atributos. Deje la propiedad [**MFPKEY \_ \_ exsupported exattribute**](mfpkey-exattribute-supported-property.md) .
-   Si no hay una correspondencia uno a uno entre los ejemplos de entrada y los ejemplos de salida, el MFT debe determinar los atributos correctos para los ejemplos de salida. Establezca la propiedad [**MFPKEY \_ exattribute \_ Supported**](mfpkey-exattribute-supported-property.md) en **Variant \_ true**.

## <a name="discontinuities"></a>Discontinuidades

Una discontinuidad es una interrupción en una secuencia de audio o de vídeo. Las discontinuidades pueden deberse a la pérdida de paquetes en una conexión de red, a datos de archivos dañados, a un cambio de un flujo de origen a otro o a un amplio abanico de otras causas. Las discontinuidades se señalizan estableciendo el [**atributo \_ discontinuidad de MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) en el primer ejemplo después de la discontinuidad. No es posible señalar una discontinuidad en medio de un ejemplo. Por lo tanto, los datos descontinuos se deben enviar en ejemplos independientes.

Algunas transformaciones, especialmente las que controlan datos sin comprimir, como efectos de audio y vídeo, deben omitir las discontinuidades al procesar los datos de entrada. Por lo general, estos MFTs están diseñados para administrar datos continuos y deben tratar los datos que reciben como continuos, incluso después de una discontinuidad.

Si un MFT omite una discontinuidad en los datos de entrada, todavía debe establecer la marca de discontinuidad en el ejemplo de salida, si el ejemplo de salida tiene la misma marca de tiempo que la muestra de entrada. Sin embargo, si el ejemplo de salida tiene una marca de tiempo diferente, la MFT no debe propagar la discontinuidad. (Este sería el caso en algunos remuestreadores de audio, por ejemplo). Una discontinuidad en el lugar equivocado de la secuencia es peor que ninguna discontinuidad.

La mayoría de los descodificadores no pueden omitir las discontinuidades, ya que una discontinuidad afecta a la interpretación de la siguiente muestra. Cualquier tecnología de codificación que use la compresión entre fotogramas, como MPEG-2, entra en esta categoría. Algunos esquemas de codificación solo usan la compresión intra-Frame, como DV y MJPEG. Estos descodificadores pueden omitir de forma segura las discontinuidades.

Las transformaciones que responden a las discontinuidades normalmente deben generar la mayoría de los datos antes de la discontinuidad que puedan y descartar el resto. El ejemplo de entrada con la marca de discontinuidad debe procesarse como si fuera la primera muestra de la secuencia. (Este comportamiento coincide con el especificado en el mensaje de [**agotamiento del comando del mensaje de MFT \_ \_ \_**](mft-message-command-drain.md) ). Sin embargo, los detalles exactos dependerán del formato del medio.

Si un descodificador no realiza ninguna acción para mitigar una discontinuidad, debe copiar la marca de discontinuidad en los datos de salida. Los demultiplexadores y otros MFTs que funcionan completamente con datos comprimidos deben copiar cualquier interrupción en sus flujos de salida. De lo contrario, es posible que los componentes de nivel inferior no puedan descodificar los datos comprimidos correctamente. En general, casi siempre es correcto para pasar las discontinuidad de nivel inferior, a menos que la MFT contenga código explícito para suavizar las discontinuidades.

## <a name="dynamic-format-changes"></a>Cambios en el formato dinámico

Los formatos pueden cambiar durante el streaming. Por ejemplo, la relación de aspecto puede cambiar en medio de una secuencia de vídeo.

Para obtener más información sobre cómo se administran los cambios de flujo mediante un MFT, consulte [control de los cambios de flujo](handling-stream-changes.md).

## <a name="stream-events"></a>Eventos de secuencia

Para enviar un evento a un MFT, llame a [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Si el método devuelve **MF \_ S \_ Transform \_ \_ no \_ Propagate \_ Event**, MFT devolverá el evento al llamador en una llamada subsiguiente a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Si el método devuelve cualquier otro valor **HRESULT** , el MFT no devolverá el evento al cliente en **ProcessOutput**. En ese caso, el cliente es responsable de propagar el evento de nivel inferior al siguiente componente de la canalización, si procede. Para obtener más información, vea [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



