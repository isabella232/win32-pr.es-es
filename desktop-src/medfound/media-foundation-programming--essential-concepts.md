---
description: Si no está nuevo en los medios digitales, en este tema se presentan algunos conceptos que debe comprender antes de escribir una Media Foundation aplicación.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: conceptos esenciales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825e84b3c7ad3060cae0a2530bc9a7af3155fd9113c490ce2c42f69771c1f9b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357270"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: conceptos esenciales

Si no está nuevo en los medios digitales, en este tema se presentan algunos conceptos que debe comprender antes de escribir una Media Foundation aplicación.

-   [Secuencias](#streams)
-   [Compresión](#compression)
-   [Contenedores multimedia](#media-containers)
-   [Formatos](#formats)
-   [Temas relacionados](#related-topics)

## <a name="streams"></a>Secuencias

Una *secuencia* es una secuencia de datos multimedia con un tipo uniforme. Los tipos más comunes son audio y vídeo, pero una secuencia puede contener casi cualquier tipo de datos, incluido texto, comandos de script e imágenes fijas. El término *secuencia de* esta documentación no implica la entrega a través de una red. Un archivo multimedia destinado a la reproducción local también contiene secuencias.

Normalmente, un archivo multimedia contiene una sola secuencia de audio o exactamente una secuencia de vídeo y una secuencia de audio. Sin embargo, un archivo multimedia puede contener varias secuencias del mismo tipo. Por ejemplo, un archivo de vídeo podría contener secuencias de audio en varios idiomas diferentes. En tiempo de ejecución, la aplicación seleccionaría la secuencia que se va a usar.

## <a name="compression"></a>Compresión

*La* compresión hace referencia a cualquier proceso que reduzca el tamaño de un flujo de datos mediante la eliminación de información redundante. Los algoritmos de compresión se divide en dos categorías generales:

-   *Compresión sin* pérdida de datos. Con un algoritmo sin pérdida, los datos reconstruidos son idénticos al original.
-   *Compresión de pérdida.* Con un algoritmo de pérdida, los datos reconstruidos son una aproximación del original, pero no es una coincidencia exacta.

En la mayoría de los demás dominios, la compresión de pérdida no es aceptable. (Imagine obtener una "aproximación" de una hoja de cálculo). Pero los esquemas de compresión con pérdida son adecuados para audio y vídeo, por un par de motivos.

La primera razón tiene que ver con la física de la percepción humana. Cuando escuchamos un sonido complejo, como una grabación de música, parte de la información contenida en ese sonido no es perceptible para el oído. Con la ayuda de la teoría del procesamiento de señales, es posible analizar y separar las frecuencias que no se pueden percibir. Estas frecuencias se pueden quitar sin ningún efecto perceptual. Aunque el audio reconstruido no coincidirá exactamente con el original, *sonará* igual al agente de escucha. Se aplican principios similares al vídeo.

En segundo lugar, es posible que se acepte alguna degradación en la calidad del sonido o de la imagen, en función del propósito previsto. En telefonía, por ejemplo, el audio suele estar muy comprimido. El resultado es lo suficientemente bueno para una conversación telefónica, pero no le gustaría escuchar a una orquestal a través de un teléfono.

La compresión también se denomina *codificación* y un dispositivo que codifica se denomina *codificador*. El proceso inverso está *descodificando* y el dispositivo es un descodificador denominado de forma *natural.* El término general para los codificadores y descodificadores es *el códec*. Los códecs se pueden implementar en hardware o software.

La tecnología de compresión ha cambiado rápidamente desde la llegada de los medios digitales y actualmente se usa un gran número de esquemas de compresión. Este hecho es uno de los principales desafíos de la programación de medios digitales.

## <a name="media-containers"></a>Contenedores multimedia

No es habitual almacenar una secuencia de audio o vídeo sin procesar como un archivo de equipo o enviar una directamente a través de la red. Por un lado, sería imposible descodificar este tipo de secuencia, sin saber de antemano qué códec usar. Por lo tanto, los archivos multimedia normalmente contienen al menos algunos de los siguientes elementos:

-   Encabezados de archivo que describen el número de secuencias, el formato de cada secuencia, y así sucesivamente.
-   Índice que permite el acceso aleatorio al contenido.
-   Metadatos que describen el contenido (por ejemplo, el intérprete o el título).
-   Encabezados de paquete, para habilitar la transmisión de red o el acceso aleatorio.

En esta documentación se usa el término *contenedor* para describir todo el paquete de secuencias, encabezados, índices, metadatos, etc. La razón para usar el término *contenedor en* lugar de *archivo* es que algunos formatos de contenedor están diseñados para la difusión en vivo. Una aplicación podría generar el contenedor en tiempo real, nunca almacenarlo en un archivo.

Un ejemplo temprano de un contenedor multimedia es el formato de archivo AVI. Otros ejemplos son MP4 y Advanced Systems Format (ASF). Los contenedores se pueden identificar por extensión de nombre de archivo (por ejemplo, .mp4) o por tipo MIME.

En el diagrama siguiente se muestra una estructura típica para un contenedor multimedia. El diagrama no representa ningún formato específico; los detalles de cada formato varían mucho.

![diagrama que muestra un contenedor multimedia típico](images/concepts01.png)

Observe que la estructura que se muestra en el diagrama es jerárquica, con información de encabezado que aparece al principio del contenedor. Esta estructura es típica de muchos formatos de contenedor (pero no todos). Observe también que la sección de datos contiene paquetes de audio y vídeo intercalados. Este tipo de intercalación es común en los contenedores multimedia.

El término *multiplexación hace* referencia al proceso de paquetes de las secuencias de audio y vídeo e intercalación de los paquetes en el contenedor. El proceso inverso, volver a recomprimir las secuencias de los datos en paquetes, se denomina *demultiplexación.*

## <a name="formats"></a>Formatos

En los medios digitales, el *término formato* es ambiguo. Un formato puede hacer referencia al tipo de *codificación,* como vídeo H.264, o al *contenedor*, como MP4. Esta distinción suele resultar confusa para los usuarios normales. Los nombres dados a los formatos multimedia no siempre ayudan. Por ejemplo, *MP3 hace referencia* tanto a un formato de codificación (MPEG-1 Audio Layer 3) como a un formato de archivo.

Sin embargo, la distinción es importante porque la lectura de un archivo multimedia implica realmente dos fases:

1.  En primer lugar, se debe analizar el contenedor. En la mayoría de los casos, el número de secuencias y el formato de cada secuencia no se pueden conocer hasta que se complete este paso.
2.  A continuación, si las secuencias están comprimidas, deben descodificarse con los descodificadores adecuados.

Este hecho conduce de forma natural a un diseño de software en el que se usan componentes independientes para analizar contenedores y descodificar secuencias. Además, este enfoque se presta a un modelo de complemento, para que terceros puedan proporcionar sus propios analizadores y códecs. En Windows, el modelo de objetos componentes (COM) proporciona una manera estándar de separar una API de su implementación, que es un requisito para cualquier modelo de complemento. Por esta razón (entre otros), Media Foundation usa interfaces COM.

En el diagrama siguiente se muestran los componentes usados para leer un archivo multimedia:

![diagrama que muestra los componentes para leer un archivo multimedia](images/concepts02.png)

La escritura de un archivo multimedia también requiere dos pasos:

1.  Codificación de los datos de audio y vídeo sin comprimir.
2.  Colocar los datos comprimidos en un formato de contenedor determinado.

En el diagrama siguiente se muestran los componentes usados para escribir un archivo multimedia:

![diagrama que muestra los componentes para escribir un archivo multimedia.](images/concepts03.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 



