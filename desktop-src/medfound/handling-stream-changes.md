---
description: En este tema se describe cómo una transformación de Media Foundation (MFT) debe controlar los cambios de formato durante el streaming.
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: Control de los cambios de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275773"
---
# <a name="handling-stream-changes"></a>Control de los cambios de flujo

En este tema se describe cómo una transformación de Media Foundation (MFT) debe controlar los cambios de formato durante el streaming.

> [!IMPORTANT]
>
> Este tema no se aplica a los codificadores. Los codificadores no deben propagar los cambios de formato tal y como se describe en este tema. Los codificadores solo deben aceptar un tipo de entrada que coincida con el tipo de salida configurado actualmente.

 

## <a name="overview-of-format-changes"></a>Información general de los cambios de formato

Por lo general, hay dos razones por las que un formato puede cambiar durante el streaming.

-   El cliente puede cambiar a un flujo con un nuevo formato. Por ejemplo, en televisión digital, esto puede ocurrir debido a un cambio de canal.
-   En algunos formatos de vídeo, como H. 264, el fragmentada puede indicar un cambio de formato. Estos cambios pueden incluir cambios en la superposición de los campos, la resolución de vídeo o la relación de aspecto de píxeles.

Si el tipo de codificación cambia, es posible que el cliente tenga que quitar el MFT de la canalización y reemplazarlo por otro MFT. (Por ejemplo, es posible que el cliente necesite intercambiarse en un nuevo descodificador). En este tema no se trata esta situación. En este tema solo se trata el caso en el que la MFT actual puede controlar el nuevo formato.

Si el formato cambia, el MFT podría requerir un nuevo tipo de entrada, un nuevo tipo de salida o ambos.

-   El cliente inicia los cambios en el tipo de entrada. Una MFT nunca cambia su propio tipo de entrada.
-   La MFT inicia los cambios en el tipo de salida. La MFT indica que requiere un nuevo tipo de salida y el cliente negocia el nuevo tipo de salida con la MFT.

Por lo tanto, son posibles tres casos distintos:

-   El cliente establece un nuevo tipo de entrada. La MFT usa el nuevo formato, sin ningún cambio en su tipo de salida.
-   El cliente establece un nuevo tipo de entrada y desencadena un cambio en el tipo de salida.
-   El tipo de entrada no cambia, pero el MFT detecta un cambio de formato en fragmentada, lo que requiere un nuevo tipo de salida.

## <a name="implementing-format-changes"></a>Implementar cambios de formato

En el resto de este tema se describe cómo el cliente debe procesar un cambio de formato y cómo implementar los cambios de formato en una MFT.

### <a name="output-type"></a>Tipo de salida

Cualquier MFT puede iniciar un cambio en su tipo de salida, como se indica a continuación:

1.  El cliente llama a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). La MFT responde de la siguiente manera:
    1.  MFT no genera un ejemplo de salida en [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
    2.  MFT establece la marca **de \_ \_ cambio del \_ \_ formato \_ de búfer de datos de salida de MFT** en el miembro **dwStatus** de la estructura de búfer de [**\_ \_ datos \_ de salida MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) .
    3.  El método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) devuelve el código de error **MF \_ E transformar el \_ \_ \_ cambio de flujo**.
