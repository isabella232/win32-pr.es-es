---
description: Sesiones de audio
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Sesiones de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ae67a3eafe7a76add2fad192823868304e860d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153524"
---
# <a name="audio-sessions"></a>Sesiones de audio

Una *sesión de audio* es un grupo de secuencias de audio relacionadas que un cliente de WASAPI puede administrar colectivamente. Los clientes pueden controlar el nivel de volumen y silenciar el estado de cada sesión individual. El sistema aplica la configuración de volumen y silencio especificada por el cliente uniformemente a todas las secuencias de la sesión.

Cuando un cliente Inicializa una secuencia de audio, asigna la secuencia de audio a una sesión de audio. Para obtener más información, vea [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Una sesión de audio contiene flujos de representación o secuencias de captura, pero no ambos. De forma predeterminada, la configuración de volumen y silenciar para una sesión de representación es persistente en todos los reinicios del sistema. La configuración de volumen y silenciar para una sesión de captura no es persistente. (Una sesión que contiene secuencias que funcionan en modo de bucle invertido se trata igual que una sesión de captura. Es decir, la configuración de la sesión no es persistente. Para obtener más información sobre el modo de bucle invertido, vea [grabación de bucle invertido](loopback-recording.md)).

Cada secuencia de audio pertenece exactamente a una sesión. Un cliente asigna una secuencia de audio a una sesión determinada en el momento en que inicializa el objeto de secuencia. La secuencia conserva su pertenencia a la sesión durante la duración de la secuencia. Después de crear un objeto de flujo, el objeto existe hasta que un cliente libera la última referencia de recuento al objeto y, a continuación, se elimina el objeto.

Aunque un cliente no puede cambiar la sesión a la que se asigna una secuencia existente, puede lograr un efecto similar eliminando la secuencia (liberando todas las referencias a ella), creando una nueva secuencia para reemplazar la secuencia eliminada y asignando la nueva secuencia a otra sesión.

Cada sesión de representación representa un subconjunto de las secuencias que forman la combinación global que se reproduce a través de un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md)determinado. La combinación global combina todas las sesiones de todas las aplicaciones que comparten el dispositivo.

Con frecuencia, una aplicación con varios flujos asigna todos sus flujos a la misma sesión. Sin embargo, la aplicación puede, opcionalmente, asignar diferentes flujos a diferentes sesiones. Cualquier secuencia que la aplicación no asigna explícitamente a una sesión pertenece a la sesión predeterminada.

Las aplicaciones de audio típicas deben evitar modificar el volumen y silenciar la configuración de las sesiones. En su lugar, los usuarios controlan estos valores a través de las interfaces de usuario de los programas de control. Por ejemplo, en Windows Vista, el programa proporcionado por el sistema, Sndvol.exe, muestra un control de volumen y un control de silencio para cada sesión de representación activa o reciente en el sistema. A través de estos controles, los usuarios pueden ajustar el volumen y silenciar la configuración de todas las sesiones del sistema.

El programa Sndvol actualmente solo muestra los controles de volumen para los dispositivos de punto de conexión de representación de audio. No muestra controles de volumen para dispositivos de captura de audio.

Una sesión está activa si contiene una o varias secuencias activas. Un flujo activo está en *Estado de ejecución*. Una secuencia inactiva está en *estado detenido*. Una sesión se activa cuando su primera secuencia se activa. Una sesión se vuelve inactiva cuando su última secuencia activa se vuelve inactiva. Una vez que una sesión ha estado inactiva durante un período de tiempo, el sistema cambia el estado de la sesión de inactiva a expirada.

Sndvol muestra los controles VOLUME y MUTE para todas las sesiones de representación activas e inactivas. Sndvol quita los controles VOLUME y MUTE de una sesión cuando el estado de la sesión cambia de inactivo a expirado, o cuando la sesión finaliza. (Una sesión finaliza cuando se elimina el último de sus flujos; es decir, cuando un cliente libera el recuento de referencias final en el último objeto de flujo restante de la sesión). La única excepción a esta regla son los sonidos de la notificación del sistema. Sndvol siempre muestra los controles volumen y silenciar para los sonidos de la notificación del sistema, independientemente del estado de la sesión para estos sonidos.

Normalmente, una secuencia pertenece a una sesión que abarca solo el proceso que contiene la aplicación que creó la secuencia. Sin embargo, las aplicaciones tienen la opción de definir sesiones entre procesos que combinen flujos de dos o más procesos.

WASAPI admite las sesiones entre procesos principalmente para que:

-   El programa Sndvol puede presentar al usuario un único control de volumen para administrar los sonidos de la notificación del sistema en todas las aplicaciones.
-   Un reproductor de media que se ejecuta en un proceso puede transmitir contenido protegido a un programa de descifrado que se ejecuta en otro proceso.

De forma predeterminada, es similar a la configuración de control de las sesiones de representación específicas del proceso, ya que la configuración de control de las sesiones de representación entre procesos es persistente de forma predeterminada a través de reinicios del sistema. WASAPI proporciona este comportamiento principalmente para la ventaja de los sonidos de la notificación del sistema, que deben conservar el volumen del usuario y silenciar la configuración a medida que la combinación de aplicaciones varía con el tiempo.

