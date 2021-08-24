---
description: En este tema se describe cómo escribir una transformación de Media Foundation (MFT) que actúa como proxy para un codificador de hardware, descodificador o procesador de señal digital (DSP).
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: MTA de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532fef959e2c2b5946d5a27ad98106a2e25cc77f8426c0a871e821c7298a69f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724942"
---
# <a name="hardware-mfts"></a>MTA de hardware

> [!Note]  
> Este tema se aplica a Windows 7 o posterior.

 

En este tema se describe cómo escribir una transformación de Media Foundation (MFT) que actúa como proxy para un codificador de hardware, descodificador o procesador de señal digital (DSP).

> [!IMPORTANT]
> Si un códec de hardware usa el controlador de clase multimedia AVStream, no requiere un MFT personalizado. Media Foundation proporciona un proxy AVStream para este propósito. La información de este tema solo se aplica en el caso especial en el que el códec de hardware no usa AVStream. Para obtener más información, vea Compatibilidad con [códecs de hardware en AVStream.](https://msdn.microsoft.com/library/dd568169.aspx)

 

Este tema contiene las siguientes secciones:

-   [Introducción](#introduction)
-   [Atributos MFT de hardware](#hardware-mft-attributes)
-   [Secuencia de protocolo de enlace de hardware](#hardware-handshake-sequence)
-   [Procesamiento de datos](#data-processing)
-   [Descodificador/codificador emparejado](#paired-decoderencoder)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Cualquier códec de hardware que no se base en AVStream debe proporcionar su propio MFT para que actúe como proxy para el controlador. Un códec de hardware podría incorporar varios bloques funcionales distintos:

-   Codificador
-   Descodificador
-   Conversión de formato y escalado de fotogramas

Cada una de estas funciones debe administrarse mediante un MFT independiente. Un MFT de hardware nunca debe actuar como un "transcodificador" multiuso. En su lugar, coloque las funciones de codificación en un MFT del codificador y decoding functions en un descodificador MFT. Si el hardware ofrece conversiones de formato y escalado de fotogramas, coloque esas funciones en un procesador de vídeo independiente, registrado en la categoría PROCESADOR DE VÍDEO CATEGORÍA **MFT. \_ \_ \_** Si el hardware no admite el escalado de fotogramas ni la conversión de formato, Media Foundation un procesador de vídeo de software.

Las MTA de hardware tienen los siguientes requisitos generales:

-   Las MTA de hardware deben usar el nuevo modelo de procesamiento asincrónico, como se describe en [MTA asincrónicos.](asynchronous-mfts.md)
-   Las MTA de hardware deben admitir cambios de formato dinámico, como se describe en [Cambios de formato dinámico.](basic-mft-processing-model.md)

## <a name="hardware-mft-attributes"></a>Atributos MFT de hardware

Un MFT de hardware debe implementar los métodos siguientes relacionados con los atributos:

-   [**IMFTransform::GetAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)devuelve un almacén de atributos para los atributos globales de MFT.
-   [**IMFTransform::GetInputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)devuelve un almacén de atributos para un flujo de entrada.
-   [**IMFTransform::GetOutputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)devuelve un almacén de atributos para un flujo de salida.

Cuando se crea el MFT por primera vez, debe establecer los siguientes atributos en su propio almacén de atributos global (es decir, el almacén de atributos devuelto por [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)):



| Atributo                                                                                    | Descripción                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                               | Debe establecerse en **TRUE.** Indica que MFT realiza el procesamiento asincrónico.                                                                                                      |
| [Atributo MFT \_ ENUM \_ HARDWARE \_ URL \_](mft-enum-hardware-url-attribute.md)                   | Contiene el vínculo simbólico para el dispositivo de hardware.<br/> El cargador de topologías usa la presencia de este atributo para probar si un MFT representa un dispositivo de hardware.<br/> |
| [**MFT \_ ADMITE EL CAMBIO DE FORMATO \_ \_ \_ DINÁMICO**](mft-support-dynamic-format-change-attribute.md) | Debe establecerse en **TRUE.** Indica que MFT admite cambios de formato dinámicos.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Secuencia de protocolo de enlace de hardware

Si dos MTA representan el mismo dispositivo físico, pueden intercambiar datos dentro del hardware, por ejemplo, a través de un bus de hardware. No es necesario copiar los datos en la memoria del sistema y, a continuación, volver al dispositivo.

En el diagrama siguiente, los MTA etiquetados como "A" y "B" representan bloques funcionales dentro del mismo hardware. Por ejemplo, en un escenario de transcodificación, "A" podría representar un descodificador de hardware y "B" podría representar un codificador de hardware. El flujo de datos entre "A" y "B" se produce dentro del hardware. El MFT con la etiqueta "C" es un MFT de software. El flujo de datos de "B" a "C" usa memoria del sistema.

![diagrama que muestra cuadros etiquetados de a a c y un códec de hardware: un punto a b y el códec, el códec apunta a b y b apunta a c](images/proxy-mft.png)

Para establecer una conexión de hardware, las dos MTA de hardware deben usar un canal de comunicación privado. Esta conexión se establece durante la negociación de formato, antes de establecer los tipos de medios y antes de la primera llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). El proceso de conexión funciona de la siguiente manera:

1.  El cargador de topologías comprueba la presencia del atributo [MFT \_ ENUM HARDWARE \_ \_ URL \_ Attribute](mft-enum-hardware-url-attribute.md) en ambos MFT. Tenga en cuenta que no examina el valor de este atributo.
2.  Si [el atributo de dirección URL de hardware de MFT \_ ENUM \_ \_ \_ ](mft-enum-hardware-url-attribute.md) está presente en ambos MFT, el cargador de topologías hace lo siguiente:
    1.  El cargador de topologías [**llama a IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) en el MFT (A) ascendente. Este método devuelve un [**puntero DE TIPO IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Deje que este puntero se denote *como pUpstream*.
    2.  El cargador de topologías [**llama a IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) en el MFT de bajada (B). Esta llamada también devuelve un [**puntero DE TIPO IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Deje que este puntero se denote *como pDownstream*.
    3.  El cargador de topologías establece el atributo [ \_ MFT CONNECTED \_ STREAM \_ ATTRIBUTE](mft-connected-stream-attribute.md) en *pDownstream* mediante una llamada a [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). El valor del atributo es el *puntero pUpstream.*
    4.  El cargador de topologías establece el [atributo \_ MFT CONNECTED \_ TO HW \_ \_ STREAM](mft-connected-to-hw-stream.md) en **TRUE** en *pDownstream* y *pUpstream.*
3.  En este punto, el MFT de bajada tiene un puntero al almacén de atributos de MFT ascendente, como se muestra en el diagrama siguiente.

    ![diagrama con cada mfts que apunta a su flujo, cada flujo que apunta a su almacén y el almacén de entrada con una línea discontinua al almacén de salida](images/proxy-mft2.png)

    > [!Note]  
    > Para mayor claridad, este diagrama muestra las secuencias y los almacenes de atributos como objetos distintos, pero eso no es necesario para la implementación.

     

4.  El MFT de bajada usa el puntero [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer un canal de comunicación privado con el MFT ascendente. Dado que el canal es privado, la implementación define el mecanismo exacto. Por ejemplo, MFT podría consultar una interfaz COM privada.

Durante el paso 4, el MFT de bajada debe comprobar si los dos MFT comparten el mismo dispositivo físico. Si no es así, deben volver a usar la memoria del sistema para el transporte de datos. Esto permite que MFT funcione correctamente con MFT de software y otros dispositivos de hardware.

Si el protocolo de enlace se realiza correctamente y los dos MTA comparten un canal de datos privado, no usan el modelo de procesamiento de datos estándar (descrito en la sección siguiente) en el punto de conexión. En concreto, el MFT de bajada no envía [eventos METransformNeedInput;](metransformneedinput.md) Para obtener más información, consulte la sección siguiente de este tema.

## <a name="data-processing"></a>Procesamiento de datos

Cuando un MFT de hardware usa memoria del sistema para el transporte de datos, el proceso funciona de la siguiente manera:

1.  Para solicitar más entradas, MFT envía un [evento METransformNeedInput.](metransformneedinput.md)
2.  El [evento METransformNeedInput hace](metransformneedinput.md) que la canalización llame a [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
3.  Cuando MFT tiene datos de salida, MFT envía un [evento METransformTransformTransformOutput.](metransformhaveoutput.md)
4.  El [evento METransformTransformTransformOutput](metransformhaveoutput.md) hace que la canalización llame a [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Para obtener más información, consulte [MFT asincrónicos.](asynchronous-mfts.md)

Sin embargo, si MFT usa un canal de hardware, no envía estos eventos en el punto de conexión de hardware, ya que toda la transferencia de datos se realiza internamente dentro del hardware. Por lo tanto, la canalización no llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) o [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en el punto de conexión.

Por ejemplo, considere el primer diagrama de este tema. Dada esta configuración, el procesamiento de datos se produciría de la siguiente manera:

1.  "A" envía [METransformNeedInput para](metransformneedinput.md) solicitar datos.
2.  La canalización llama [**a ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) en "A".
3.  "A" y "B" procesan los datos en hardware.
4.  Una vez completado el procesamiento, "B" envía un [evento METransformTransformTransformOutput.](metransformhaveoutput.md)
5.  La canalización llama [**a ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en "B".

## <a name="paired-decoderencoder"></a>Descodificador/codificador emparejado

Si un descodificador y un codificador se encuentran en el mismo chip de hardware, puede ser preferible usarlos juntos al transcodificación. Es decir, al seleccionar uno se debe hacer que el otro se seleccione en la canalización de transcodificación. Para asegurarse de que se eligen códecs de hardware que coincidan, ambos códecs deben ofrecer un tipo de medio personalizado. Para crear un tipo de medio personalizado:

-   Establezca el [**atributo MF MT MAJOR \_ \_ \_ TYPE**](mf-mt-major-type-attribute.md) en **MFMediaType \_ Audio** o **MFMediaType \_ Video**, según corresponda.
-   Establezca el [**atributo MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) en un valor GUID personalizado.

Otros atributos de tipo son opcionales. El descodificador devuelve el tipo personalizado a partir de [**su valor DECITRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)y el codificador devuelve el tipo personalizado de su [**método IMFTransform::GetInputAvailableType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) En ambos casos, el tipo personalizado debe ser la primera entrada de la lista (*dwTypeIndex* = 0).

Para trabajar con códecs de software, el códec también debe devolver al menos un formato estándar, como NV12 para vídeo. Los formatos estándar deben aparecer después del tipo personalizado *(dwTypeIndex* > 0). Si los dos códecs siempre deben estar emparejados y no pueden interoperar con códecs de software, los MTA solo deben devolver el formato personalizado y no devolver ningún formato estándar.

> [!Note]  
> Si un descodificador no devuelve ningún formato estándar, no se puede usar para la reproducción con el [representador de vídeo mejorado](enhanced-video-renderer.md). En ese caso, debe registrarse como descodificador de solo transcodificación. Vea [Descodificadores de solo transcodificación.](implementing-a-codec-mft.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir un MFT personalizado](writing-a-custom-mft.md)
</dt> <dt>

[Implementación de un MFT de códec](implementing-a-codec-mft.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 