2.  El cliente llama a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Este método devuelve un conjunto actualizado de tipos de salida.
3.  El cliente llama a [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer un nuevo tipo de salida.
4.  El cliente reanuda la llamada a [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

### <a name="input-type"></a>Tipo de entrada

El cliente inicia los cambios en el tipo de entrada, nunca el MFT. Si el tipo de entrada cambia, podría desencadenar un cambio en el tipo de salida.

La secuencia exacta de eventos depende del valor del atributo de [**\_ cambio de \_ \_ formato dinámico \_ compatible con MFT**](mft-support-dynamic-format-change-attribute.md) .



| Value     | Descripción                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | Antes de que el cliente establezca un nuevo tipo de entrada, debe purgar la MFT. |
| **TRUE**  | El cliente puede establecer un nuevo tipo de entrada sin agotar la MFT.   |



 

Un MFT expone este atributo a través de su método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . El valor predeterminado de este atributo es **false**; Si MFT no establece el atributo, trate el valor como **false**.

**La \_ compatibilidad con el \_ cambio de formato dinámico de MFT \_ \_ es falsa**

1.  El cliente envía el mensaje de [**agotamiento del comando del mensaje de MFT \_ \_ \_**](mft-message-command-drain.md) .
2.  El cliente purga la MFT mediante una llamada a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) hasta que **ProcessOutput** devuelve la **\_ transformación MF E \_ \_ necesita \_ más \_ entrada**.
3.  El cliente llama a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el nuevo tipo de entrada.
4.  La MFT valida el tipo de entrada. Si el tipo no es válido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) devuelve **MF \_ E \_ INVALIDMEDIATYPE** u otro código de error. De lo contrario, **SetInputType** devuelve S \_ OK.
5.  Suponiendo que el tipo de entrada es válido, el MFT evalúa si el tipo de salida también cambia. En caso contrario, continúa la transmisión por secuencias y no es necesario realizar ninguna otra acción.
6.  Si el tipo de salida cambia:
    1.  La MFT invalida su tipo de medio de salida actual y actualiza la lista de tipos de medios de salida disponibles.
    2.  La siguiente llamada a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) devuelve **el \_ \_ cambio de \_ secuencia \_ de transformación MF E**, como se describe en la sección anterior.
    3.  El cliente llama a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener la lista actualizada de tipos de salida.
    4.  El cliente llama a [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

**La \_ compatibilidad con el \_ cambio de formato dinámico de MFT \_ \_ es true**

1.  El cliente llama a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el nuevo tipo de entrada.
2.  La MFT valida el tipo de entrada. Si el tipo no es válido, [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) devuelve **MF \_ E \_ INVALIDMEDIATYPE** u otro código de error. De lo contrario, **SetInputType** devuelve S \_ OK.
3.  Suponiendo que el tipo de entrada es válido, el MFT evalúa si el tipo de salida también cambia. En caso contrario, continúa la transmisión por secuencias y no es necesario realizar ninguna otra acción.
4.  Antes de que el tipo de salida cambie, el MFT debe procesar cualquier ejemplo de entrada en caché, como se indica a continuación:
    1.  MFT no invalida su tipo de salida actual.
    2.  La MFT genera tantas salidas como pueda de los ejemplos de entrada almacenados en caché.
    3.  Es opcional si el MFT acepta nuevos ejemplos de entrada mientras procesa los ejemplos almacenados en caché. Si es así, los nuevos ejemplos de entrada usarán el nuevo formato de entrada, por lo que la MFT debe realizar un seguimiento del punto cuando el formato cambie.
5.  Una vez que el MFT procesa todos los ejemplos que recibió antes de que se cambiara el tipo de entrada, [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) devuelve el **\_ cambio de flujo de \_ transformación \_ \_ MF E**.
6.  La MFT invalida su tipo de salida actual y actualiza la lista de tipos de medios de salida disponibles.
7.  El cliente negocia el nuevo tipo de salida, tal y como se ha descrito anteriormente.

Los [MFTs asincrónicos](asynchronous-mfts.md) deben devolver el valor **true** para el atributo de [**\_ \_ \_ \_ cambio de formato dinámico de compatibilidad con MFT**](mft-support-dynamic-format-change-attribute.md) . Cuando se usa una MFT asincrónica, el cliente puede suponer que el atributo **\_ compatibilidad con el \_ \_ \_ cambio de formato dinámico de MFT** está establecido en **true**.

Cuando [**la \_ compatibilidad con el \_ \_ \_ cambio de formato dinámico de MFT**](mft-support-dynamic-format-change-attribute.md) es **true**, la principal diferencia es que el cliente no necesita purgar la MFT antes de establecer un nuevo tipo de entrada. Como resultado, el tipo de entrada puede cambiar mientras la MFT contiene los ejemplos de entrada. Es importante que la MFT no quite simplemente estos ejemplos. Además, el tipo de salida no puede cambiar hasta que la MFT procese todos los datos almacenados en caché.

El párrafo anterior se aplica especialmente a los descodificadores de vídeo, que pueden recibir fotogramas intercodificados fuera del orden temporal y, por tanto, deben almacenarse en caché. Si una MFT no almacena en caché los ejemplos de entrada, la purga es esencialmente una operación no operativa. En ese caso, el MFT puede establecer [**el \_ \_ cambio de \_ formato \_ dinámico de compatibilidad con MFT**](mft-support-dynamic-format-change-attribute.md) en **false** (o dejar el atributo sin definir).

Además, tenga en cuenta que se espera que cada MFT controle los cambios de formato correctamente tras su purga. El atributo de [**\_ \_ \_ \_ cambio de formato dinámico de MFT**](mft-support-dynamic-format-change-attribute.md) indica si la MFT admite cambios de formato sin purgar.

## <a name="change-in-interlace-mode"></a>Cambiar en modo entrelazado

Los cambios en el modo de entrelazado de vídeo son un caso especial, ya que no invalidan el tipo de medio actual. En su lugar, se especifica el modo entrelazado para cada fotograma de vídeo mediante el establecimiento de atributos en el ejemplo multimedia. Un MFT de vídeo debe comprobar cada ejemplo de entrada para la presencia de estas marcas.

El modo entrelazado puede cambiar cuando el campo dominador cambia de campo superior a campo inferior, o cuando el vídeo cambia entre imágenes progresivas e entrelazadas.

Para obtener más información, vea el apartado [sobre marcas de entrelazado en ejemplos](video-interlacing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 



