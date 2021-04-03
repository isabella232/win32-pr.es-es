---
description: Controles de volumen de sesión
ms.assetid: e6d112f9-08c9-4d95-b37b-267beebd0d7f
title: Controles de volumen de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add29b18b39c942c54926190ef9c0f85e447bb88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907316"
---
# <a name="session-volume-controls"></a>Controles de volumen de sesión

Como se explicó anteriormente, los clientes de WASAPI pueden controlar individualmente el nivel de volumen de cada [sesión de audio](audio-sessions.md). WASAPI aplica la configuración de volumen de una sesión uniformemente a todas las secuencias de la sesión. Cada nivel de volumen es un valor comprendido en el intervalo de 0,0 a 1,0, donde 0,0 indica silencio y 1,0 indica volumen completo (sin atenuación).

Un cliente crea implícitamente una sesión asignando la primera secuencia a esa sesión. El nivel de volumen predeterminado de la nueva sesión es 1,0. Como se explicó anteriormente, el usuario puede ajustar el nivel de volumen de la sesión a través de la interfaz de usuario de un programa de control (por ejemplo, Sndvol), que es un cliente de WASAPI. La configuración del control es persistente.

Además de la configuración de volumen controlada por el cliente, el sistema aplica su propia configuración de volumen a las sesiones. Estos valores se basan en la Directiva de audio y cambian dinámicamente en respuesta a los cambios en las secuencias que componen la combinación de audio global. Para obtener más información acerca de la Directiva de audio, consulte [componentes de audio de modo de usuario](user-mode-audio-components.md).

El software del sistema que implementa el control de volumen para cada flujo multiplica los ejemplos de PCM en el flujo por el nivel de volumen efectivo. El nivel de volumen efectivo es el resultado de multiplicar la configuración del cliente y del volumen del sistema. Por lo tanto, el cambio resultante en la amplitud de la señal es una combinación lineal de los niveles de volumen del cliente y del sistema. Por ejemplo, si el nivel de volumen del cliente es 0,8 y el nivel de volumen del sistema es 0,5, el nivel de volumen efectivo es (0,8)<sup>.</sup> (0,5) = 0,4.

Tenga en cuenta que la sonoridad percibida no es lineal con respecto a la amplitud de la señal. En su lugar, la sonoridad varía aproximadamente como el logaritmo del nivel de volumen v:

sonoridad en decibelios = 20<sup>.</sup> log ₁ ₀ (v)

Por lo tanto, la configuración v = 0,5 atenúa la sonoridad de la señal original (la señal antes de que se aplique el nivel de volumen) en 6 decibelios; el valor v = 0,25 atenúa la señal en 12 decibelios, y así sucesivamente. Un nivel de volumen v = 1,0, correspondiente a 0 decibelios, no modifica el nivel de señal original.

Las aplicaciones de audio con interfaces de usuario para controlar el nivel de volumen suelen mostrar los controles deslizantes que generan cambios en la sonoridad percibida que son linealmente proporcional a los cambios en la posición del control deslizante. Para generar una relación lineal entre la sonoridad percibida y la posición del control deslizante, la aplicación debe definir una relación no lineal entre el nivel de volumen v y la posición del control deslizante. Para obtener más información, consulte [controles de volumen con inclinación de audio](audio-tapered-volume-controls.md).

Como se explicó anteriormente, el programa de control de volumen del sistema, Sndvol, muestra los controles deslizantes de volumen de las sesiones de audio que se reproducen en cada dispositivo de representación de audio. Estos controles deslizantes aparecen en el cuadro grupo denominado **aplicaciones** en la ventana SndVol. Normalmente, cada sesión contiene todos los flujos de reproducción de una ventana de aplicación determinada. A través de los controles deslizantes de la ventana de Sndvol, los usuarios controlan los niveles de volumen de las aplicaciones de audio individuales.

Como norma general, una aplicación debe asignar todos sus flujos de reproducción a la misma sesión de audio. WASAPI no impide que una aplicación distribuya sus flujos de reproducción entre varias sesiones. Sin embargo, la proliferación resultante de los controles deslizantes de volumen en Sndvol puede confundir a los usuarios.

Como opción, una ventana de la aplicación puede mostrar un control deslizante de volumen. El control deslizante de la aplicación debe reflejar todo el estado del control deslizante Sndvol correspondiente. Por lo tanto, si el usuario cambia el nivel de volumen moviendo el control deslizante en la ventana de la aplicación, el control deslizante correspondiente de la ventana Sndvol debe moverse al unísono con el control deslizante de la aplicación. Del mismo modo, si el usuario mueve el control deslizante Sndvol, el control deslizante de la aplicación debe moverse al unísono con el control deslizante de Sndvol.

