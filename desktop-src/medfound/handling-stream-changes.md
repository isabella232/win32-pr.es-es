---
description: En este tema se describe cómo una Media Foundation transformación (MFT) debe controlar los cambios de formato durante el streaming.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Control de cambios de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e238073bf518bc875b7b2d536c758eab48c8502278aae6780999c7616430337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974434"
---
# <a name="handling-stream-changes"></a>Control de cambios de flujo

En este tema se describe cómo una Media Foundation transformación (MFT) debe controlar los cambios de formato durante el streaming.

> [!IMPORTANT]
>
> Este tema no se aplica a los codificadores. Los codificadores no deben propagar los cambios de formato como se describe en este tema. Los codificadores solo deben aceptar un tipo de entrada que coincida con el tipo de salida configurado actualmente.

 

## <a name="overview-of-format-changes"></a>Introducción a los cambios de formato

Por lo general, hay dos razones por las que un formato puede cambiar durante el streaming.

-   El cliente puede cambiar a una secuencia con un nuevo formato. Por ejemplo, en la televisión digital, esto puede ocurrir debido a un cambio de canal.
-   En algunos formatos de vídeo, como H.264, la secuencia de bits puede indicar un cambio de formato. Estos cambios pueden incluir cambios en la dominación de campo, la resolución de vídeo o la relación de aspecto de píxeles.

Si cambia el tipo de codificación, es posible que el cliente tenga que quitar el MFT de la canalización y reemplazarlo por otro MFT. (Por ejemplo, es posible que el cliente tenga que intercambiar en un nuevo descodificador). En este tema no se trata esa situación. En este tema solo se trata el caso en el que el MFT actual puede controlar el nuevo formato.

Si cambia el formato, MFT podría requerir un nuevo tipo de entrada, un nuevo tipo de salida o ambos.

-   El cliente inicia los cambios en el tipo de entrada. Un MFT nunca cambia su propio tipo de entrada.
-   El MFT inicia los cambios en el tipo de salida. El MFT indica que requiere un nuevo tipo de salida y el cliente negocia el nuevo tipo de salida con el MFT.

Por lo tanto, son posibles tres casos distintos:

-   El cliente establece un nuevo tipo de entrada. El MFT consume el nuevo formato, sin cambios en su tipo de salida.
-   El cliente establece un nuevo tipo de entrada y esto desencadena un cambio en el tipo de salida.
-   El tipo de entrada no cambia, pero MFT detecta un cambio de formato en la secuencia de bits, que requiere un nuevo tipo de salida.

## <a name="implementing-format-changes"></a>Implementar cambios de formato

En el resto de este tema se describe cómo el cliente debe procesar un cambio de formato y cómo implementar cambios de formato en un MFT.

### <a name="output-type"></a>Tipo de salida

Cualquier MFT puede iniciar un cambio en su tipo de salida, como se muestra a continuación:

