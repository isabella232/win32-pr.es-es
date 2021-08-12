---
description: El &\# 0034;leaky bucket&0034; es una manera de modelar los requisitos de almacenamiento en búfer para una \# reproducción sin problemas.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: El modelo de búfer de cubo filtrada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848a0088a0e2b155deb6945e4a6532edb2677dc484341e50172f1bb1eb8187d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238061"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>El modelo de búfer de cubo filtrada (Microsoft Media Foundation)

Al transmitir medios a través de una red, el descodificador recibe datos codificados a una velocidad teóricamente constante (la velocidad de transmisión). El descodificador consume estos datos para generar una salida descodificada. Sin embargo, en el caso general, el descodificador consume los datos a una velocidad *variable,* ya que el codificador puede usar una velocidad de codificación variable.

El modelo de "cubo de fugas" es una manera de modelar los requisitos de almacenamiento en búfer para una reproducción sin problemas. En este modelo, el descodificador mantiene un búfer. Los datos codificados van de la red al búfer y del búfer al descodificador. Si el búfer se subdesborda, significa que el descodificador quita datos del búfer más rápido de lo que la red está entregando. Si el búfer se desborda, significa que la red entrega datos más rápido de lo que el descodificador los consume.

En este tema se describe el modelo de "cubo de pérdida" de búferes para codificación y codificación.

