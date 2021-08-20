---
description: X3DAudio es una API que se usa con XAudio2 para colocar el sonido en el espacio 3D para crear la sensación de sonido procedente de un punto en el espacio en relación con la posición de la cámara.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Información general sobre X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb39239027bf8c7387fbe4cb25b80cef88bb241b74facf0b7bd7ee35c77965b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962554"
---
# <a name="x3daudio-overview"></a>Información general sobre X3DAudio

X3DAudio es una API que se usa con [XAudio2](programming-guide.md) para colocar el sonido en el espacio 3D para crear la sensación de sonido procedente de un punto en el espacio en relación con la posición de la cámara. En concreto, los títulos que incluyen escenas 3D querrán usar X3DAudio. Los sonidos que no requieren posicionamiento 3D, como sonidos de sonido ambiental no posicionados, pueden omitir X3DAudio por completo.

## <a name="listeners-and-emitters"></a>Agentes de escucha y emisores

Para administrar sonidos en espacio 3D, X3DAudio emplea los *conceptos* de agentes de escucha *y emisores.* Los agentes de escucha y emisores representan la posición de lo que escucha sonidos 3D y el punto desde el que se originan esos sonidos.

-   Un agente de escucha se define como un punto en el espacio y una orientación. Es la posición en la que se escucha el *sonido.* La posición y orientación del agente de escucha suele ser la misma que la posición y la orientación de la cámara. Esto es así si un título usa una vista de perspectiva de primera persona o de tercera persona. La posición del agente de escucha se expresa en coordenadas globales. Es importante tener en cuenta que es  la posición del agente de escucha con respecto a un emisor la que determina cómo calcular los volúmenes finales del hablante.
-   Un emisor se define como uno (o más) puntos en el espacio desde los que se *origina un sonido.* La posición del emisor puede estar en cualquier lugar del espacio 3D. Al igual que un agente de escucha, la posición de un emisor se expresa en coordenadas globales. Es la posición del  emisor con respecto al agente de escucha la que determina cómo se calculan los volúmenes finales del hablante.
-   X3DAudio usa coordenadas a la izquierda. Para usar con coordenadas de mano derecha, los desarrolladores deben negar el elemento .z de los miembros OrientTop, OrientFront, Position y Velocity de X3DAUDIO LISTENER y \_ X3DAUDIO \_ EMITTER.

Además de la posición, los agentes de escucha y emisores pueden incluir velocidad. A diferencia de un motor de representación 3D, X3DAudio solo usa la velocidad para calcular los efectos de Doppler (no se usa para calcular la posición).

Para más información sobre los agentes de escucha y emisores, consulte los temas de referencia sobre la estructura [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) y [**X3DAUDIO \_ EMITTER.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

## <a name="using-x3daudio-with-xaudio2"></a>Uso de X3DAudio con XAudio2

Para toda la interacción entre X3DAudio y XAudio2, use las siguientes funciones X3DAudio.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Llame a [**la función X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) para inicializar X3DAudio. Normalmente, solo es necesario llamar a **X3DAudioInitialize** una vez en la duración de un juego, a menos que se cambie la configuración del hablante.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Después de inicializar X3DAudio, puede determinar el volumen y otros valores de un sonido determinado pasando el emisor del sonido y el agente de escucha a la función [**X3DAudioCalculate.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) Los valores calculados por **X3DAudioCalculate** se pueden aplicar a voces o efectos de XAudio2 según corresponda para las marcas que se pasan a la función. Puede aplicar valores de volumen y tono calculados por X3DAudio a una voz con los métodos [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice::SetFrequencyRatio.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) Otros valores calculados por X3DAudio tendrán que aplicarse a un [**efecto de reverberación**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) mediante el método [**IXAudio2Voice::SetEffectParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)

Para obtener un ejemplo paso a paso del uso de X3DAudio con XAudio2, consulte Integración de [X3DAudio con XAudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