1.  El cliente llama [**a IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). El MFT responde de la siguiente manera:
    1.  El MFT no genera un ejemplo de salida en [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  MFT establece la marca **MFT \_ OUTPUT DATA BUFFER FORMAT \_ \_ \_ \_ CHANGE** en el **miembro dwStatus** de la estructura [**DATA BUFFER de salida \_ \_ \_ de MFT.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer)
    3.  El [**método ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) devuelve el código de error **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE**.
2.  El cliente llama [**a IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Este método devuelve un conjunto actualizado de tipos de salida.
3.  El cliente llama [**a SetOutputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) establecer un nuevo tipo de salida.
4.  El cliente reanuda la llamada [**a ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

### <a name="input-type"></a>Tipo de entrada

El cliente inicia los cambios en el tipo de entrada, nunca mediante el MFT. Si cambia el tipo de entrada, podría desencadenar un cambio en el tipo de salida.

La secuencia exacta de eventos depende del valor del atributo [**\_ MFT SUPPORT \_ DYNAMIC FORMAT \_ \_ CHANGE.**](mft-support-dynamic-format-change-attribute.md)



| Value     | Descripción                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Antes de que el cliente establece un nuevo tipo de entrada, debe purgar el MFT. |
| **TRUE**  | El cliente puede establecer un nuevo tipo de entrada sin purgar el MFT.   |



 

Un MFT expone este atributo a través de [**su método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) El valor predeterminado de este atributo es **FALSE**; si el MFT no establece el atributo , trate el valor como **FALSE.**

**MFT \_ SUPPORT DYNAMIC FORMAT CHANGE es \_ \_ \_ FALSE**

1.  El cliente envía el mensaje [**DE PURGA DEL \_ \_ COMANDO \_ MFT MESSAGE.**](mft-message-command-drain.md)
2.  El cliente purga el MFT mediante una llamada [**a MFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) hasta que **ProcessOutput** devuelve **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT**.
3.  El cliente llama [**a IMFTransform::SetInputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) establecer el nuevo tipo de entrada.
4.  El MFT valida el tipo de entrada. Si el tipo no es válido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) devuelve **MF E \_ \_ INVALIDMEDIATYPE** u otro código de error. De lo contrario, **SetInputType** devuelve S \_ OK.
5.  Suponiendo que el tipo de entrada es válido, MFT evalúa si el tipo de salida también cambia. Si no es así, el streaming continúa y no se requiere ninguna otra acción.
6.  Si cambia el tipo de salida:
    1.  MFT invalida su tipo de medio de salida actual y actualiza la lista de tipos de medios de salida disponibles.
    2.  La siguiente llamada a [**ProcessOutput devuelve**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE**, como se describe en la sección anterior.
    3.  El cliente llama [**a IMFTransform::GetOutputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) obtener la lista actualizada de tipos de salida.
    4.  El cliente llama [**a SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)

**MFT \_ SUPPORT \_ DYNAMIC \_ FORMAT \_ CHANGE is TRUE**

1.  El cliente llama [**a IMFTransform::SetInputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) establecer el nuevo tipo de entrada.
2.  El MFT valida el tipo de entrada. Si el tipo no es válido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) devuelve **MF E \_ \_ INVALIDMEDIATYPE** u otro código de error. De lo contrario, **SetInputType** devuelve S \_ OK.
3.  Suponiendo que el tipo de entrada es válido, MFT evalúa si el tipo de salida también cambia. Si no es así, el streaming continúa y no se requiere ninguna otra acción.
4.  Antes de que cambie el tipo de salida, MFT debe procesar los ejemplos de entrada almacenados en caché, como se muestra a continuación:
    1.  MFT no invalida su tipo de salida actual.
    2.  El MFT genera tanta salida como sea posible a partir de los ejemplos de entrada almacenados en caché.
    3.  Es opcional si MFT acepta nuevos ejemplos de entrada mientras procesa los ejemplos almacenados en caché. Si es así, los nuevos ejemplos de entrada usarán el nuevo formato de entrada, por lo que MFT debe realizar un seguimiento del punto en el que cambió el formato.
5.  Después de que el MFT procese todos los ejemplos que recibió antes de que cambiara el tipo de entrada, [**EL VALOR DE LA SALIDA DE LA TRANSFORMACIÓN DE MFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) devuelve **MF E TRANSFORM STREAM \_ \_ \_ \_ CHANGE**.
6.  MFT invalida su tipo de salida actual y actualiza la lista de tipos de medios de salida disponibles.
7.  El cliente negocia el nuevo tipo de salida, como se ha descrito anteriormente.

[Las MTA asincrónicas](asynchronous-mfts.md) deben devolver el valor **TRUE** para el [**atributo \_ MFT SUPPORT \_ DYNAMIC FORMAT \_ \_ CHANGE.**](mft-support-dynamic-format-change-attribute.md) Cuando se usa un MFT asincrónico, el cliente puede suponer que el atributo **\_ MFT SUPPORT \_ DYNAMIC FORMAT \_ \_ CHANGE** está establecido en **TRUE.**

Cuando [**MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) es **TRUE,** la diferencia principal es que el cliente no es necesario purgar el MFT antes de establecer un nuevo tipo de entrada. Como resultado, el tipo de entrada puede cambiar mientras MFT se mantiene en los ejemplos de entrada. Es importante que el MFT no se limite a quitar estos ejemplos. Además, el tipo de salida no puede cambiar hasta que MFT procesa todos sus datos almacenados en caché.

El párrafo anterior se aplica especialmente a los descodificadores de vídeo, que pueden recibir fotogramas codificados entre sí fuera del orden temporal y, por tanto, necesitan almacenarlos en caché. Si un MFT no almacena en caché ejemplos de entrada, purgar es esencialmente una operación no op. En ese caso, MFT puede establecer [**MFT \_ SUPPORT DYNAMIC \_ FORMAT \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) en **FALSE** (o dejar el atributo sin establecer).

Además, tenga en cuenta que se espera que cada MFT controle los cambios de formato correctamente después de purgar. El [**atributo \_ MFT SUPPORT DYNAMIC FORMAT \_ \_ \_ CHANGE**](mft-support-dynamic-format-change-attribute.md) indica si MFT admite cambios de formato sin purgar.

## <a name="change-in-interlace-mode"></a>Cambio en el modo de intercalación

Los cambios en el modo de entrelazado de vídeo son un caso especial, ya que no invalidan el tipo de medio actual. En su lugar, el modo de intercalación se especifica para cada fotograma de vídeo estableciendo atributos en el ejemplo multimedia. Un MFT de vídeo debe comprobar la presencia de estas marcas en cada ejemplo de entrada.

El modo de intercalación puede cambiar cuando la dominación del campo cambia de campo superior a inferior, o cuando el vídeo cambia entre imágenes progresivas e entrelazadas.

Para obtener más información, [vea Interlace Flags on Samples](video-interlacing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 