Para admitir este comportamiento, WASAPI implementa la interfaz [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Cuando el usuario mueve el control deslizante de la aplicación, la aplicación llama al método [**ISimpleAudioVolume:: SetMasterVolume**](/windows/desktop/api/Audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume) para ajustar el nivel de volumen de la sesión en consecuencia. Sndvol supervisa los cambios de volumen realizados a través de este método y refleja los cambios en los controles deslizantes de volumen que muestra. Además, una aplicación puede recibir notificaciones de cambios en el volumen de sesión que el usuario realiza a través de Sndvol. Para este propósito, la aplicación implementa una interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y registra la interfaz con WASAPI. Después, cada vez que el usuario cambia el nivel de volumen de la sesión a través de Sndvol, la aplicación recibe una llamada de notificación a través del método [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) . Para obtener un ejemplo de código que implementa una interfaz **IAudioSessionEvents** , vea [eventos de sesión de audio](audio-session-events.md). Para obtener un ejemplo de código que registra una interfaz **IAudioSessionEvents** , consulte [eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md).

La interfaz **ISimpleAudioVolume** aplica el mismo nivel de volumen uniformemente a todos los canales de una sesión de audio. Aunque esta interfaz debe cumplir los requisitos de control de volumen de la mayoría de las aplicaciones, algunas aplicaciones pueden requerir capacidades de control de volumen más especializadas. La interfaz [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) controla el volumen de una secuencia individual en una sesión con respecto a las demás secuencias de la sesión. **IAudioStreamVolume** también permite a un cliente controlar individualmente los niveles de volumen de todos los canales de la secuencia. Por ejemplo, una aplicación puede usar esta funcionalidad para lograr efectos de audio como simular el movimiento espacial de un origen de audio mediante la panorámica de izquierda a derecha. Otra interfaz especializada, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), controla los niveles de volumen de los canales individuales en una sesión. Por ejemplo, una aplicación puede utilizar **IChannelAudioVolume** para implementar controles de equilibrio para un sistema de sonido stereophonic.

Los controles deslizantes de volumen del cuadro **aplicaciones** de Sndvol solo reflejan los cambios de volumen que se realizan a través de la interfaz **ISimpleAudioVolume** . No reflejan los cambios de volumen que se realizan a través de las interfaces **IAudioStreamVolume** y **IChannelAudioVolume** . Aunque algunas aplicaciones pueden permitir que los usuarios controlen directa o indirectamente la configuración de volumen a través de **IAudioStreamVolume** y **IChannelAudioVolume**, los desarrolladores deben evitar la presentación de controles deslizantes de la aplicación para esta configuración de volumen que es probable que los usuarios puedan confundir con los controles deslizantes de volumen en Sndvol. De lo contrario, un usuario puede desplazar un control deslizante de la aplicación que espera ver el cambio reflejado en un control deslizante de Sndvol y se confunde cuando no se produce este cambio. Los desarrolladores pueden evitar este problema a través de un cuidadoso diseño de la interfaz de usuario.

El nivel de volumen efectivo de cualquier canal en la submezcla de la sesión, como se oye en los oradores, es el producto de los cuatro factores de nivel de volumen siguientes:

-   Los niveles de volumen por canal de las secuencias de la sesión, que los clientes pueden controlar a través de los métodos de la interfaz **IAudioStreamVolume** .
-   Nivel de volumen por canal de la sesión, que los clientes pueden controlar a través de los métodos de la interfaz **IChannelAudioVolume** .
-   Nivel de volumen maestro de la sesión, que los clientes pueden controlar a través de los métodos de la interfaz **ISimpleAudioVolume** .
-   El nivel de volumen basado en directivas de la sesión, que el sistema modifica dinámicamente a medida que cambia la combinación global.

Cada uno de los cuatro factores de nivel de volumen de la lista anterior es un valor comprendido en el intervalo de 0,0 a 1,0, donde 0,0 indica silencio y 1,0 indica volumen completo (sin atenuación). El nivel de volumen efectivo también es un valor comprendido en el intervalo de 0,0 a 1,0.

El motor de audio aplica el nivel de volumen efectivo de cada canal a los canales de una secuencia antes de mezclar el flujo con las demás secuencias en la sesión de audio. Si los valores de ejemplo de un canal superan 0 decibelios después de que el motor de audio los haya multiplicado por el nivel de volumen efectivo, el motor recorta los ejemplos antes de agregarlos a la submezcla de la sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> </dl>

 

 



