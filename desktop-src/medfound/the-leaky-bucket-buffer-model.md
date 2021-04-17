---
description: El &\# 0034; depósito de fugas&\# 0034; modelo es una forma de modelar los requisitos de almacenamiento en búfer para la reproducción fluida.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: El modelo de búfer de depósito con fugas (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a99932fb121808f6a49323360c47c09d0acbb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717413"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>El modelo de búfer de depósito con fugas (Microsoft Media Foundation)

Al transmitir por secuencias contenido multimedia a través de una red, el descodificador recibe datos codificados en una velocidad teóricamente constante (la velocidad de transmisión). El descodificador consume estos datos para generar una salida descodificada. Sin embargo, en el caso general, el descodificador consume los datos a una velocidad *variable* , ya que el codificador puede usar una velocidad de codificación variable.

El modelo de "depósito de fugas" es una manera de modelar los requisitos de almacenamiento en búfer para la reproducción fluida. En este modelo, el descodificador mantiene un búfer. Los datos codificados van de la red al búfer y del búfer al descodificador. Si el búfer se desborda, significa que el descodificador está quitando datos del búfer más rápidamente de lo que la red lo está entregando. Si el búfer se desborda, significa que la red está entregando datos más rápido de lo que el descodificador lo consume.

En este tema se describe el modelo de "depósito de fugas" de búferes para la codificación y la descodificación.

