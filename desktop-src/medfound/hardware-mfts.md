---
description: En este tema se describe cómo escribir una transformación de Media Foundation (MFT) que actúa como proxy para un codificador de hardware, un descodificador o un procesador de señal digital (DSP).
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: MFTs de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275772"
---
# <a name="hardware-mfts"></a>MFTs de hardware

> [!Note]  
> Este tema se aplica a Windows 7 o posterior.

 

En este tema se describe cómo escribir una transformación de Media Foundation (MFT) que actúa como proxy para un codificador de hardware, un descodificador o un procesador de señal digital (DSP).

> [!IMPORTANT]
> Si un códec de hardware usa el controlador de la clase multimedia AVStream, no necesita un MFT personalizado. Media Foundation proporciona un proxy AVStream para este propósito. La información de este tema solo se aplica en el caso especial en el que el códec de hardware no usa AVStream. Para obtener más información, consulte [compatibilidad con códecs de hardware en AVStream](https://msdn.microsoft.com/library/dd568169.aspx).

 

Este tema contiene las siguientes secciones:

-   [Introducción](#introduction)
-   [Atributos de MFT de hardware](#hardware-mft-attributes)
-   [Secuencia de protocolo de enlace de hardware](#hardware-handshake-sequence)
-   [Procesamiento de datos](#data-processing)
-   [Descodificador/codificador emparejados](#paired-decoderencoder)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Cualquier códec de hardware que no esté basado en AVStream debe proporcionar su propio MFT para que actúe como proxy para el controlador. Un códec de hardware puede incorporar varios bloques funcionales distintos:

-   Codificador
-   Descodificador
-   Escala de fotogramas/conversión de formato

Cada una de estas funciones debe administrarse mediante un MFT independiente. Un MFT de hardware nunca debe actuar como "transcodificador" multipropósito. En su lugar, coloque las funciones de codificación en una MFT del codificador y descodifique las funciones en un MFT del descodificador. Si el hardware ofrece conversiones de formato y escalado de fotogramas, coloque esas funciones en un procesador de vídeo independiente registrado en la categoría de **\_ \_ \_ procesador de vídeo categoría de MFT** . Si el hardware no admite la escala de fotogramas o la conversión de formato, Media Foundation proporciona un procesador de vídeo de software.

Los MFTs de hardware tienen los siguientes requisitos generales:

-   El MFTs de hardware debe usar el nuevo modelo de procesamiento asincrónico, como se describe en [MFTs asincrónico](asynchronous-mfts.md).
-   Los MFTs de hardware deben admitir los cambios de formato dinámico, tal y como se describe en [cambios de formato dinámico](basic-mft-processing-model.md).

## <a name="hardware-mft-attributes"></a>Atributos de MFT de hardware

Un MFT de hardware debe implementar los métodos siguientes relacionados con los atributos:

-   [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes): devuelve un almacén de atributos para los atributos globales de MFT.
-   [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes): devuelve un almacén de atributos para un flujo de entrada.
-   [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes): devuelve un almacén de atributos para un flujo de salida.

Cuando se crea por primera vez la MFT, debe establecer los atributos siguientes en su propio almacén de atributos global (es decir, el almacén de atributos devuelto por [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)):



| Atributo                                                                                    | Descripción                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ transformación \_ asincrónica](mf-transform-async.md)                                               | Debe establecerse en **true**. Indica que MFT realiza el procesamiento asincrónico.                                                                                                      |
| [\_Atributo de \_ \_ dirección URL de hardware enum de MFT \_](mft-enum-hardware-url-attribute.md)                   | Contiene el vínculo simbólico para el dispositivo de hardware.<br/> El cargador de topología usa la presencia de este atributo para probar si una MFT representa un dispositivo de hardware.<br/> |
| [**la MFT \_ admite el \_ \_ cambio de formato dinámico \_**](mft-support-dynamic-format-change-attribute.md) | Debe establecerse en **true**. Indica que la MFT admite cambios de formato dinámico.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Secuencia de protocolo de enlace de hardware

Si dos MFTs representan el mismo dispositivo físico, pueden intercambiar datos dentro del hardware, por ejemplo, a través de un bus de hardware. No es necesario copiar los datos en la memoria del sistema y, a continuación, volver al dispositivo.

En el diagrama siguiente, el MFTs con la etiqueta "A" y "B" representa bloques funcionales dentro del mismo hardware. Por ejemplo, en un escenario de transcodificación, "A" podría representar un descodificador de hardware y "B" podría representar un codificador de hardware. El flujo de datos entre "A" y "B" se produce en el hardware. La MFT con la etiqueta "C" es un MFT de software. El flujo de datos de "B" a "C" utiliza la memoria del sistema.

![diagrama que muestra cuadros con la etiqueta a a c y un códec de hardware: a apunta a b y el códec, el códec apunta a b y b apunta a c](images/proxy-mft.png)

Para establecer una conexión de hardware, los dos MFTs de hardware deben usar un canal de comunicación privado. Esta conexión se establece durante la negociación del formato, antes de que se establezcan los tipos de medios y antes de la primera llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). El proceso de conexión funciona de la siguiente manera:

1.  El cargador de topología comprueba MFTs para comprobar la presencia del atributo [de \_ \_ atributo de \_ dirección \_ URL de hardware enum de MFT](mft-enum-hardware-url-attribute.md) . Tenga en cuenta que no examina el valor de este atributo.
2.  Si [el \_ \_ atributo de \_ dirección \_ URL de hardware de enumeración de MFT](mft-enum-hardware-url-attribute.md) está presente en ambos MFTs, el cargador de topología hace lo siguiente:
    1.  El cargador de topología llama a [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) en el MFT ascendente (a). Este método devuelve un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Permita que este puntero se dediga *pUpstream*.
    2.  El cargador de topología llama a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) en la MFT de nivel inferior (B). Esta llamada también devuelve un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Permita que este puntero se dediga *pDownstream*.
    3.  El cargador de topología establece el atributo de [ \_ \_ \_ atributo Stream conectado de MFT](mft-connected-stream-attribute.md) en *pDownstream* mediante una llamada a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). El valor del atributo es el puntero *pUpstream* .
    4.  El cargador de topología establece el [atributo MFT \_ conectado \_ a \_ HW \_ Stream](mft-connected-to-hw-stream.md) en **true** en *pDownstream* y *pUpstream*.
3.  En este punto, la MFT de bajada tiene un puntero al almacén de atributos de la MFT ascendente, tal como se muestra en el diagrama siguiente.

    ![diagrama con cada MFTs que apunta a su flujo, cada secuencia que apunta a su almacén y el almacén de entrada con una línea discontinua en el almacén de salida](images/proxy-mft2.png)

    > [!Note]  
    > Para mayor claridad, este diagrama muestra los flujos y los almacenes de atributos como objetos distintos, pero esto no es necesario para la implementación.

     

4.  La MFT de nivel inferior usa el puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer un canal de comunicación privado con el MFT ascendente. Dado que el canal es privado, la implementación define el mecanismo exacto. Por ejemplo, MFT podría consultar una interfaz COM privada.

Durante el paso 4, la MFT de bajada debe comprobar si los dos MFTs comparten el mismo dispositivo físico. Si no es así, deben revertirse al uso de la memoria del sistema para el transporte de datos. Esto permite que la MFT funcione correctamente con el software MFTs y otros dispositivos de hardware.

Si el protocolo de enlace se realiza correctamente y los dos MFTs comparten un canal de datos privado, no usan el modelo de procesamiento de datos estándar (descrito en la sección siguiente) en el punto de conexión. En concreto, la MFT de nivel inferior no envía eventos [METransformNeedInput](metransformneedinput.md) ; para obtener más información, consulte la sección siguiente de este tema.

## <a name="data-processing"></a>Procesamiento de datos

Cuando un MFT de hardware utiliza la memoria del sistema para el transporte de datos, el proceso funciona de la siguiente manera:

1.  Para solicitar más entradas, el MFT envía un evento [METransformNeedInput](metransformneedinput.md) .
2.  El evento [METransformNeedInput](metransformneedinput.md) hace que la canalización llame a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
3.  Cuando el MFT tiene datos de salida, el MFT envía un evento [METransformHaveOutput](metransformhaveoutput.md) .
4.  El evento [METransformHaveOutput](metransformhaveoutput.md) hace que la canalización llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Para obtener más información, consulte [MFTs asincrónico](asynchronous-mfts.md).

Sin embargo, si la MFT usa un canal de hardware, no envía estos eventos en el punto de conexión de hardware, ya que toda la transferencia de datos se realiza internamente en el hardware. Por lo tanto, la canalización no llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) o [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el punto de conexión.

Por ejemplo, considere el primer diagrama de este tema. Dada esta configuración, el procesamiento de datos tendría lugar de la siguiente manera:

1.  "A" envía [METransformNeedInput](metransformneedinput.md) para solicitar datos.
2.  La canalización llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) en "a".
3.  "A" y "B" procesan los datos en el hardware.
4.  Una vez completado el procesamiento, "B" envía un evento [METransformHaveOutput](metransformhaveoutput.md) .
5.  La canalización llama a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en "B".

## <a name="paired-decoderencoder"></a>Descodificador/codificador emparejados

Si un descodificador y un codificador se encuentran en el mismo chip de hardware, puede ser preferible utilizarlos juntos al transcodificar. Es decir, la selección de una debe hacer que la otra se seleccione en la canalización de transcodificación. Para asegurarse de que se eligen los códecs de hardware coincidentes, ambos códecs MFTs deben ofrecer un tipo de medio personalizado. Para crear un tipo de medio personalizado:

-   Establezca el atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) en **MFMediaType \_ audio** o **MFMediaType \_ video**, según corresponda.
-   Establezca el atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) en un valor GUID personalizado.

Otros atributos de tipo son opcionales. El descodificador devuelve el tipo personalizado de su [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)y el codificador devuelve el tipo personalizado de su método [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) . En ambos casos, el tipo personalizado debe ser la primera entrada de la lista (*dwTypeIndex* = 0).

Para trabajar con los códecs de software, el códec también debe devolver al menos un formato estándar, como NV12 para vídeo. Los formatos estándar deben aparecer después del tipo personalizado (*dwTypeIndex* > 0). Si los dos códecs siempre deben estar emparejados y no pueden interoperar con los códecs de software, el MFTs debe devolver solo el formato personalizado y no devolver ningún formato estándar.

> [!Note]  
> Si un descodificador no devuelve ningún formato estándar, no se puede usar para la reproducción con el [representador de vídeo mejorado](enhanced-video-renderer.md). En ese caso, se debe registrar como un descodificador de solo transcodificación. Vea [descodificadores de solo transcodificación](implementing-a-codec-mft.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> <dt>

[Implementar un MFT de códec](implementing-a-codec-mft.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