El programa Sndvol etiqueta el control de volumen de cada sesión con un nombre para mostrar y un icono. Un cliente tiene la opción de asignar explícitamente un nombre para mostrar y un icono a una sesión. Si el cliente no proporciona estos elementos, Sndvol muestra un nombre predeterminado y un icono predeterminado en su lugar. El nombre predeterminado incorpora información como el título de la ventana de la aplicación. El icono predeterminado es el icono de la ventana de la aplicación. Solo en el caso de las sesiones específicas del proceso, estos valores predeterminados proporcionan información significativa a los usuarios. Tenga en cuenta que se puede asociar una sesión entre procesos a más de una aplicación. En este caso, solo es significativo el nombre para mostrar y el icono proporcionado por el cliente.

Aunque la configuración de volumen y silenciar para una sesión de representación es persistente de forma predeterminada a través de reinicios del sistema, el nombre para mostrar proporcionado por el cliente y el icono no lo son. Para asegurarse de que Sndvol muestra el nombre y el icono proporcionados por el cliente, el cliente debe asignar explícitamente el nombre y el icono a la sesión en el momento en que el cliente asigna la primera secuencia a la sesión. El sistema conserva el nombre para mostrar y el icono de una sesión solo hasta que finalice la sesión.

Cada sesión se identifica mediante un GUID de sesión. En el momento en que un cliente abre una secuencia, el cliente asigna esa secuencia a una sesión determinada. El cliente proporciona los dos fragmentos de información siguientes para identificar la sesión:

-   GUID de sesión.
-   Si la sesión es una sesión específica del proceso o entre procesos, una sesión específica del proceso solo contiene flujos del proceso del cliente.

Esta información es suficiente para distinguir una sesión determinada de todas las demás sesiones del mismo equipo. El GUID de sesión para una sesión específica del proceso solo identifica la sesión en el ámbito del proceso que posee la sesión. Por el contrario, el GUID de sesión para una sesión entre procesos es único dentro del ámbito de todos los procesos que se ejecutan en el equipo.

En el caso de una sesión específica del proceso, el sistema utiliza una combinación de GUID de sesión e identificador de proceso para identificar de forma única la sesión en el ámbito del equipo. Por lo tanto, si los clientes de dos procesos diferentes asignan sus flujos respectivos a dos sesiones específicas del proceso con GUID de sesión idénticos, el sistema trata las sesiones como independientes porque sus identificadores de proceso son diferentes. Además, si una sesión entre procesos utiliza el mismo GUID de sesión que una o varias sesiones específicas del proceso, el sistema trata la sesión entre procesos como distinta de las sesiones específicas del proceso, aunque compartan el mismo GUID de sesión.

Por ejemplo, en Windows Vista, las API de nivel superior, como las funciones **waveOutXxx** de multimedia de Windows y DirectSound, normalmente asignan las secuencias de audio que crean a las sesiones predeterminadas específicas del proceso identificadas por el GUID del valor GUID de la sesión \_ . En el caso de los clientes de estas API, la sesión predeterminada para cada proceso de cliente es independiente de las sesiones predeterminadas para otros procesos de cliente, aunque las sesiones tengan GUID de sesión idénticos. Además, si una o varias aplicaciones asignan flujos a la sesión entre procesos que se identifica con el GUID NULL del valor GUID de la sesión \_ , el sistema trata esta sesión entre procesos como independiente de las sesiones predeterminadas específicas del proceso que comparten el mismo GUID de sesión. Por lo tanto, el programa Sndvol muestra un control de volumen independiente para cada sesión predeterminada específica del proceso de cada cliente, y muestra un control de volumen adicional para la sesión entre procesos que se identifica mediante el GUID NULL del valor GUID de sesión \_ , si la sesión existe.

Cada sesión está asociada solo a un dispositivo de punto de conexión de audio. Si dos sesiones tienen GUID de sesión idénticos e identificadores de proceso, pero están asociados a distintos dispositivos, el sistema trata las dos sesiones como independientes. Una sesión nunca puede contener secuencias de captura y representación porque una secuencia de captura solo se puede asociar a un dispositivo de captura y un flujo de representación solo se puede asociar a un dispositivo de representación.

Como se mencionó anteriormente, los valores Volume y MUTE de una sesión son persistentes en los reinicios del sistema. Dos o más instancias de una aplicación pueden crear sesiones específicas del proceso con GUID de sesión idénticos. A través del programa Sndvol, el usuario puede seleccionar diferentes valores de configuración de volumen y de silencio para cada una de estas sesiones. Una vez finalizadas estas sesiones, el sistema conserva la configuración de control de solo una de estas sesiones, la última sesión que se va a finalizar. Más adelante, si una nueva instancia de la aplicación crea una sesión específica del proceso con el mismo GUID de sesión que antes, dicha sesión heredará la configuración de volumen y silencia previamente guardada.

Una aplicación no debe intentar agregar una secuencia a o controlar el nivel de volumen de una sesión que pertenece a otra aplicación no relacionada. Además, una aplicación no debe intentar controlar el nivel de volumen de la sesión administrada por el sistema para los sonidos de notificación. Sin embargo, una aplicación puede reproducir un sonido a través de la sesión del sistema para los sonidos de notificación mediante una llamada a la función **PlaySound** . Para obtener más información, consulte [sonidos de notificación para aplicaciones de audio heredadas](notification-sounds-for-legacy-audio-applications.md).

Una aplicación puede registrarse para recibir notificaciones cuando cambia el estado de una sesión. Para obtener más información, consulte [eventos de sesión de audio](audio-session-events.md).

En raras ocasiones, una aplicación que crea una sesión específica del proceso podría necesitar consolidar el control de las sesiones específicas del proceso para dos o más instancias de la aplicación en un control de volumen único en Sndvol. Para obtener más información, vea [Grouping Parameters](grouping-parameters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



