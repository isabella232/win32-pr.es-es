---
description: En este tema se ofrece información general sobre las API de codificación de archivos que se proporcionan en Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Información general de la codificación en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104552529"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Información general de la codificación en Media Foundation

En este tema se ofrece información general sobre las API de codificación de archivos que se proporcionan en Microsoft Media Foundation.

## <a name="terminology"></a>Terminología

La *codificación* es un término general que abarca varios procesos distintos:

1.  Codificar una secuencia de audio o vídeo en formatos comprimidos. Por ejemplo, codificar una secuencia de vídeo en un vídeo H. 264.
2.  Multiplexación ("Multiplexación") uno o más flujos en una sola secuencia de bytes. Normalmente, los flujos entrantes se codifican en primer lugar. Este paso puede implicar la packetabilidad de las secuencias codificadas.
3.  Escritura de una secuencia de bytes multiplexada en un archivo, como un archivo MP4 o Advanced Systems Format (ASF). Como alternativa, la secuencia multiplexada se puede enviar a través de la red.

En el diagrama siguiente se muestran estos tres procesos:

![diagrama que muestra los procesos de codificación y multiplexación](images/encoding03.png)

Entre las variaciones de este proceso se incluyen transcodificación y remuxing:

-   La *transcodificación* significa descodificar un archivo existente, volver a codificar los flujos y volver a multiplexar las secuencias codificadas. La transcodificación puede realizarse para convertir un archivo de un tipo de codificación a otro; por ejemplo, para convertir el vídeo H. 264 en Windows Media Video (WMV). También se puede hacer para cambiar la velocidad de bits codificada; tamaño del fotograma de vídeo; la velocidad de fotogramas; u otros parámetros de formato.
-   *Remultiplexar* o *remuxing* significa desmultiplexar un archivo y volver a multiplexar los flujos, sin ningún paso de descodificación/codificación. Esto puede hacerse para cambiar el modo en que los paquetes de audio y vídeo se multiplexan, para quitar una secuencia o para combinar secuencias de dos archivos de origen diferentes.
-   *Transclasificación* es un caso especial de transcodificación, donde se cambia la velocidad de bits sin cambiar el tipo de compresión. Por ejemplo, puede convertir un archivo de velocidad de bits alto en una velocidad de bits inferior. Un escenario típico en el que se podría usar la transclasificación es al sincronizar contenido multimedia desde un equipo a un dispositivo portátil. Si el dispositivo portátil no es compatible con una velocidad de bits alta, el archivo se puede transclasificar antes de copiarlo en el dispositivo portátil.

El siguiente diagrama de bloque muestra el proceso de transcodificación.

![diagrama que muestra el proceso de transcodificación](images/encoding05.png)

El siguiente diagrama de bloque muestra el proceso remuxing.

![diagrama que muestra el proceso remuxing](images/encoding06.png)

En ocasiones, en esta documentación se usa la *codificación* de términos para incluir transcodificación y remuxing. Cuando sea importante distinguir entre ellos, la documentación indicará la diferencia.

Vea también: [Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Arquitectura de codificación de Media Foundation

En el nivel más bajo de la arquitectura de Media Foundation, se usan los siguientes tipos de componente para la codificación:

-   Para la transcodificación, los [orígenes multimedia](media-sources.md) se usan para desmultiplexar el archivo de código fuente.
-   En el proceso de codificación, se usan [Media Foundation transformaciones](media-foundation-transforms.md) para descodificar y codificar secuencias.
-   En el proceso de multiplexación, los [receptores de medios](media-sinks.md) se usan para multiplexar los flujos y escribir la secuencia multiplexada en un archivo o una red.

En el siguiente diagrama se muestra el flujo de datos entre estos componentes en un escenario de transcodificación:

![diagrama que muestra los componentes usados en la transcodificación](images/encoding04.png)

La mayoría de las aplicaciones no usarán estos componentes directamente. En su lugar, una aplicación usará API de nivel superior que administren estos componentes de nivel inferior. Media Foundation proporciona dos API de nivel superior para la codificación:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sesión de medios](media-session.md)
</dt> <dd>

La sesión multimedia proporciona una canalización de un extremo a otro que mueve los datos desde el origen de medios, a través de los códecs y, por último, al receptor de medios. La aplicación controla la sesión multimedia y recibe los eventos de estado de la sesión de medios.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Lector de origen](source-reader.md) más [escritor de receptor](sink-writer.md)
</dt> <dd>

El lector de origen ajusta el origen de medios y, opcionalmente, los descodificadores. Proporciona ejemplos codificados o descodificados en la aplicación. El escritor del receptor incluye el receptor de medios y, opcionalmente, los codificadores. La aplicación pasa ejemplos al escritor del receptor.

</dd> </dl>

En el diagrama siguiente se muestra la sesión multimedia:

![diagrama que muestra cómo la sesión multimedia realiza la transcodificación](images/encoding01.png)

La [API de Transcode](transcode-api.md) (el cuadro sombreado azul) es un conjunto de API incorporadas en Windows 7, que facilitan la configuración de la sesión multimedia para la codificación.

En el diagrama siguiente se muestra el lector de origen y el escritor del receptor:

![diagrama que muestra la transcodificación con el lector de origen y el escritor del receptor](images/encoding02.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación y creación de archivos](encoding-and-file-authoring.md)
</dt> <dt>

[Programación de Media Foundation: conceptos básicos](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



