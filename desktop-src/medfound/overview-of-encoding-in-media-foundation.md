---
description: Este tema es una introducción a las API de codificación de archivos proporcionadas en Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Información general sobre la codificación en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474052"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Información general sobre la codificación en Media Foundation

Este tema es una introducción a las API de codificación de archivos proporcionadas en Microsoft Media Foundation.

## <a name="terminology"></a>Terminología

*La* codificación es un término general que abarca varios procesos distintos:

1.  Codificación de una secuencia de audio o vídeo en formatos comprimidos. Por ejemplo, codificar una secuencia de vídeo en vídeo H.264.
2.  Multiplexar ("muxing") una o varias secuencias en una sola secuencia de bytes. Normalmente, las secuencias entrantes se codifican primero. Este paso puede implicar la aplicación de paquetes a las secuencias codificadas.
3.  Escribir una secuencia de bytes multiplexada en un archivo, como un archivo MP4 o de formato de sistemas avanzados (ASF). Como alternativa, la secuencia multiplexada se puede enviar a través de la red.

En el diagrama siguiente se muestran estos tres procesos:

![diagrama que muestra los procesos de codificación y multiplexación](images/encoding03.png)

Las variaciones de este proceso incluyen transcodificación y reuxing:

-   *La transcodificación* significa descodificar un archivo existente, volver a codificar las secuencias y volver a multiplexar las secuencias codificadas. La transcodificación se puede realizar para convertir un archivo de un tipo de codificación a otro. por ejemplo, para convertir vídeo H.264 a Windows Media Video (WMV). También se puede hacer para cambiar la velocidad de bits codificada; el tamaño del fotograma de vídeo; la velocidad de fotogramas; u otros parámetros de formato.
-   *La remultiplexación* o *la* nueva experiencia significa desmultiplexar un archivo y volver a multiplexar las secuencias, sin ningún paso de descodificación o codificación. Esto puede hacerse para cambiar la forma en que se multiplexan los paquetes de audio y vídeo, para quitar una secuencia o para combinar secuencias de dos archivos de origen diferentes.
-   *La transratación* es un caso especial de transcodificación, donde la velocidad de bits cambia sin cambiar el tipo de compresión. Por ejemplo, puede convertir un archivo de velocidad de bits alta en una velocidad de bits inferior. Un escenario típico en el que se podría usar la transratación es al sincronizar contenido multimedia desde un equipo a un dispositivo portátil. Si el dispositivo portátil no admite una velocidad de bits alta, es posible que el archivo se transrate antes de copiarlo en el dispositivo portátil.

En el siguiente diagrama de bloques se muestra el proceso de transcodificación.

![diagrama que muestra el proceso de transcodificación](images/encoding05.png)

En el siguiente diagrama de bloques se muestra el proceso de reuxing.

![diagrama que muestra el proceso de reuxing](images/encoding06.png)

En esta documentación a veces se usa el término *codificación* para incluir la transcodificación y la reuxing. Cuando sea importante distinguirlos, la documentación tendrá en cuenta la diferencia.

Vea también: [Media Foundation: Conceptos esenciales](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Media Foundation de codificación

En la capa más baja de la Media Foundation, se usan los siguientes tipos de componente para la codificación:

-   Para la transcodificación, [los orígenes multimedia](media-sources.md) se usan para desmultiplexar el archivo de origen.
-   Para el proceso de [codificación, Media Foundation transformaciones](media-foundation-transforms.md) se usan para descodificar y codificar secuencias.
-   Para el proceso de [](media-sinks.md) multiplexación, los receptores multimedia se usan para multiplexar las secuencias y escribir la secuencia multiplexada en un archivo o red.

En el diagrama siguiente se muestra el flujo de datos entre estos componentes en un escenario de transcodificación:

![diagrama que muestra los componentes usados en la transcodificación](images/encoding04.png)

La mayoría de las aplicaciones no usarán estos componentes directamente. En su lugar, una aplicación usará API de nivel superior que administran estos componentes de nivel inferior. Media Foundation proporciona dos API de nivel superior para la codificación:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sesión multimedia](media-session.md)
</dt> <dd>

La sesión multimedia proporciona una canalización de un extremo a otro que mueve los datos desde el origen multimedia, a través de los códecs y, por último, al receptor multimedia. La aplicación controla la sesión multimedia y recibe eventos de estado de la sesión multimedia.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Lector de origen](source-reader.md) más [escritor receptor](sink-writer.md)
</dt> <dd>

El Lector de origen ajusta el origen multimedia y, opcionalmente, los descodificadores. Proporciona ejemplos codificados o descodificados de la aplicación. Sink Writer encapsula el receptor multimedia y, opcionalmente, los codificadores. La aplicación pasa ejemplos al escritor de receptores.

</dd> </dl>

En el diagrama siguiente se muestra la sesión multimedia:

![diagrama que muestra cómo realiza la transcodificación la sesión multimedia](images/encoding01.png)

[Transcode API](transcode-api.md) (el cuadro sombreado azul) es un conjunto de API introducidas en Windows 7, que facilitan la configuración de la sesión multimedia para la codificación.

En el diagrama siguiente se muestran el lector de origen y el escritor de receptores:

![diagrama que muestra la transcodificación con el lector de origen y el escritor de receptores](images/encoding02.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación y creación de archivos](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation programación: Conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



