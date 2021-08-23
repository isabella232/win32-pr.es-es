---
description: Controles de volumen de sesión
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Controles de volumen de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe45dce825dedd116c8f9c65684ac665eb6483f95dec3d247071f66408e8ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758895"
---
# <a name="session-volume-controls"></a>Controles de volumen de sesión

Como se explicó anteriormente, los clientes WASAPI pueden controlar individualmente el nivel de volumen de cada [sesión de audio.](audio-sessions.md) WASAPI aplica la configuración del volumen de una sesión de forma uniforme a todas las secuencias de la sesión. Cada nivel de volumen es un valor en el intervalo de 0,0 a 1,0, donde 0,0 indica silencio y 1,0 indica volumen completo (sin atenuación).

Un cliente crea implícitamente una sesión asignando la primera secuencia a esa sesión. El nivel de volumen predeterminado de la nueva sesión es 1.0. Como se ha comentado anteriormente, el usuario puede ajustar el nivel de volumen de la sesión a través de la interfaz de usuario de un programa de control (por ejemplo, Sndvol) que es un cliente WASAPI. La configuración del control es persistente.

Además de la configuración del volumen controlado por el cliente, el sistema aplica su propia configuración de volumen a las sesiones. Esta configuración se basa en la directiva de audio y cambia dinámicamente en respuesta a los cambios en las secuencias que la mezcla de audio global. Para obtener más información sobre la directiva de audio, vea [Componentes de audio en modo de usuario](user-mode-audio-components.md).

El software del sistema que implementa el control de volumen para cada secuencia multiplica los ejemplos de PCM de la secuencia por el nivel de volumen efectivo. El nivel de volumen efectivo es el resultado de multiplicar la configuración del volumen del cliente y del sistema. Por lo tanto, el cambio resultante en la amplitud de señal es una combinación lineal de los niveles de volumen del cliente y del sistema. Por ejemplo, si el nivel de volumen de cliente es 0,8 y el nivel de volumen del<sup></sup> sistema es 0,5, el nivel de volumen efectivo es (0,8). (0,5) = 0,4.

Tenga en cuenta que la sonoridad percibida no es lineal con respecto a la amplitud de señal. En su lugar, la sonoridad varía aproximadamente como el logaritmo del nivel de volumen v:

sonoridad en decibelios = 20<sup>.</sup> log₁₀(v)

Por lo tanto, al establecer v = 0,5 se atenua la sonoridad de la señal original (la señal antes de aplicar el nivel de volumen) por 6 decibelios, al establecer v = 0,25 se atenua la señal en 12 decibelios, y así sucesivamente. Un nivel de volumen v = 1,0, correspondiente a 0 decibelios, no modifica el nivel de señal original.

Las aplicaciones de audio con interfaces de usuario para controlar el nivel de volumen suelen mostrar controles deslizantes que generan cambios en la sonoridad percibida que son linealmente proporcionales a los cambios en la posición del control deslizante. Para generar una relación lineal entre la sonoridad percibida y la posición del control deslizante, la aplicación debe definir una relación no lineal entre el nivel de volumen v y la posición del control deslizante. Para obtener más información, vea [Audio-Tapered Volume Controls](audio-tapered-volume-controls.md).

Como se explicó anteriormente, el programa de control de volumen del sistema, Sndvol, muestra controles deslizantes de volumen para las sesiones de audio que se reproducen en cada dispositivo de representación de audio. Estos controles deslizantes aparecen en el cuadro de grupo con la etiqueta **Aplicaciones** en la ventana SndVol. Normalmente, cada sesión contiene todas las secuencias de reproducción de una ventana de aplicación determinada. A través de los controles deslizantes de la ventana Sndvol, los usuarios controlan los niveles de volumen de las aplicaciones de audio individuales.

Como regla general, una aplicación debe asignar todas sus secuencias de reproducción a la misma sesión de audio. WASAPI no impide que una aplicación distribua sus secuencias de reproducción entre varias sesiones. Sin embargo, la proliferación resultante de controles deslizantes de volumen en Sndvol podría confundir a los usuarios.

Como opción, una ventana de aplicación puede mostrar un control deslizante de volumen. El control deslizante de la aplicación debe reflejar el estado del control deslizante de Sndvol correspondiente en todo momento. Por lo tanto, si el usuario cambia el nivel de volumen moviendo el control deslizante en la ventana de la aplicación, el control deslizante correspondiente de la ventana Sndvol debe moverse al unísono con el control deslizante de la aplicación. De forma similar, si el usuario mueve el control deslizante de Sndvol, el control deslizante de la aplicación debe moverse al unísono con el control deslizante de Sndvol.