-   [El cubo de pérdidas](#the-leaky-bucket)
-   [El cubo en uso](#the-bucket-in-use)
-   [Establecimiento de valores de cubo de pérdidas para asf Secuencias](#setting-leaky-bucket-values-for-asf-streams)
-   [Valores de cubo con fugas en el multiplexor de ASF](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Actualización de los valores del cubo de pérdidas en el receptor de medios de ASF](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Temas relacionados](#related-topics)

## <a name="the-leaky-bucket"></a>El cubo de pérdidas

Para comprender el modelo de cubo con fugas, considere la posibilidad de un cubo con un pequeño hueco en la parte inferior. Tres parámetros definen el cubo:

-   La capacidad (B)
-   Velocidad a la que fluye el agua fuera del depósito (R)
-   La integridad inicial del cubo (F)

En esta metáfora, el cubo es el búfer:

![ilustración en la que se muestra un búfer como depósito, la velocidad de entrada como agua que entra en el cubo y la velocidad de salida como agua que sale a través de un hueco en el cubo](images/asf-components03.png)

Si el agua se vierte al depósito a la velocidad *exacta R*, el cubo permanecerá en F, porque la velocidad de entrada es igual a la velocidad de salida. Si la tasa de entrada aumenta mientras *R sigue* siendo constante, el depósito acumula agua. Si la velocidad de entrada es mayor que *R* durante un período sostenido, finalmente el cubo se desborda. Sin embargo, la velocidad de entrada puede variar en torno a *R* sin desbordar el cubo, siempre y cuando la tasa de entrada media no supere la capacidad del cubo. Cuanto mayor sea la capacidad, más puede variar la velocidad de entrada en un período de tiempo determinado.

En ASF, el cubo con pérdidas se define mediante tres parámetros:

-   Velocidad de bits media, en bytes por segundo, que corresponde a la velocidad de salida *(R*)
-   Ventana de búfer, medida en milisegundos, que corresponde a la capacidad del cubo (*B*).
-   La integridad inicial del búfer, que generalmente se establece en cero.

La velocidad de bits mide el número medio de bits por segundo en la secuencia codificada. La ventana de búfer mide el número de milisegundos de datos a esa velocidad de bits que puede caber en el búfer. El tamaño del búfer en bits es igual a R \* (B/1000).

Los datos de carga de ASF pueden entrar en el cubo con pérdidas en momentos irregulares y en cantidades irregulares, pero deben dejar el cubo a una velocidad de bits positiva constante. Debido a la ventana de búfer, hay un posible retraso entre el momento en que la carga entra en el cubo y cuando sale. El retraso máximo que puede producirse es *B* / *R*. Los datos de carga que entran en el cubo se según el tiempo de presentación y nunca deben desbordar el cubo. Además del tiempo de presentación, cada carga también tiene un tiempo de envío, la hora a la que los datos de carga dejan el cubo según la velocidad de bits. El tiempo de envío debe ser anterior al tiempo de presentación para asegurarse de que, cuando el cubo con pérdidas se acerca a estar lleno, cada carga sale del cubo antes o en su momento de presentación. Para ello, los tiempos de presentación se desplazan por delante por el valor de *B* R (el preinseleccionado) y las horas de envío obtienen un inicio inicial inicial /  a partir de cero.  El tiempo de envío no debe ser posterior al tiempo de presentación, ya que esto indicaría que la carga entraba en el cubo demasiado tarde y no se puede incluir en el objeto de datos. El valor de la inscripción previa se incluye en el objeto [de encabezado asf](asf-file-structure.md) .

Para el streaming sin problemas a través de la red, las secuencias comprimidas dentro del contenido multimedia deben mantener una velocidad de bits constante a lo largo de la duración de la reproducción. El modelo de cubo de pérdida de ASF garantiza que los datos multimedia se envían a través de la red a una velocidad de bits constante. Los parámetros del cubo de pérdidas se especifican en el objeto propiedades de flujo extendido del objeto [de encabezado ASF](asf-file-structure.md). En Microsoft Media Foundation, se establecen como atributos en el tipo de medio que representa la secuencia.

Los valores del cubo de pérdida se definen tanto en el receptor del archivo ASF como en el objeto multiplexor de ASF subyacente, y en Windows Codificador multimedia. Estos valores pueden ser iguales o diferentes. Por ejemplo, considere un escenario de streaming, que requiere que los ejemplos de audio se entreguen más adelante que los ejemplos de vídeo para que el archivo se pueda transmitir sin latencia. Para ello, el cubo de fugas de la secuencia de audio en el receptor de medios se puede establecer en un valor superior al establecido en el codificador de audio multimedia Windows multimedia.

Para establecer valores de B/R en el codificador, la aplicación debe establecer las propiedades [**MFPKEY \_ PRESSG,**](mfpkey-ravgproperty.md) [**MFPKEY \_ BAVG,**](mfpkey-bavgproperty.md) [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)y [**MFPKEY \_ BMAX.**](mfpkey-bmaxproperty.md) Para obtener información sobre cómo establecer propiedades en el codificador, vea [Propiedades de codificación.](configuring-the-encoder.md)

## <a name="the-bucket-in-use"></a>El cubo en uso

El objetivo de un codificador es asegurarse de que el contenido nunca desborda el búfer. El codificador usa los valores de velocidad de bits y ventana de búfer como guías. El número real de bits pasados en cualquier período de tiempo igual a la ventana de búfer nunca puede ser mayor que el doble del tamaño del búfer.

Considere el ejemplo siguiente: tiene un cubo de tres cubos con un hueco en él a través del cual puede fluir 1 minuto. Coloque el cubo bajo una aguja y abra la válvula para dejar salir el agua a una velocidad de 1 minuto. El agua sale del depósito tan pronto como entra, sin dejar ningún adicional en el cubo. A continuación, aumente el flujo de la spi spi a 2 ones por minuto. Cada minuto en que el agua fluye a esta velocidad, 2 va en el cubo y 1 fuga, dejando 1 en el cubo. Al final de 3 minutos, han pasado seis depósitos de agua al cubo, tres han desaparecido y el cubo está lleno.

En la práctica, nunca se logra la velocidad de datos máxima teórica durante un intervalo igual a la ventana de búfer. En el ejemplo anterior se presupone una velocidad de datos constante. Dado el mismo cubo de 3 minutos, podría aumentar la velocidad de flujo desde el spi a 6 nins por minuto durante un minuto y, a continuación, desactivar el spiion durante dos minutos. Aunque la cantidad total de agua que se coloca en el depósito se encuentra dentro del máximo teórico de la ventana de búfer, la concentración de esa cantidad en una parte de la ventana hace que el cubo se desborde. A 6 grados por minuto, el cubo de 3 segundos se desborda poco después de pasar 30 segundos. Por lo tanto, la cantidad máxima real de datos que se pueden entregar al búfer durante cualquier intervalo igual a la configuración de la ventana de búfer depende del tamaño de las muestras individuales y del momento en que se entregan.

Hasta ahora, los ejemplos solo han analizado el búfer usado por el descodificador, pero el codificador también usa un búfer de cubo con fugas que crea el contenido comprimido. El codificador realiza los ajustes necesarios en los algoritmos de compresión para mantener la velocidad de bits de las muestras comprimidas dentro de los límites descritos por la velocidad de bits y la ventana de búfer, suponiendo que las muestras se entreguen al descodificador a una velocidad constante. Puede pensar en el cubo del codificador como la creación de reflejo del cubo del descodificador. El cubo del codificador se rellena a una velocidad variable determinada por el tamaño de las muestras individuales y las pérdidas a una velocidad constante igual a la velocidad de bits media.

Considere el ejemplo siguiente de un codificador y descodificador conectados juntos a través de una red. Codifica un archivo de vídeo a 30 fotogramas por segundo con una velocidad de bits de 6000 bits por segundo y una ventana de búfer de 3 segundos (un tamaño total de búfer de 18 000 bits). El primer ejemplo se codifica como un fotograma clave y ocupa 7000 bits. El búfer del codificador ahora contiene 7000 bits. Los 29 fotogramas siguientes son fotogramas delta que suman un total de 3000 bits. Por lo tanto, el primer segundo de contenido (30 fotogramas) colocaría la integridad del búfer en 10 000 bits si no se filtrara nada. Sabemos que la velocidad de bits de la secuencia es de 6000 bits por segundo, por lo que después de colocar el primer segundo de contenido codificado en el búfer del codificador, la integridad disminuye a 4000 bits. En la aplicación de descodificación, esta secuencia se entrega al búfer del descodificador a 6000 bits por segundo. Después de un segundo, el búfer contiene 6000 bits. El primer ejemplo contiene 7000 bits, por lo que el búfer del descodificador debe rellenarse más antes de que el descodificador comience a quitar muestras.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Establecimiento de valores de cubo de pérdidas para asf Secuencias

En un escenario de codificación de archivos, una aplicación puede establecer los valores del cubo de pérdidas al configurar las secuencias en el [perfil de ASF](asf-profile.md).

Después de crear la secuencia y tener una referencia a la interfaz [**DEFSTREAMConfig DE LA SECUENCIA,**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) puede establecer los valores mediante los siguientes atributos:

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (promedio de valores de cubo con fugas)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valores máximos del cubo de pérdidas)

Para obtener información sobre cómo agregar secuencias y obtener el puntero **IMFASFStreamConfig,** vea [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).

Estos valores contienen el siguiente conjunto de información:

-   Velocidad de bits media: obtenga la velocidad de bits media del tipo de medio de salida seleccionado durante la negociación del tipo de medio. Use el [**atributo MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) (para secuencias de audio) o el atributo [**MF MT AVG \_ \_ \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) (para secuencias de vídeo).
-   Ventana búfer: si tiene una instancia del codificador y tiene tipos de medios de salida negociados, puede actualizar este valor más adelante consultando el codificador para la interfaz [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) y llamando a [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib). De lo contrario, use el valor predeterminado de 3000 milisegundos.
-   Tamaño inicial del búfer: se establece en 0.

Los valores proporcionados por la aplicación dependen del tipo de codificación y el tipo de medio de la secuencia. Por ejemplo, [la codificación de velocidad de](constant-bit-rate-encoding.md) bits constante requiere una velocidad de bits fija predeterminada y una ventana de búfer. La aplicación puede especificar estos valores de cubo de pérdida estableciendo la propiedad de codificación [**MFPKEY \_ VIDEOWINDOW**](mfpkey-videowindowproperty.md) y el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en la secuencia. Los valores de ventana de búfer especificados se usan para asegurarse de que el archivo codificado tiene las horas de envío correctas marcadas en los paquetes de datos y que el valor de inscripción previa aparece en el objeto de encabezado asf. Es suficiente establecer **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** porque estos valores especificados se copian en el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2.**](mf-asfstreamconfig-leakybucket2-attribute.md)

Para los modos de codificación de dos pasos, debe establecer ambos atributos para especificar los valores promedio y máximo.

En el caso de la codificación VBR, la aplicación puede consultar los valores del cubo de pérdida usados por el codificador solo después de que se complete el paso de codificación. Por lo tanto, al configurar el receptor de medios, la aplicación puede optar por no establecer los atributos o propiedades relacionados con cubos con pérdidas. Después de la codificación, la aplicación debe consultar en el codificador las propiedades [**MFPKEY \_ SOAPG,**](mfpkey-ravgproperty.md) [**MFPKEY \_ BAVG,**](mfpkey-bavgproperty.md) [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)y [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) y establecerlas en el receptor de medios para que los valores precisos se reflejen en el objeto de encabezado. Para obtener un ejemplo de código sobre cómo actualizar los valores para la codificación VBR, vea "Actualizar propiedades de codificación en el receptor de archivos" en [Tutorial: 1-Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

Si va a copiar contenido Windows multimedia desde el origen al receptor multimedia sin codificación, los valores del cubo de pérdida deben establecerse en el receptor de medios.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Valores de cubo con fugas en el multiplexor de ASF

En Media Foundation, el [multiplexor de ASF](asf-multiplexer.md) usa los valores del cubo de fugas para configurar los valores internos del cubo de fugas que usa para generar paquetes de datos. La carga se encuentra dentro de un ejemplo multimedia y una serie de muestras multimedia constituye un paquete de datos de ASF. En función de los valores del cubo de fugas y el tiempo de presentación, el multiplexador asigna un tiempo de envío para cada ejemplo multimedia de modo que las velocidades de bits de los paquetes que se envían a través de la red se encuentra en una velocidad de bits constante *(R*).

Una aplicación no puede establecer directamente los valores del cubo de pérdidas en el multiplexor. Los valores deben proporcionarse en el receptor de medios de ASF, que establece los valores adecuados en el multiplexor. El multiplexor usa los valores establecidos en [**\_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) y [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) para validar que los ejemplos enviados al receptor de medios de ASF se generan mediante los valores especificados.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Actualización de los valores del cubo de pérdidas en el receptor de medios de ASF

Una aplicación puede sobrescribir los valores del cubo de pérdida de nivel de flujo (establecidos en el perfil de ASF durante la creación de la secuencia) estableciendo la propiedad [**\_ MFPKEY ASFSTREAMSINK \_ \_ CORRECTED LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) en el almacén de propiedades del receptor de medios. Para obtener una referencia al almacén de propiedades, use el objeto ContentInfo implementado por el receptor de medios. Para obtener más información, vea [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).

**Nota**  Esta operación solo se permite para secuencias de audio.

Esta propiedad debe establecerse después de haber establecido el tipo de salida en el codificador. En función de la velocidad de bits establecida en el tipo de medio, el codificador calcula el tamaño del búfer para asegurarse de que las muestras de medios generadas nunca desbordan el búfer. El codificador realiza los ajustes necesarios durante la compresión para mantener la velocidad de bits de las muestras comprimidas dentro de los límites descritos por la velocidad de bits y la ventana de búfer.

De forma similar a los atributos de configuración de flujo para cubos con pérdidas, establezca la velocidad de bits media y el tamaño del búfer, y la integridad inicial del búfer en una matriz de DWORD. Para obtener más información, vea la sección "Establecimiento de valores de cubo con fugas Secuencias ASF" de este tema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