-   [El depósito de fugas](#the-leaky-bucket)
-   [El depósito en uso](#the-bucket-in-use)
-   [Establecimiento de valores de cubo con fugas para secuencias ASF](#setting-leaky-bucket-values-for-asf-streams)
-   [Valores de depósito con fugas en el multiplexor ASF](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Actualización de valores de cubo con fugas en el receptor de medios ASF](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Temas relacionados](#related-topics)

## <a name="the-leaky-bucket"></a>El depósito de fugas

Para entender el modelo de depósito con fugas, considere la posibilidad de un cubo con un pequeño orificio en la parte inferior. Tres parámetros definen el cubo:

-   La capacidad (B)
-   La velocidad a la que el agua fluye fuera del depósito (R)
-   El llenado inicial del depósito (F)

En esta metáfora, el cubo es el búfer:

![Ilustración en la que se muestra un búfer como un depósito, la velocidad de entrada como agua que entra en el depósito y la tasa de salida como agua que sale por un orificio en el depósito](images/asf-components03.png)

Si el agua se vierten en el depósito con la velocidad *R* exactamente, el cubo permanecerá en F, ya que la tasa de entrada es igual a la tasa de salida. Si la velocidad de entrada aumenta mientras *R* permanece constante, el depósito acumula agua. Si la velocidad de entrada es mayor que *R* durante un período sostenido, el cubo se desborda. Sin embargo, la velocidad de entrada puede variar en torno a *R* sin desbordar el cubo, siempre que la tasa de entrada promedio no supere la capacidad del depósito. Cuanto mayor sea la capacidad, más la velocidad de entrada puede variar dentro de un período de tiempo determinado.

En ASF, el depósito de fugas se define mediante tres parámetros:

-   La velocidad de bits promedio, en bytes por segundo, que corresponde a la tasa de salida (*R*)
-   La ventana de búfer, medida en milisegundos, que corresponde a la capacidad de depósito (*B*).
-   El llenado inicial del búfer, que normalmente se establece en cero.

La velocidad de bits mide el promedio de bits por segundo en el flujo codificado. La ventana de búfer mide el número de milisegundos de datos a la velocidad de bits que pueden caber en el búfer. El tamaño del búfer en bits es igual a R \* (B/1000).

Los datos de carga de ASF pueden entrar en el depósito de fugas en momentos irregulares y en cantidades irregulares, pero deben dejar el depósito en una velocidad de bits positivo constante. Debido a la ventana de búfer, existe un posible retraso entre el momento en que la carga entra en el cubo y el momento en que lo abandona. El retraso máximo que se puede producir es *B* / *R*. Los datos de carga que entran en el depósito están según el tiempo de presentación y nunca deben desbordar el depósito. Además del tiempo de presentación, cada carga también tiene un tiempo de envío, es decir, la hora a la que los datos de carga salen del cubo según la velocidad de bits. La hora de envío debe ser anterior al tiempo de presentación para asegurarse de que, cuando el depósito de fugas esté cerca de estar lleno, cada carga deja el cubo antes o en el momento de la presentación. Para ello, los tiempos de presentación se desplazan hacia arriba *por el* / valor de *R* (el *predesplazamiento*) y los tiempos de envío obtienen un encabezado empiece a partir de cero. La hora de envío no debe ser posterior a la hora de presentación, ya que esto indicaría que la carga entró en el depósito demasiado tarde y no se puede incluir en el objeto de datos. El valor de reversión se incluye en el [objeto de encabezado ASF](asf-file-structure.md) .

Para el streaming sin problemas a través de la red, las secuencias comprimidas dentro del contenido multimedia deben mantener una velocidad de bits constante a lo largo de la duración de la reproducción. El modelo de depósito de fugas ASF garantiza que los datos multimedia se envíen a través de la red a una velocidad de bits constante. Los parámetros del depósito de fuga se especifican en el objeto Extended Stream Properties del [objeto de encabezado ASF](asf-file-structure.md). En Microsoft Media Foundation, se establecen como atributos en el tipo de medio que representa la secuencia.

Los valores del depósito con fugas se definen tanto en el receptor de archivos ASF como en el objeto multiplexor ASF subyacente, y en el codificador de Windows Media. Estos valores pueden ser iguales o diferentes. Por ejemplo, considere un escenario de streaming, que requiere que las muestras de audio se entreguen después de los ejemplos de vídeo para que el archivo se pueda transmitir sin latencia. Para ello, el depósito de fugas del flujo de audio del receptor de medios se puede establecer en un valor mayor que el valor establecido en el codificador de audio de Windows Media.

Para establecer los valores de B/R en el codificador, la aplicación debe establecer las propiedades [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)y [**MFPKEY \_ Bmax**](mfpkey-bmaxproperty.md) . Para obtener información sobre cómo establecer las propiedades del codificador, consulte [propiedades de codificación](configuring-the-encoder.md).

## <a name="the-bucket-in-use"></a>El depósito en uso

El objetivo de un codificador es asegurarse de que el contenido nunca desborda el búfer. El codificador usa los valores de velocidad de bits y de la ventana de búfer como guías. El número real de bits pasados a lo largo de un período de tiempo igual a la ventana de búfer nunca puede ser mayor que el doble del tamaño del búfer.

Considere el ejemplo siguiente: tiene un depósito de 3 litros con un orificio en él a través del cual 1 galones puede fluir por minuto. Coloque el depósito en una spigot y abra la válvula para dejar agua a una velocidad de 1 galón por minuto. El agua fluye fuera del cubo tan pronto como entra, sin dejar ningún extra en el cubo. A continuación, se aumenta el flujo de spigot a 2 galones por minuto. Cada minuto que el agua fluye a esta velocidad, 2 litros entran en el depósito y 1 galones se filtran, lo que sale de 1 galones en el cubo. Al final de 3 minutos, se han desplazado 6 litros de agua en el depósito, se han perdido 3 galones y el cubo está lleno.

En la práctica, nunca se consigue la velocidad de datos máxima teórica a lo largo de un intervalo igual a la ventana del búfer. En el ejemplo anterior se presupone una velocidad de datos constante. Dado el mismo depósito de 3 litros, podría aumentar la velocidad de flujo de spigot a 6 galones por minuto durante un minuto y, a continuación, desactivar el spigot durante dos minutos. Aunque la cantidad total de agua que se coloca en el depósito está dentro del máximo teórico de la ventana de búfer, la concentración de esa cantidad en una parte de la ventana provoca el desbordamiento del cubo. A 6 galones por minuto, el depósito de 3 litros se desborda poco después de pasar 30 segundos. Por lo tanto, la cantidad de datos máxima real que se puede entregar al búfer a lo largo de un intervalo igual a la configuración de la ventana de búfer depende del tamaño de cada uno de los ejemplos y del momento en que se entregan.

Hasta ahora, los ejemplos solo han analizado el búfer usado por el descodificador, pero el codificador que crea el contenido comprimido también usa un búfer de cubo de pérdida de memoria. El codificador realiza los ajustes necesarios en los algoritmos de compresión para mantener la velocidad de bits de los ejemplos comprimidos dentro de los límites descritos por la ventana velocidad de bits y búfer, suponiendo que los ejemplos se entreguen al descodificador a una velocidad constante. Puede pensar en el cubo del codificador como la creación de reflejo del cubo del descodificador. El depósito del codificador se rellena a una velocidad variable determinada por el tamaño de las muestras individuales y las pérdidas a una velocidad constante igual a la velocidad de bits promedio.

Considere el ejemplo siguiente de un codificador y un descodificador conectados juntos a través de una red. Codifica un archivo de vídeo en 30 fotogramas por segundo con una velocidad de bits de 6.000 bits por segundo y una ventana de búfer de 3 segundos (un tamaño de búfer total de 18.000 bits). La primera muestra se codifica como un fotograma clave y ocupa 7.000 bits. El búfer del codificador ahora contiene 7.000 bits. Los 29 fotogramas siguientes son todos fotogramas Delta que tienen un total de 3.000 bits. Por lo tanto, el primer segundo de contenido (30 fotogramas) pondría el llenado de búfer en 10.000 bits si no se ha perdido nada. Sabemos que la velocidad de bits de la secuencia es 6.000 bits por segundo, por lo que, una vez que el primer segundo del contenido codificado se coloca en el búfer del codificador, el llenado desciende hasta 4.000 bits. En la aplicación de descodificación, esta secuencia se entrega al búfer del descodificador en 6.000 bits por segundo. Después de un segundo, el búfer contiene 6.000 bits. El primer ejemplo contiene 7.000 bits, por lo que el búfer del descodificador debe rellenarse más antes de que el descodificador comience a quitar ejemplos.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Establecimiento de valores de cubo con fugas para secuencias ASF

En un escenario de codificación de archivos, una aplicación puede establecer los valores del depósito de fugas mientras se configuran las secuencias en el [perfil ASF](asf-profile.md).

Después de crear la secuencia y tener una referencia a la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) de la secuencia, puede establecer los valores con los siguientes atributos:

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valores de cubo de fugas promedio)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valores de depósito máximo de fugas)

Para obtener información sobre cómo agregar secuencias y obtener el puntero **IMFASFStreamConfig** , consulte [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md).

Estos valores contienen el siguiente conjunto de información:

-   Velocidad de bits media: obtiene la velocidad de bits media del tipo de medio de salida que se selecciona durante la negociación del tipo de medio. Use el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para secuencias de audio) o el atributo de velocidad de [**\_ \_ \_ bits media MF MT**](mf-mt-avg-bitrate-attribute.md) (para secuencias de vídeo).
-   Ventana de búfer: Si tiene una instancia del codificador y ha negociado tipos de medios de salida, puede actualizar este valor más adelante consultando el codificador para la interfaz [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) y llamando a [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib). De lo contrario, use el valor predeterminado de 3000 milisegundos.
-   Tamaño de búfer inicial: establézcalo en 0.

