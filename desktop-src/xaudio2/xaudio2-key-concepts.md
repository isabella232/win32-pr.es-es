---
description: En esta información general se presentan algunos conceptos clave para usar XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Conceptos clave de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720714"
---
# <a name="xaudio2-key-concepts"></a>Conceptos clave de XAudio2

En esta información general se presentan algunos conceptos clave para usar XAudio2.

-   [Motor de XAudio2](#xaudio2-engine)
-   [Voces](#voices)
-   [Gráfico de audio](#audio-graph)
-   [Devoluciones de llamada](#callbacks)
-   [Temas relacionados](#related-topics)

## <a name="xaudio2-engine"></a>Motor de XAudio2

La interfaz [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) es el núcleo del motor XAudio2. La creación de una instancia de la interfaz **IXAudio2** permite al cliente enumerar los dispositivos de audio disponibles, configurar las propiedades globales de la API, crear voces y supervisar el rendimiento. La función auxiliar [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) realiza las tareas de creación de instancias e inicialización de XAudio2.

Puede crear instancias de XAudio2 varias veces en un único proceso. Cada objeto XAudio2 funciona de forma independiente y tiene su propio subproceso de procesamiento de audio. Solo se comparten los valores de Debug. Esto es importante en Windows, donde pueden cargarse varios componentes diferentes en un único proceso. Por ejemplo, Internet Explorer podría usar varios componentes de XAudio2 simultáneamente. Aunque es posible crear varios objetos del motor de XAudio2 en una sola aplicación cliente, no se debe pasar información entre sus respectivos gráficos.

Para obtener un ejemplo de cómo inicializar el motor de XAudio2, consulte [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md).

## <a name="voices"></a>Voces

Las voces son los objetos que usa XAudio2 para procesar, manipular y reproducir datos de audio. Hay tres tipos de voces en XAudio2.

-   [**Voces de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    Las voces de origen representan un flujo de datos de audio. Las voces de origen envían sus datos a otros tipos de voces.

-   [**Voces de submezcla**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    Las voces de submezcla realizan alguna manipulación de los datos de audio que reciben. Un ejemplo de manipulación de datos de audio podría ser la conversión de la frecuencia de muestreo. Después de que una voz de submezcla procese los datos, los pasa a otra voz de submezcla o a una voz maestra.

-   [**Voces de mastering**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    Las voces de Master reciben datos de voces de origen y voces de submezcla, y envían los datos al hardware de audio.

Consulte las [voces de xaudio2](voices.md) para obtener información general sobre las voces de xaudio2.

## <a name="audio-graph"></a>Gráfico de audio

Un gráfico de audio es una colección de voces de XAudio2. El audio se inicia en un lado de un gráfico de audio en las voces de origen y, opcionalmente, pasa a través de una o más voces de la mezcla y finaliza en una voz de la maestra. Un gráfico de audio contendrá una voz de origen para cada sonido que se reproduce actualmente, cero o más voces de submezcla y una voz de maestro. El gráfico de audio más sencillo, y el mínimo necesario para crear un ruido en XAudio2, es una voz de origen única que se envía directamente a una voz de mastering. Consulte [Cómo: reproducir un sonido con xaudio2](how-to--play-a-sound-with-xaudio2.md) para ver un ejemplo de los pasos mínimos necesarios para reproducir un sonido con xaudio2.

Consulte [gráfico de audio de xaudio2](audio-graphs.md) para obtener información general sobre los gráficos de audio de xaudio2.

## <a name="callbacks"></a>Devoluciones de llamada

Las devoluciones de llamada son el mecanismo que usa XAudio2 para indicar al código de cliente que se ha producido algún evento en una voz o en el objeto de motor. Dado que la reproducción de audio es asincrónica en el motor de XAudio2, las devoluciones de llamada proporcionan la única manera de determinar cuándo finaliza la reproducción de un sonido.

Consulte [devoluciones de llamada de xaudio2](callbacks.md) para obtener información general sobre las devoluciones de llamada de xaudio2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Versiones de XAudio2](xaudio2-versions.md)
</dt> <dt>

[Cómo: inicializar XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Cómo: reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



