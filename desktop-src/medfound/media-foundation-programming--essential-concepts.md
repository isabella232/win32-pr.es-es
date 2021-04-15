---
description: Si no está familiarizado con los medios digitales, en este tema se presentan algunos conceptos que debe conocer antes de escribir una aplicación Media Foundation.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: conceptos esenciales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0298a20518df91dab4439770e0f1193802969ae8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424111"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: conceptos esenciales

Si no está familiarizado con los medios digitales, en este tema se presentan algunos conceptos que debe conocer antes de escribir una aplicación Media Foundation.

-   [Secuencias](#streams)
-   [Compresión](#compression)
-   [Contenedores de medios](#media-containers)
-   [Formatos](#formats)
-   [Temas relacionados](#related-topics)

## <a name="streams"></a>Secuencias

Una *secuencia* es una secuencia de datos multimedia con un tipo uniforme. Los tipos más comunes son audio y vídeo, pero un flujo puede contener casi cualquier tipo de datos, incluidos texto, comandos de script y imágenes fijas. La *secuencia* de términos de esta documentación no implica la entrega a través de una red. Un archivo multimedia diseñado para la reproducción local también contiene secuencias.

Normalmente, un archivo multimedia contiene una sola secuencia de audio o exactamente una secuencia de vídeo y una secuencia de audio. Sin embargo, un archivo multimedia podría contener varios flujos del mismo tipo. Por ejemplo, un archivo de vídeo puede contener secuencias de audio en varios idiomas distintos. En tiempo de ejecución, la aplicación seleccionaría la secuencia que se va a usar.

## <a name="compression"></a>Compresión

La *compresión* hace referencia a cualquier proceso que reduzca el tamaño de un flujo de datos mediante la eliminación de información redundante. Los algoritmos de compresión se dividen en dos amplias categorías:

-   Compresión sin *pérdida* . Con un algoritmo sin pérdida, los datos reconstruidos son idénticos a los originales.
-   Compresión de *pérdida* . Con un algoritmo de pérdida, los datos reconstruidos son una aproximación del original, pero no es una coincidencia exacta.

En la mayoría de los demás dominios, la compresión con pérdida no es aceptable. (Imagínese obtener una "aproximación" de una hoja de cálculo) Sin embargo, los esquemas de compresión con pérdida son adecuados para audio y vídeo, por un par de razones.

La primera razón tiene que hacer con la física de la percepción humana. Cuando escuchamos un sonido complejo, como una grabación de música, parte de la información contenida en ese sonido no es perceptible a la lengüeta. Con la ayuda de la teoría del procesamiento de señales, es posible analizar y separar las frecuencias que no se pueden percibir. Estas frecuencias se pueden quitar sin ningún efecto perceptual. Aunque el audio reconstruido no coincidirá exactamente con el original, *sonará* igual al agente de escucha. Se aplican principios similares al vídeo.

En segundo lugar, es posible que se produzca una degradación de la calidad de imagen o sonido, según el propósito previsto. Por ejemplo, en telefonía, el audio suele ser muy comprimido. El resultado es lo suficientemente bueno para una conversación telefónica, pero no desearía escuchar una orquestación de Symphony a través de un teléfono.

La compresión también se denomina *codificación* y un dispositivo que codifica se denomina *codificador*. El proceso inverso se está *descodificando* y el dispositivo es un *descodificador* que se denomina de forma natural. El término general para ambos codificadores y descodificadores es *codec*. Los códecs se pueden implementar en hardware o software.

La tecnología de compresión ha cambiado rápidamente desde la llegada de los medios digitales y actualmente se usa un gran número de esquemas de compresión. Este hecho es uno de los principales desafíos de la programación multimedia digital.

## <a name="media-containers"></a>Contenedores de medios

No es raro almacenar una secuencia de audio o de vídeo sin procesar como un archivo de equipo o enviar una directamente a través de la red. Por un lado, sería imposible descodificar este tipo de flujo, sin conocer por adelantado el códec que se va a usar. Por lo tanto, los archivos multimedia normalmente contienen al menos algunos de los siguientes elementos:

-   Encabezados de archivo que describen el número de flujos, el formato de cada flujo, etc.
-   Índice que permite el acceso aleatorio al contenido.
-   Metadatos que describen el contenido (por ejemplo, el artista o el título).
-   Encabezados de paquetes, para habilitar la transmisión de red o el acceso aleatorio.

En esta documentación se usa el término *contenedor* para describir todo el paquete de secuencias, encabezados, índices, metadatos, etc. La razón para usar el término *contenedor* en lugar de un *archivo* es que algunos formatos de contenedor están diseñados para la difusión en directo. Una aplicación podría generar el contenedor en tiempo real, nunca almacenarlo en un archivo.

Un ejemplo temprano de un contenedor multimedia es el formato de archivo AVI. Otros ejemplos incluyen MP4 y Advanced Systems Format (ASF). Los contenedores se pueden identificar por extensión de nombre de archivo (por ejemplo,. mp4) o por tipo MIME.

En el diagrama siguiente se muestra una estructura típica para un contenedor de medios. El diagrama no representa ningún formato específico; los detalles de cada formato varían considerablemente.

![diagrama que muestra un contenedor multimedia típico](images/concepts01.png)

Observe que la estructura que se muestra en el diagrama es jerárquica, con información de encabezado que aparece al principio del contenedor. Esta estructura es típica de muchos formatos de contenedor (pero no todos). Observe también que la sección de datos contiene paquetes de audio y vídeo intercalados. Este tipo de intercalación es común en los contenedores de multimedia.

El término *multiplexación* se refiere al proceso de paquetes de secuencias de audio y vídeo y la intercalación de los paquetes en el contenedor. El proceso inverso, el reensamblado de los flujos de datos de paquetes, se denomina *demultiplexación*.

## <a name="formats"></a>Formatos

En los medios digitales, el *formato* del término es ambiguo. Un formato puede hacer referencia al tipo de *codificación*, como el vídeo H. 264 o el *contenedor*, como MP4. Esta distinción suele ser confusa para los usuarios normales. Los nombres asignados a formatos multimedia no siempre son de ayuda. Por ejemplo, *mp3* hace referencia a un formato de codificación (nivel 3 de audio MPEG-1) y a un formato de archivo.

Sin embargo, la distinción es importante, ya que la lectura de un archivo multimedia implica realmente dos fases:

1.  En primer lugar, se debe analizar el contenedor. En la mayoría de los casos, no se puede conocer el número de flujos y el formato de cada flujo hasta que se complete este paso.
2.  Después, si las secuencias están comprimidas, deben descodificarse mediante los descodificadores adecuados.

Este hecho conduce de forma bastante natural a un diseño de software en el que se usan componentes independientes para analizar contenedores y descodificar flujos. Además, este enfoque se presta a un modelo de complemento, por lo que los terceros pueden proporcionar sus propios analizadores y códecs. En Windows, el modelo de objetos componentes (COM) proporciona una manera estándar de separar una API de su implementación, que es un requisito para cualquier modelo de complemento. Por esta razón (entre otras), Media Foundation usa interfaces COM.

En el diagrama siguiente se muestran los componentes que se usan para leer un archivo multimedia:

![diagrama que muestra los componentes para leer un archivo multimedia](images/concepts02.png)

La escritura de un archivo multimedia también requiere dos pasos:

1.  Codificar los datos de audio y vídeo sin comprimir.
2.  Colocar los datos comprimidos en un formato de contenedor determinado.

En el diagrama siguiente se muestran los componentes que se usan para escribir un archivo multimedia:

![diagrama que muestra los componentes para escribir un archivo multimedia.](images/concepts03.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 