Los valores proporcionados por la aplicación dependen del tipo de codificación y del tipo de medio de la secuencia. Por ejemplo, la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md) requiere una velocidad de bits fija predeterminada y una ventana de búfer. La aplicación puede especificar estos valores de depósitos de fugas estableciendo la propiedad de codificación de la [**\_ ventana de videoMFPKEY**](mfpkey-videowindowproperty.md) y el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en la secuencia. Los valores de la ventana de búfer especificada se utilizan para asegurarse de que el archivo codificado tiene las horas de envío correctas marcadas en los paquetes de datos y el valor de la precodificación aparece en el objeto de encabezado ASF. Basta con establecer **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** porque estos valores especificados se copian en el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) .

En el caso de los modos de codificación de dos pasos, debe establecer ambos atributos para especificar los valores promedio y máximo.

En el caso de la codificación VBR, la aplicación puede consultar los valores de los depósitos con fugas usados por el codificador solo después de que se complete la fase de codificación. Por lo tanto, al configurar el receptor de medios, la aplicación puede elegir no establecer los atributos o propiedades relacionados con los depósitos de fugas. Después de la codificación, la aplicación debe consultar al codificador las propiedades [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)y [**MFPKEY \_ Bmax**](mfpkey-bmaxproperty.md) y establecerlas en el receptor de medios para que los valores precisos se reflejen en el objeto de encabezado. Para obtener un ejemplo de código sobre cómo actualizar los valores de la codificación VBR, vea "actualizar las propiedades de codificación en el receptor de archivos" en el [Tutorial: 1-pasar la codificación de Windows Media](tutorial--1-pass-windows-media-encoding.md).

