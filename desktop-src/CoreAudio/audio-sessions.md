---
description: Sesiones de audio
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Sesiones de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ae67a3eafe7a76add2fad192823868304e860d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165134"
---
# <a name="audio-sessions"></a>Sesiones de audio

Una *sesión de audio* es un grupo de secuencias de audio relacionadas que un cliente WASAPI puede administrar colectivamente. Los clientes pueden controlar el nivel de volumen y el estado muting de cada sesión individual. El sistema aplica la configuración de volumen y exclusión especificada por el cliente de forma uniforme a todas las secuencias de la sesión.

Cuando un cliente inicializa una secuencia de audio, asigna la secuencia de audio a una sesión de audio. Para obtener más información, [**vea IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Una sesión de audio contiene secuencias de representación o secuencias de captura, pero no ambas. De forma predeterminada, la configuración de volumen y exclusión mutua de una sesión de representación es persistente en los reinicios del sistema. La configuración de volumen y exclusión mutua de una sesión de captura no es persistente. (Una sesión que contiene secuencias que funcionan en modo de bucle recuperación se trata igual que una sesión de captura. Es decir, la configuración de la sesión no es persistente. Para obtener más información sobre el modo de bucle recuperación, vea [Grabación de buclesback).](loopback-recording.md)

Cada secuencia de audio pertenece exactamente a una sesión. Un cliente asigna una secuencia de audio a una sesión determinada en el momento en que inicializa el objeto de secuencia. La secuencia conserva su pertenencia a la sesión durante la vigencia de la secuencia. Después de crear un objeto de secuencia, el objeto existe hasta que un cliente libera la última referencia contada al objeto y, a continuación, se elimina el objeto.

Aunque un cliente no puede cambiar la sesión a la que se asigna una secuencia existente, puede lograr un efecto similar eliminando la secuencia (liberando todas las referencias a ella), creando una nueva secuencia para reemplazar la secuencia eliminada y asignando la nueva secuencia a otra sesión.

Cada sesión de representación representa un subconjunto de las secuencias que forman la combinación global que se reproduce a través de un dispositivo de punto de [conexión de audio determinado.](audio-endpoint-devices.md) La combinación global combina todas las sesiones de todas las aplicaciones que comparten el dispositivo.

Con frecuencia, una aplicación con varios flujos asigna todos sus flujos a la misma sesión. Sin embargo, la aplicación puede, como opción, asignar secuencias diferentes a diferentes sesiones. Cualquier secuencia que la aplicación no asigne explícitamente a una sesión pertenece a la sesión predeterminada.

Las aplicaciones de audio típicas deben evitar modificar la configuración de volumen y exclusión mutua de las sesiones. En su lugar, los usuarios controlan esta configuración a través de las interfaces de usuario de los programas de control. Por ejemplo, en Windows Vista, el programa proporcionado por el sistema, Sndvol.exe, muestra un control de volumen y un control de exclusión mutua para cada sesión de representación activa o recientemente activa en el sistema. A través de estos controles, los usuarios pueden ajustar la configuración de volumen y exclusión mutua para todas las sesiones del sistema.

Actualmente, el programa Sndvol solo muestra controles de volumen para dispositivos de punto de conexión de representación de audio. No muestra controles de volumen para dispositivos de captura de audio.

Una sesión está activa si contiene una o varias secuencias activas. Una secuencia activa está en el *estado en ejecución*. Una secuencia inactiva está en estado *detenido.* Una sesión se activa cuando su primera secuencia se activa. Una sesión se vuelve inactiva cuando su última secuencia activa queda inactiva. Una vez que una sesión ha estado inactiva durante un período de tiempo, el sistema cambia el estado de la sesión de inactiva a expirada.

Sndvol muestra controles de volumen y exclusión mutua para todas las sesiones de representación activas e inactivas. Sndvol quita los controles de volumen y exclusión mutua de una sesión cuando el estado de la sesión cambia de inactivo a expirado, o cuando finaliza la sesión. (Una sesión finaliza cuando se elimina la última de sus secuencias; es decir, cuando un cliente libera el recuento de referencias final en el último objeto de secuencia restante de la sesión). La única excepción a esta regla es para los sonidos de notificación del sistema. Sndvol siempre muestra los controles de volumen y exclusión mutua para los sonidos de notificación del sistema, independientemente del estado de la sesión para estos sonidos.

Normalmente, una secuencia pertenece a una sesión que abarca solo el proceso que contiene la aplicación que creó la secuencia. Sin embargo, las aplicaciones tienen la opción de definir sesiones entre procesos que combinan secuencias de dos o más procesos.

WASAPI admite sesiones entre procesos principalmente para:

-   El programa Sndvol puede presentar al usuario un control de volumen único para administrar los sonidos de notificación del sistema en todas las aplicaciones.
-   Un reproductor multimedia que se ejecuta en un proceso puede transmitir contenido protegido a un programa de descifrado que se ejecuta en otro proceso.

De forma similar a la configuración del control para las sesiones de representación específicas del proceso, la configuración de control para las sesiones de representación entre procesos es, de forma predeterminada, persistente en los reinicios del sistema. WASAPI proporciona este comportamiento principalmente para la ventaja de los sonidos de notificación del sistema, que deben conservar la configuración de volumen y exclusión mutua del usuario a medida que la combinación de aplicaciones varía con el tiempo.

El programa Sndvol etiqueta el control de volumen de cada sesión con un nombre para mostrar y un icono. Un cliente tiene la opción de asignar explícitamente un nombre para mostrar y un icono a una sesión. Si el cliente no proporciona estos elementos, Sndvol muestra un nombre predeterminado y un icono predeterminado en su lugar. El nombre predeterminado incorpora información como el título de la ventana de la aplicación. El icono predeterminado es el icono de la ventana de la aplicación. Solo en el caso de sesiones específicas del proceso, estos valores predeterminados proporcionan información significativa a los usuarios. Tenga en cuenta que una sesión entre procesos se puede asociar a más de una aplicación. En este caso, solo un icono y un nombre para mostrar proporcionados por el cliente son significativos.

Aunque la configuración de volumen y exclusión mutua de una sesión de representación es, de forma predeterminada, persistente en los reinicios del sistema, el icono y el nombre para mostrar proporcionados por el cliente no lo son. Para asegurarse de que Sndvol muestra el nombre y el icono proporcionados por el cliente, el cliente debe asignar explícitamente el nombre y el icono a la sesión en el momento en que el cliente asigna la primera secuencia a la sesión. El sistema conserva el nombre para mostrar y el icono de una sesión solo hasta que finaliza la sesión.

Cada sesión se identifica mediante un GUID de sesión. En el momento en que un cliente abre una secuencia, el cliente asigna esa secuencia a una sesión determinada. El cliente proporciona los dos fragmentos de información siguientes para identificar esa sesión:

-   GUID de sesión.
-   Si la sesión es una sesión entre procesos o específica del proceso: una sesión específica del proceso solo contiene secuencias del proceso del cliente.

Esta información es suficiente para distinguir una sesión determinada de todas las demás sesiones del mismo equipo. El GUID de sesión de una sesión específica del proceso identifica de forma única la sesión solo dentro del ámbito del proceso que posee la sesión. Por el contrario, el GUID de sesión para una sesión entre procesos es único dentro del ámbito de todos los procesos que se ejecutan en el equipo.

En el caso de una sesión específica del proceso, el sistema usa una combinación de GUID de sesión e identificador de proceso para identificar de forma única la sesión dentro del ámbito del equipo. Por lo tanto, si los clientes de dos procesos diferentes asignan sus respectivos flujos a dos sesiones específicas del proceso con GUID de sesión idénticos, el sistema trata las sesiones como independientes porque sus id. de proceso son diferentes. Además, si una sesión entre procesos usa el mismo GUID de sesión que una o varias sesiones específicas del proceso, el sistema trata la sesión entre procesos como distinta de las sesiones específicas del proceso, aunque compartan el mismo GUID de sesión.

Por ejemplo, en Windows Vista, las API de nivel superior, como las funciones **waveOutXxx** multimedia de Windows y Direct Sound suelen asignar las secuencias de audio que crean a sesiones específicas del proceso predeterminadas identificadas por el valor GUID de sesión GUID \_ NULL. Para los clientes de estas API, la sesión predeterminada para cada proceso de cliente es independiente de las sesiones predeterminadas para otros procesos de cliente, aunque las sesiones tengan GUID de sesión idénticos. Además, si una o varias aplicaciones asignan secuencias a la sesión entre procesos identificada por el valor GUID de sesión GUID NULL, el sistema trata esta sesión entre procesos como independiente de las sesiones predeterminadas específicas del proceso que comparten el mismo GUID de \_ sesión. En consecuencia, el programa Sndvol muestra un control de volumen independiente para la sesión predeterminada específica del proceso de cada cliente y muestra un control de volumen adicional para la sesión entre procesos que se identifica mediante el VALOR GUID NULL de la sesión, si esa sesión \_ existe.

Cada sesión está asociada a un único dispositivo de punto de conexión de audio. Si dos sesiones tienen GUID de sesión idénticos e id. de proceso, pero están asociadas a distintos dispositivos, el sistema trata las dos sesiones como independientes. Una sesión nunca puede contener secuencias de captura y representación porque una secuencia de captura solo se puede asociar a un dispositivo de captura y una secuencia de representación solo se puede asociar a un dispositivo de representación.

Como se mencionó anteriormente, la configuración de volumen y exclusión mutua de una sesión es persistente en los reinicios del sistema. Dos o más instancias de una aplicación pueden crear sesiones específicas del proceso con GUID de sesión idénticos. A través del programa Sndvol, el usuario puede seleccionar diferentes configuraciones de volumen y exclusión mutua para cada una de estas sesiones. Una vez que finalizan estas sesiones, el sistema conserva la configuración de control de solo una de estas sesiones: la última sesión que se termina. Más adelante, si una nueva instancia de la aplicación crea una sesión específica del proceso con el mismo GUID de sesión que antes, esa sesión hereda la configuración de volumen y exclusión previamente guardada.

Una aplicación no debe intentar agregar una secuencia ni controlar el nivel de volumen de una sesión que sea propiedad de otra aplicación no relacionada. Además, una aplicación no debe intentar controlar el nivel de volumen de la sesión administrada por el sistema para los sonidos de notificación. Sin embargo, una aplicación puede reproducir un sonido a través de la sesión del sistema para los sonidos de notificación mediante una llamada a la **función Play Sound.** Para obtener más información, vea [Sonidos de notificación para aplicaciones de audio heredadas.](notification-sounds-for-legacy-audio-applications.md)

Una aplicación puede registrarse para recibir notificaciones cuando cambia el estado de una sesión. Para obtener más información, vea [Eventos de sesión de audio](audio-session-events.md).

En raras ocasiones, una aplicación que crea una sesión específica del proceso podría necesitar consolidar el control de las sesiones específicas del proceso para dos o más instancias de aplicación bajo un control de volumen único en Sndvol. Para obtener más información, vea [Parámetros de agrupación.](grouping-parameters.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



