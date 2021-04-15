---
description: En este tema se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea Guía de programación de Media Foundation.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Información general de la arquitectura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104555620"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Información general de la arquitectura de Media Foundation

En este tema se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea [Guía de programación de Media Foundation](media-foundation-programming-guide.md).

En el diagrama siguiente se muestra una vista de alto nivel de la arquitectura de Media Foundation.

![diagrama que muestra una vista de alto nivel de la arquitectura de Media Foundation.](images/mfarch01.png)

Media Foundation proporciona dos modelos de programación distintos. El primer modelo, que se muestra en el lado izquierdo del diagrama, utiliza una canalización de un extremo a otro para los datos multimedia. La aplicación inicializa la canalización (por ejemplo, proporcionando la dirección URL de un archivo que se va a reproducir) y, a continuación, llama a los métodos para controlar el streaming. En el segundo modelo, que se muestra en el lado derecho del diagrama, la aplicación extrae datos de un origen o los empuja a un destino (o ambos). Este modelo es especialmente útil si necesita procesar los datos, porque la aplicación tiene acceso directo al flujo de datos.

### <a name="primitives-and-platform"></a>Primitivas y plataforma

A partir de la parte inferior del diagrama, los *primitivos* son objetos auxiliares que se utilizan en la API de Media Foundation:

-   [Los atributos](attributes-and-properties.md) son una manera genérica de almacenar información dentro de un objeto, como una lista de pares clave-valor.
-   Los [tipos de medios](media-types.md) describen el formato de un flujo de datos multimedia.
-   Los [búferes multimedia](media-buffers.md) contienen fragmentos de datos multimedia, como fotogramas de vídeo y muestras de audio, y se usan para transportar datos entre objetos.
-   Los [ejemplos de medios](media-samples.md) son contenedores de búferes multimedia. También contienen metadatos acerca de los búferes, como las marcas de tiempo.

Las [API de Media Foundation Platform](media-foundation-platform-apis.md) proporcionan alguna funcionalidad básica que usa la canalización de Media Foundation, como las devoluciones de llamada asincrónicas y las colas de trabajos. Es posible que algunas aplicaciones necesiten llamar a estas API directamente; Además, los necesitará si implementa un origen, una transformación o un receptor personalizado para Media Foundation.

### <a name="media-pipeline"></a>Canalización multimedia

La canalización multimedia contiene tres tipos de objetos que generan o procesan datos multimedia:

-   Los [orígenes de medios](media-sources.md) introducen los datos en la canalización. Un origen multimedia puede obtener datos de un archivo local, como un archivo de vídeo. desde un flujo de red; o desde un dispositivo de captura de hardware.
-   [Media Foundation transformaciones](media-foundation-transforms.md) (MFTs) procesan datos de una secuencia. Los codificadores y descodificadores se implementan como MFTs.
-   Los [receptores de medios](media-sinks.md) consumen los datos; por ejemplo, mostrando vídeo en la pantalla, reproduciendo audio o escribiendo los datos en un archivo multimedia.

Los terceros pueden implementar sus propios orígenes personalizados, receptores y MFTs; por ejemplo, para admitir nuevos formatos de archivo multimedia.

La [sesión multimedia](media-session.md) controla el flujo de datos a través de la canalización y controla tareas como el control de calidad, la sincronización de audio y vídeo y la respuesta a los cambios de formato.

### <a name="source-reader-and-sink-writer"></a>Lector de origen y escritor de receptor

El [lector de origen](source-reader.md) y el [escritor de receptores](sink-writer.md) proporcionan una manera alternativa de usar los componentes de Media Foundation básicos (orígenes de medios, transformaciones y receptores multimedia). El lector de origen hospeda un origen de medios y cero o más descodificadores, mientras que el escritor de receptor hospeda un receptor de medios y cero o más codificadores. Puede usar el lector de origen para obtener datos comprimidos o sin comprimir de un origen multimedia y usar el escritor de receptores para codificar datos y enviarlos a un receptor de medios.

> [!Note]  
> El lector de origen y el escritor del receptor están disponibles en Windows 7.

 

Este modelo de programación proporciona a la aplicación más control sobre el flujo de datos y también proporciona a la aplicación acceso directo a los datos desde el origen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 



