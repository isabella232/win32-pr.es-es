---
description: X3DAudio es una API que se usa con XAudio2 para colocar sonido en el espacio 3D con el fin de crear la ilusión de sonido que provienen de un punto en el espacio con respecto a la posición de la cámara.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Información general de X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff509b16556ee1932d2a2543ad5008ddcbaa5b92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669869"
---
# <a name="x3daudio-overview"></a>Información general de X3DAudio

X3DAudio es una API que se usa con [XAudio2](programming-guide.md) para colocar sonido en el espacio 3D con el fin de crear la ilusión de sonido que provienen de un punto en el espacio con respecto a la posición de la cámara. En concreto, los títulos que incluyen escenas 3D querrán usar X3DAudio. Los sonidos que no requieren el posicionamiento 3D, como las bandas sonoras o los sonidos ambientales no posicionados, pueden omitir por completo X3DAudio.

## <a name="listeners-and-emitters"></a>Agentes de escucha y emisores

Para administrar sonidos en el espacio 3D, X3DAudio emplea los conceptos de *agentes de escucha* y *emisores*. Los agentes de escucha y los emisores representan la posición de lo que está escuchando sonidos 3D y el punto desde el que se originan esos sonidos.

-   Un agente de escucha se define como un punto en el espacio y una orientación. Es la posición en la que se *oye* el sonido. La posición y la orientación del agente de escucha suelen ser las mismas que la posición y la orientación de la cámara. Esto es cierto si un título usa una vista de perspectiva de primera persona o de tercera persona. La posición del agente de escucha se expresa en coordenadas universales. Es importante tener en cuenta que es la posición del agente de escucha *con respecto* a un emisor que determina cómo calcular los volúmenes del altavoz final.
-   Un emisor se define como uno o más puntos en el espacio desde el que se *origina* un sonido. La posición del emisor puede estar en cualquier lugar en el espacio 3D. Al igual que un agente de escucha, la posición de un emisor se expresa en coordenadas universales. Es la posición del emisor en *relación* con el agente de escucha que determina cómo se calculan los volúmenes del altavoz final.
-   X3DAudio usa coordenadas de la izquierda. Para usar con coordenadas a la derecha, los desarrolladores deben negar el elemento. z de los miembros OrientTop, OrientFront, Position y Velocity de X3DAUDIO \_ Listener y X3DAUDIO \_ emisor.

Además de la posición, los agentes de escucha y los emisores pueden incluir la velocidad. A diferencia de un motor de representación en 3D, X3DAudio solo usa Velocity para calcular los efectos de Doppler (no se usa para calcular la posición).

Para obtener más información acerca de los agentes de escucha y los emisores, consulte los temas de referencia de la estructura [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) y [**X3DAUDIO \_ emisor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

## <a name="using-x3daudio-with-xaudio2"></a>Uso de X3DAudio con XAudio2

Para todas las interacciones entre X3DAudio y XAudio2, use las siguientes funciones de X3DAudio.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Llame a la función [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) para inicializar X3DAudio. Normalmente, solo necesita llamar a **X3DAudioInitialize** una vez en la duración de un juego, a menos que se cambie la configuración de los altavoces.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Después de inicializar X3DAudio, puede determinar el volumen y otros valores para un sonido determinado pasando el emisor del sonido y el agente de escucha a la función [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) . Los valores calculados por **X3DAudioCalculate** se pueden aplicar a las voces o efectos de XAudio2 según corresponda para las marcas que se pasan a la función. Puede aplicar valores de volumen y de paso calculados por X3DAudio a una voz con los métodos [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) y [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) . Otros valores calculados por X3DAudio deberán aplicarse a un [**efecto de reverberación**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) mediante el método [**IXAudio2Voice:: SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) .

Para obtener un ejemplo paso a paso del uso de X3DAudio con XAudio2, consulte [Cómo: integrar X3DAudio con XAudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
