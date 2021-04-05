---
description: Dispositivos de punto de conexión de audio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Dispositivos de punto de conexión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14d21aa174e34f8cb4ddab520819446a0e0ec89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000802"
---
# <a name="audio-endpoint-devices"></a>Dispositivos de punto de conexión de audio

El término *dispositivo de extremo* hace referencia a un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso de datos que se origina o finaliza en un programa de aplicación. Algunos ejemplos de dispositivos de punto de conexión de audio son los altavoces, los auriculares, los micrófonos y los reproductores de CD. Los datos de audio que se mueven a lo largo de la ruta de acceso de datos pueden atravesar varios componentes de software y hardware durante su recorrido entre la aplicación y el dispositivo de extremo. Aunque estos componentes son esenciales para el funcionamiento del dispositivo de extremo, tienden a ser invisibles para los usuarios. Los usuarios tienen más probabilidades de pensar en los dispositivos de punto de conexión que manipulan directamente en lugar de en los dispositivos de los adaptadores de audio que los dispositivos de punto de conexión conectan a los mismos o en términos de los componentes de software que procesan las secuencias de audio que fluyen hacia y desde estos adaptadores.

Para evitar la confusión con los dispositivos de extremo, esta documentación hace referencia a un dispositivo de un adaptador de audio como un *dispositivo de adaptador*.

En el diagrama siguiente se muestra cómo difieren los dispositivos de punto de conexión de audio de los dispositivos adaptador.

![ejemplos de dispositivos de punto de conexión de audio y dispositivos de adaptador](images/devices.jpg)

En el diagrama anterior, los siguientes son ejemplos de dispositivos de punto de conexión:

-   Altavoces
-   Micrófono
-   Dispositivo de entrada auxiliar

Los siguientes son ejemplos de dispositivos de adaptador:

-   Dispositivo de salida de onda (contiene el convertidor digital a analógico)
-   Dispositivo de controles de salida (contiene controles de volumen y de silencio)
-   Dispositivo de entrada de onda (contiene convertidor de analógico a digital)
-   Dispositivo de controles de entrada (contiene control de volumen y multiplexor)

Normalmente, las interfaces de usuario de las aplicaciones de audio hacen referencia a dispositivos de punto de conexión de audio, no a dispositivos de adaptador. Windows Vista simplifica el diseño de aplicaciones fáciles de obtener al admitir directamente la abstracción del dispositivo de extremo.

Algunos dispositivos de extremo pueden conectarse permanentemente a un dispositivo de adaptador. Por ejemplo, un equipo puede contener dispositivos internos como un reproductor de CD, un micrófono o altavoces que están integrados en el chasis del sistema. Normalmente, el usuario no quita físicamente estos dispositivos de extremo.

Es posible que otros dispositivos de extremo se conecten a un adaptador de audio a través de conectores de audio. El usuario conecta y desconecta estos dispositivos externos. Por ejemplo, un dispositivo de punto de conexión de audio, como un micrófono externo o auriculares, se encuentra en un extremo de un cable cuyo otro extremo se conecta a un conector en un dispositivo adaptador.

El adaptador se comunica con el procesador del sistema a través de un bus del sistema (normalmente, PCI o PCI Express) o bus externo (USB o IEEE 1394) que admite Plug and Play (PnP). Durante la enumeración de dispositivos, el administrador de Plug and Play identifica los dispositivos del adaptador de audio y los registra para que estén disponibles para su uso por parte del sistema operativo y de las aplicaciones.

A diferencia de la conexión entre un adaptador y un bus externo, como USB o el bus IEEE 1394, la conexión entre un dispositivo de extremo y un dispositivo de adaptador no admite la detección de dispositivos PnP. Sin embargo, algunos adaptadores de audio admiten la *detección de la presencia de enchufes*: cuando se inserta o se quita un conector en un conector, el hardware genera una interrupción para notificar al controlador de adaptador el cambio en la configuración de hardware. El administrador de extremos en Windows Vista puede aprovechar esta capacidad de hardware para notificar a las aplicaciones qué dispositivos de punto de conexión están presentes en cualquier momento. De esta manera, la operación del administrador de extremos es análoga a la del administrador de Plug and Play, que realiza un seguimiento de los dispositivos de adaptador que están presentes en el sistema.