Si va a copiar contenido de Windows Media desde el origen al receptor de medios sin codificación, se deben establecer los valores de los depósitos con fugas en el receptor de medios.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Valores de depósito con fugas en el multiplexor ASF

En Media Foundation, el [multiplexor de ASF](asf-multiplexer.md) usa los valores del depósito de fugas para configurar los valores del cubo de fugas internas que usa para generar paquetes de datos. La carga está incluida en un ejemplo multimedia y una serie de ejemplos de medios constituye un paquete de datos ASF. En función de los valores del depósito de fugas y el tiempo de presentación, el multiplexor asigna un tiempo de envío para cada ejemplo de medio, de modo que las velocidades de bits de los paquetes que se envían a través de la red estén a una velocidad de bits constante (*R*).

Una aplicación no puede establecer valores de cubo con fugas directamente en el multiplexor. Los valores se deben proporcionar en el receptor de medios ASF, que establece los valores adecuados en el multiplexor. El multiplexor usa los valores establecidos en [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) y [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) para validar que las muestras enviadas al receptor de medios ASF se generan usando los valores especificados.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Actualización de valores de cubo con fugas en el receptor de medios ASF

Una aplicación puede sobrescribir los valores del cubo de pérdida de nivel de secuencia (establecido en el perfil ASF durante la creación de la secuencia) estableciendo la propiedad [**MFPKEY \_ ASFSTREAMSINK \_ corregida \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) en el almacén de propiedades del receptor de medios. Para obtener una referencia al almacén de propiedades, use el objeto ContentInfo implementado por el receptor de medios. Para obtener más información, vea [establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).

**Nota:**  Esta operación solo se permite para secuencias de audio.

Esta propiedad debe establecerse después de haber establecido el tipo de salida en el codificador. Según la velocidad de bits establecida en el tipo de medio, el codificador calcula el tamaño del búfer para asegurarse de que los ejemplos de medios generados nunca desbordan el búfer. El codificador realiza los ajustes necesarios durante la compresión para mantener la velocidad de bits de los ejemplos comprimidos dentro de los límites descritos por la ventana de velocidad de bits y de búfer.

Similar a los atributos de configuración de la secuencia para los depósitos con fugas, establecer la velocidad de bits promedio y el tamaño del búfer, y el llenado inicial del búfer en una matriz de DWORDs. Para obtener más información, consulte la sección "configuración de valores de cubos con fugas para secuencias ASF" en este tema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
