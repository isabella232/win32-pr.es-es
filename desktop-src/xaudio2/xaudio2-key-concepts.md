---
description: En esta introducción se presentan algunos conceptos clave para usar XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Conceptos clave de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff11399d30d21ed8c602d26d1d5574231943729b155d4eb0d0e4e85f8f92bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082839"
---
# <a name="xaudio2-key-concepts"></a>Conceptos clave de XAudio2

En esta introducción se presentan algunos conceptos clave para usar XAudio2.

-   [Motor XAudio2](#xaudio2-engine)
-   [Voces](#voices)
-   [Audio Graph](#audio-graph)
-   [Devoluciones de llamada](#callbacks)
-   [Temas relacionados](#related-topics)

## <a name="xaudio2-engine"></a>Motor XAudio2

La interfaz [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) es el núcleo del motor XAudio2. La creación de una instancia de la interfaz **IXAudio2** permite al cliente enumerar los dispositivos de audio disponibles, configurar propiedades de API globales, crear voces y supervisar el rendimiento. La [**función auxiliar XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) realiza tareas de creación de instancias e inicialización para XAudio2.

Puede crear instancias de XAudio2 varias veces dentro de un único proceso. Cada objeto XAudio2 funciona de forma independiente y tiene su propio subproceso de procesamiento de audio. Solo se comparte la configuración de depuración. Esto es importante en Windows donde se pueden cargar varios componentes diferentes en un único proceso. Por ejemplo, Internet Explorer usar varios componentes XAudio2 simultáneamente. Aunque es posible crear varios objetos de motor XAudio2 dentro de una sola aplicación cliente, no debe pasar información entre sus gráficos respectivos.

Para obtener un ejemplo de inicialización del motor XAudio2, [vea Cómo: Inicializar XAudio2.](how-to--initialize-xaudio2.md)

## <a name="voices"></a>Voces

Las voces son los objetos que XAudio2 usa para procesar, manipular y reproducir datos de audio. Hay tres tipos de voces en XAudio2.

-   [**Voces de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    Las voces de origen representan un flujo de datos de audio. Las voces de origen envían sus datos a otros tipos de voces.

-   [**Submezcla voces**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    Las voces de submezcla realizan alguna manipulación de los datos de audio que reciben. Un ejemplo de manipulación de datos de audio podría ser la conversión de frecuencia de muestreo. Una vez que una voz de submezcla procesa los datos, los pasa a otra voz de submezcla o a una voz maestra.

-   [**Mastering Voices**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    Las voces maestras reciben datos de voces de origen y voces de submezcla, y los envían al hardware de audio.

Consulte [XAudio2 Voices (Voces de XAudio2)](voices.md) para obtener información general sobre las voces XAudio2.

## <a name="audio-graph"></a>Audio Graph

Un gráfico de audio es una colección de voces XAudio2. El audio comienza en un lado de un gráfico de audio en las voces de origen, opcionalmente pasa a través de una o varias voces de submezcla y termina en una voz maestra. Un gráfico de audio contendrá una voz de origen para cada sonido que se esté reproduciendo actualmente, cero o más voces de submezcla y una voz maestra. El gráfico de audio más sencillo y el mínimo necesario para hacer ruido en XAudio2 es una única voz de origen que se genera directamente a una voz maestra. Consulte [Cómo: Reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md) para obtener un ejemplo de los pasos mínimos necesarios para reproducir un sonido con XAudio2.

Consulte [XAudio2 Audio Graph](audio-graphs.md) para obtener información general sobre los gráficos de audio XAudio2.

## <a name="callbacks"></a>Devoluciones de llamada

Las devoluciones de llamada son el mecanismo que XAudio2 usa para indicar al código de cliente que se ha producido algún evento en una voz o en el objeto del motor. Dado que la reproducción de audio es asincrónica en el motor XAudio2, las devoluciones de llamada proporcionan la única manera de determinar cuándo termina de reproducirse un sonido.

Consulte [Devoluciones de llamada de XAudio2 para](callbacks.md) obtener información general sobre las devoluciones de llamada de XAudio2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Versiones de XAudio2](xaudio2-versions.md)
</dt> <dt>

[Cómo: inicializar XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Cómo: Reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