En Windows Vista, el sistema de audio realiza un seguimiento de los dispositivos de extremo y los dispositivos de adaptador. El administrador de puntos de conexión registra los dispositivos de punto de conexión y el administrador de Plug and Play registra los dispositivos de adaptador. El registro de dispositivos de punto de conexión facilita a los usuarios hacer referencia a los dispositivos de punto de conexión que los usuarios manipulan directamente en lugar de hacer referencia a los dispositivos de adaptador que podrían estar ocultos dentro del chasis del equipo. Los dispositivos de punto de conexión a los que el sistema operativo informan fielmente realizan un seguimiento de los cambios dinámicos en la configuración del hardware de audio que tiene detección de presencia de conector. Mientras un dispositivo de extremo permanece enchufado en, el sistema enumera dicho dispositivo. Cuando el usuario desconecta un dispositivo de extremo, el sistema deja de enumerarlo.

En versiones anteriores de Windows, incluidas Windows 98, Windows me, Windows 2000 y Windows XP, el sistema solo presenta dispositivos PnP a las aplicaciones de forma explícita. Por lo tanto, las aplicaciones deben inferir la existencia de dispositivos de extremo. Un sistema operativo que carece de compatibilidad explícita con los dispositivos de punto de conexión obliga a las aplicaciones cliente a realizar más tareas. Por ejemplo, una aplicación de captura de audio debe realizar los pasos siguientes para habilitar la captura desde un micrófono externo:

1.  Enumerar todos los dispositivos de captura de audio (que son dispositivos de adaptador) que se registraron anteriormente con el administrador de PnP.
2.  Después de seleccionar un dispositivo de captura, abra una secuencia de captura en el dispositivo mediante una llamada a la función **waveInOpen** o mediante la API **DirectSoundCapture** o DirectShow.
3.  Llame a la función mixerOpen y use las demás funciones **mixerXxx** para buscar una \_ línea de micrófono MIXERLINE COMPONENTTYPE \_ src \_ que se corresponda con el dispositivo de captura abierto en el paso 2. Se trata de una estimación educada.
4.  Desbloquee la ruta de acceso de datos del micrófono. Si la ruta de acceso de datos incluye un nodo silenciar, el cliente debe deshabilitar el silenciamiento de la señal del micrófono. Si el dispositivo de captura contiene un multiplexor para seleccionar entre varias entradas, el cliente debe seleccionar la entrada del micrófono.

Este proceso es propenso a errores porque el software que realiza estas operaciones podría producir un error si encuentra una configuración de hardware que sus diseñadores no preveían o para la que no se probó.

En Windows Vista, que admite dispositivos de extremo, el proceso de conexión al mismo dispositivo de extremo es mucho más sencillo:

1.  Seleccione un micrófono de una colección de dispositivos de extremo.
2.  Active una interfaz de captura de audio en el micrófono.

El sistema operativo realiza todo el trabajo necesario para identificar y habilitar el dispositivo de extremo. Por ejemplo, si la ruta de acceso de datos del micrófono incluye un multiplexor, el sistema selecciona automáticamente la entrada del micrófono para el multiplexor.

El comportamiento del subsistema de audio es más confiable y determinista si las aplicaciones, en lugar de implementar sus propios algoritmos de identificación de punto de conexión, pueden relegar la tarea de identificar los dispositivos de extremo en el sistema operativo. Los proveedores de software ya no necesitan comprobar que sus algoritmos de identificación de punto de conexión funcionan correctamente con todos los dispositivos y configuraciones de hardware de audio disponibles, por lo que simplemente pueden confiar en el sistema operativo para la identificación del punto de conexión. Del mismo modo, los proveedores de hardware ya no necesitan comprobar que todas las aplicaciones cliente pertinentes pueden identificar fácilmente cualquier dispositivo de punto de conexión que esté conectado a su adaptador de audio, solo necesitan comprobar que el sistema operativo puede identificar un dispositivo de extremo que está conectado a su adaptador de audio.

En los temas siguientes se proporciona información adicional acerca de los dispositivos de punto de conexión de audio:

-   [Acerca de la API de MMDevice](mmdevice-api.md)
-   [Enumerar dispositivos de audio](enumerating-audio-devices.md)
-   [Cadenas de ID. de punto de conexión](endpoint-id-strings.md)
-   [Propiedades de dispositivos](device-properties.md)
-   [Eventos de dispositivo](device-events.md)
-   [Roles de dispositivo](device-roles.md)
-   [Formatos de dispositivo](device-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