Para admitir este comportamiento, WASAPI implementa la [**interfaz ISimpleAudioVolume.**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) Cuando el usuario mueve el control deslizante de la aplicación, la aplicación llama al método [**ISimpleAudioVolume::SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) para ajustar el nivel de volumen de sesión en consecuencia. Sndvol supervisa los cambios de volumen realizados a través de este método y refleja los cambios en los controles deslizantes de volumen que muestra. Además, una aplicación puede recibir notificaciones de los cambios de volumen de sesión que el usuario realiza a través de Sndvol. Para ello, la aplicación implementa una [**interfaz IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y registra la interfaz con WASAPI. A partir de entonces, cada vez que el usuario cambia el nivel de volumen de sesión a través de Sndvol, la aplicación recibe una llamada de notificación a través del método [**IAudioSessionEvents::OnSimpleVolumeChanged.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) Para obtener un ejemplo de código que implementa una **interfaz IAudioSessionEvents,** vea [Eventos de sesión de audio](audio-session-events.md). Para obtener un ejemplo de código que registra una **interfaz IAudioSessionEvents,** vea Eventos de [audio para aplicaciones de audio heredadas.](audio-events-for-legacy-audio-applications.md)

La **interfaz ISimpleAudioVolume** aplica el mismo nivel de volumen uniformemente a todos los canales de una sesión de audio. Aunque esta interfaz debe satisfacer los requisitos de control de volumen de la mayoría de las aplicaciones, es posible que algunas aplicaciones requieran funcionalidades de control de volumen más especializadas. La [**interfaz IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) controla el volumen de una secuencia individual en una sesión con respecto a las demás secuencias de la sesión. **IAudioStreamVolume** también permite a un cliente controlar individualmente los niveles de volumen de todos los canales de la secuencia. Por ejemplo, una aplicación podría usar esta funcionalidad para lograr efectos de audio, como simular el movimiento espacial de un origen de audio al realizar un movimiento panorámico de izquierda a derecha. Otra interfaz especializada, [**IChannelAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)controla los niveles de volumen de los canales individuales de una sesión. Por ejemplo, una aplicación podría usar **IChannelAudioVolume** para implementar controles de equilibrio para un sistema de sonido estereofónico.

Los controles deslizantes de volumen del cuadro **Aplicaciones** de Sndvol reflejan solo los cambios de volumen que se realizan a través de la **interfaz ISimpleAudioVolume.** No reflejan los cambios de volumen que se realizan a través de las interfaces **IAudioStreamVolume** **e IChannelAudioVolume.** Aunque algunas aplicaciones pueden permitir a los usuarios controlar directa o indirectamente la configuración del volumen a través de **IAudioStreamVolume** e **IChannelAudioVolume,** los desarrolladores deben evitar presentar controles deslizantes de aplicación para esta configuración de volumen que es probable que los usuarios confundan con los controles deslizantes de volumen de Sndvol. De lo contrario, un usuario podría mover un control deslizante de la aplicación que espera ver el cambio reflejado en un control deslizante de Sndvol y confundirse cuando no se produce este cambio. Los desarrolladores pueden evitar este problema mediante un diseño cuidadoso de la interfaz de usuario.

El nivel de volumen efectivo de cualquier canal de la submezcla de sesión, como se escucha en los hablantes, es el producto de los cuatro factores de nivel de volumen siguientes:

-   Los niveles de volumen por canal de las secuencias de la sesión, que los clientes pueden controlar a través de los métodos de la **interfaz IAudioStreamVolume.**
-   Nivel de volumen por canal de la sesión, que los clientes pueden controlar a través de los métodos de la **interfaz IChannelAudioVolume.**
-   Nivel de volumen maestro de la sesión, que los clientes pueden controlar a través de los métodos de la **interfaz ISimpleAudioVolume.**
-   Nivel de volumen basado en directivas de la sesión, que el sistema modifica dinámicamente a medida que cambia la combinación global.

Cada uno de los cuatro factores de nivel de volumen de la lista anterior es un valor en el intervalo de 0,0 a 1,0, donde 0,0 indica silencio y 1,0 indica volumen completo (sin atenuación). El nivel de volumen efectivo también es un valor en el intervalo de 0,0 a 1,0.

El motor de audio aplica el nivel de volumen efectivo para cada canal a los canales de una secuencia antes de mezclar la secuencia con las demás secuencias de la sesión de audio. Si algún valor de ejemplo de un canal supera 0 decibelios después de que el motor de audio los haya multiplicado por el nivel de volumen efectivo, el motor recorta los ejemplos antes de agregarlos a la submezcla de sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> </dl>

 

 



