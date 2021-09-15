---
description: En este tema se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre cómo usar Media Foundation tareas de programación específicas, vea Media Foundation Programming Guide(Guía de programación de aplicaciones).
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Introducción a la arquitectura Media Foundation de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0944eae1a74c1a5ba3dda8d94b69088128237f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474051"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Introducción a la arquitectura Media Foundation de datos

En este tema se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, [vea Media Foundation Programming Guide](media-foundation-programming-guide.md).

En el diagrama siguiente se muestra una vista de alto nivel de la Media Foundation arquitectura.

![diagrama que muestra una vista de alto nivel de la arquitectura de la base multimedia.](images/mfarch01.png)

Media Foundation proporciona dos modelos de programación distintos. El primer modelo, que se muestra en el lado izquierdo del diagrama, usa una canalización de un extremo a otro para los datos multimedia. La aplicación inicializa la canalización (por ejemplo, proporcionando la dirección URL de un archivo para reproducir) y, a continuación, llama a métodos para controlar el streaming. En el segundo modelo, que se muestra en el lado derecho del diagrama, la aplicación extrae datos de un origen o los inserta en un destino (o ambos). Este modelo es especialmente útil si necesita procesar los datos, ya que la aplicación tiene acceso directo al flujo de datos.

### <a name="primitives-and-platform"></a>Primitivas y plataforma

A partir de la parte inferior del diagrama, los *primitivos son* objetos auxiliares que se usan en Media Foundation API:

-   [Los](attributes-and-properties.md) atributos son una manera genérica de almacenar información dentro de un objeto, como una lista de pares clave-valor.
-   [Los tipos de](media-types.md) medios describen el formato de un flujo de datos multimedia.
-   [Los búferes multimedia](media-buffers.md) tienen fragmentos de datos multimedia, como fotogramas de vídeo y ejemplos de audio, y se usan para transportar datos entre objetos.
-   [Los ejemplos de medios](media-samples.md) son contenedores para búferes multimedia. También contienen metadatos sobre los búferes, como las marcas de tiempo.

Las [API Media Foundation Platform](media-foundation-platform-apis.md) proporcionan algunas funcionalidades principales que usa la canalización de Media Foundation, como las devoluciones de llamada asincrónicas y las colas de trabajo. Es posible que determinadas aplicaciones necesiten llamar a estas API directamente; además, los necesitará si implementa un origen, una transformación o un receptor personalizados para Media Foundation.

### <a name="media-pipeline"></a>Canalización de medios

La canalización de medios contiene tres tipos de objeto que generan o procesan datos multimedia:

-   [Los orígenes multimedia](media-sources.md) introducen datos en la canalización. Un origen multimedia podría obtener datos de un archivo local, como un archivo de vídeo. desde un flujo de red; o desde un dispositivo de captura de hardware.
-   [Media Foundation transformaciones](media-foundation-transforms.md) de datos (MFT) procesan datos de una secuencia. Los codificadores y descodificadores se implementan como MFT.
-   [Los receptores multimedia](media-sinks.md) consumen los datos; por ejemplo, mostrando vídeo en la pantalla, reproduciendo audio o escribiendo los datos en un archivo multimedia.

Terceros pueden implementar sus propios orígenes, receptores y MTA personalizados. por ejemplo, para admitir nuevos formatos de archivo multimedia.

La [sesión multimedia controla](media-session.md) el flujo de datos a través de la canalización y controla tareas como el control de calidad, la sincronización de audio y vídeo y la respuesta a los cambios de formato.

### <a name="source-reader-and-sink-writer"></a>Lector de origen y escritor de receptores

El [lector de origen](source-reader.md) y el escritor [de](sink-writer.md) receptores proporcionan una manera alternativa de usar los componentes de Media Foundation básicos (orígenes multimedia, transformaciones y receptores multimedia). El lector de origen hospeda un origen multimedia y cero o más descodificadores, mientras que el escritor receptor hospeda un receptor multimedia y cero o más codificadores. Puede usar el lector de origen para obtener datos comprimidos o descomprimidos de un origen multimedia y usar el sistema de escritura del receptor para codificar los datos y enviar los datos a un receptor multimedia.

> [!Note]  
> El lector de origen y el escritor de receptores están disponibles en Windows 7.

 

Este modelo de programación proporciona a la aplicación más control sobre el flujo de datos y también proporciona a la aplicación acceso directo a los datos desde el origen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation: conceptos esenciales](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 



