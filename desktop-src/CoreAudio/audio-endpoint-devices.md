---
description: Dispositivos de punto de conexión de audio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Dispositivos de punto de conexión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11145227ff4f6cf4eb7dd11342e28b3a8260aac95c41b32faed6b2d6bd414dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407340"
---
# <a name="audio-endpoint-devices"></a>Dispositivos de punto de conexión de audio

El término *dispositivo de punto* de conexión hace referencia a un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso de datos que se origina o finaliza en un programa de aplicación. Algunos ejemplos de dispositivos de punto de conexión de audio son altavoces, micrófonos y reproductores de CD. Los datos de audio que se mueven a lo largo de la ruta de acceso de datos pueden atravesar una serie de componentes de software y hardware durante su recorrido entre la aplicación y el dispositivo de punto de conexión. Aunque estos componentes son esenciales para el funcionamiento del dispositivo de punto de conexión, tienden a ser invisibles para los usuarios. Es más probable que los usuarios piensen en términos de dispositivos de punto de conexión que manipulan directamente en lugar de en términos de los dispositivos de los adaptadores de audio a los que los dispositivos de punto de conexión se conecten o en términos de los componentes de software que procesan las secuencias de audio que fluyen hacia y desde estos adaptadores.

Para evitar confusiones con los dispositivos de punto de conexión, esta documentación hace referencia a un dispositivo en un adaptador de audio como un *dispositivo adaptador.*

En el diagrama siguiente se muestra cómo se diferencian los dispositivos de punto de conexión de audio de los dispositivos del adaptador.

![ejemplos de dispositivos de punto de conexión de audio y dispositivos adaptadores](images/devices.jpg)

En el diagrama anterior, los siguientes son ejemplos de dispositivos de punto de conexión:

-   Altavoces
-   Micrófono
-   Dispositivo de entrada auxiliar

A continuación se muestran ejemplos de dispositivos adaptadores:

-   Dispositivo de salida de onda (contiene convertidor de digital a análogo)
-   Dispositivo de controles de salida (contiene controles de volumen y exclusión mutua)
-   Dispositivo de entrada de onda (contiene convertidor de análogo a digital)
-   Dispositivo de controles de entrada (contiene control de volumen y multiplexor)

Normalmente, las interfaces de usuario de las aplicaciones de audio hacen referencia a los dispositivos de punto de conexión de audio, no a los dispositivos adaptadores. Windows Vista simplifica el diseño de aplicaciones fáciles de usar al admitir directamente la abstracción del dispositivo de punto de conexión.

Algunos dispositivos de punto de conexión pueden conectarse permanentemente a un dispositivo adaptador. Por ejemplo, un equipo podría contener dispositivos internos, como un reproductor de CD, un micrófono o altavoces integrados en el chasis del sistema. Normalmente, el usuario no quita físicamente estos dispositivos de punto de conexión.

Otros dispositivos de punto de conexión pueden conectarse a un adaptador de audio a través de conectores de audio. El usuario conecta y desconecta estos dispositivos externos. Por ejemplo, un dispositivo de punto de conexión de audio, como un micrófono externo o micrófonos, se encuentra en un extremo de un cable cuyo otro extremo se conecta a un conector en un dispositivo adaptador.

El adaptador se comunica con el procesador del sistema a través de un bus del sistema (normalmente, PCI o PCI Express) o un bus externo (USB o IEEE 1394) que admite Plug and Play (PnP). Durante la enumeración de dispositivos, Plug and Play Manager identifica los dispositivos del adaptador de audio y los registra para que estén disponibles para su uso por el sistema operativo y por las aplicaciones.

A diferencia de la conexión entre un adaptador y un bus externo como USB o el bus IEEE 1394, la conexión entre un dispositivo de punto de conexión y un dispositivo adaptador no admite la detección de dispositivos PnP. Sin embargo, algunos adaptadores de audio admiten la detección de presencia de *conector:* cuando se inserta o quita un conector de un conector, el hardware genera una interrupción para notificar al controlador del adaptador el cambio en la configuración de hardware. El administrador de puntos de conexión Windows Vista puede aprovechar esta funcionalidad de hardware para notificar a las aplicaciones qué dispositivos de punto de conexión están presentes en cualquier momento. De este modo, el funcionamiento del administrador de puntos de conexión es análogo al del administrador de Plug and Play, que realiza un seguimiento de los dispositivos adaptadores que están presentes en el sistema.

En Windows Vista, el sistema de audio realiza un seguimiento de los dispositivos de punto de conexión y los dispositivos del adaptador. El administrador de puntos de conexión registra los dispositivos de punto de conexión y Plug and Play administrador registra los dispositivos del adaptador. El registro de dispositivos de punto de conexión facilita que las aplicaciones fáciles de usar permitan a los usuarios hacer referencia a los dispositivos de punto de conexión que los usuarios manipulan directamente en lugar de hacer referencia a dispositivos adaptadores que podrían estar ocultos dentro del chasis del equipo. Los dispositivos de punto de conexión notificados por el sistema operativo realiza un seguimiento constante de los cambios dinámicos en la configuración del hardware de audio que tiene detección de presencia de conector. Mientras un dispositivo de punto de conexión permanece conectado, el sistema lo enumera. Cuando el usuario desconecta un dispositivo de punto de conexión, el sistema deja de enumerarlo.

En versiones anteriores de Windows, incluidos Windows 98, Windows Me, Windows 2000 y Windows XP, el sistema presenta explícitamente solo dispositivos PnP a las aplicaciones. Por lo tanto, las aplicaciones deben deducir la existencia de dispositivos de punto de conexión. Un sistema operativo que no tiene compatibilidad explícita con los dispositivos de punto de conexión obliga a las aplicaciones cliente a realizar más trabajo por sí mismas. Por ejemplo, una aplicación de captura de audio debe realizar los pasos siguientes para habilitar la captura desde un micrófono externo:

1.  Enumerar todos los dispositivos de captura de audio (estos son dispositivos adaptadores) registrados previamente por el administrador de PnP.
2.  Después de seleccionar un dispositivo de captura, abra una secuencia de captura en el dispositivo mediante una llamada a la función **waveInOpen** o mediante **DirectSoundCapture** o DirectShow API.
3.  Llame a la función mixerOpen y use las demás funciones **mixerXxx** para buscar una línea MIXERLINE COMPONENTTYPE SRC MICROPHONE que se corresponda con el dispositivo de captura abierto en el \_ \_ paso \_ 2. Se trata de una suposición formada.
4.  Desbloquee la ruta de acceso de datos del micrófono. Si la ruta de acceso a datos incluye un nodo de exclusión mutua, el cliente debe deshabilitar el muting de la señal desde el micrófono. Si el dispositivo de captura contiene un multiplexor para seleccionar entre varias entradas, el cliente debe seleccionar la entrada del micrófono.

Este proceso es propenso a errores porque el software que realiza estas operaciones podría producir un error si encuentra una configuración de hardware que sus diseñadores no prevén o para la que no se ha probado.

En Windows Vista, que admite dispositivos de punto de conexión, el proceso de conexión al mismo dispositivo de punto de conexión es mucho más sencillo:

1.  Seleccione un micrófono de una colección de dispositivos de punto de conexión.
2.  Active una interfaz de captura de audio en ese micrófono.

El sistema operativo realiza todo el trabajo necesario para identificar y habilitar el dispositivo de punto de conexión. Por ejemplo, si la ruta de acceso de datos del micrófono incluye un multiplexor, el sistema selecciona automáticamente la entrada del micrófono al multiplexor.

El comportamiento del subsistema de audio es más confiable y determinista si las aplicaciones, en lugar de implementar sus propios algoritmos de identificación de puntos de conexión, pueden relegar la tarea de identificar dispositivos de punto de conexión en el sistema operativo. Los proveedores de software ya no necesitan comprobar que sus algoritmos de identificación de puntos de conexión funcionan correctamente con todos los dispositivos y configuraciones de hardware de audio disponibles: simplemente pueden confiar en el sistema operativo para la identificación de puntos de conexión. Del mismo modo, los proveedores de hardware ya no necesitan comprobar que todas las aplicaciones cliente pertinentes puedan identificar fácilmente cualquier dispositivo de punto de conexión que esté conectado a su adaptador de audio; solo necesitan comprobar que el sistema operativo puede identificar un dispositivo de punto de conexión que esté conectado a su adaptador de audio.

En los temas siguientes se proporciona información adicional sobre los dispositivos de punto de conexión de audio:

-   [Acerca de MMDevice API](mmdevice-api.md)
-   [Enumeración de dispositivos de audio](enumerating-audio-devices.md)
-   [Cadenas de identificador de punto de conexión](endpoint-id-strings.md)
-   [Propiedades de dispositivos](device-properties.md)
-   [Eventos de dispositivo](device-events.md)
-   [Roles de dispositivo](device-roles.md)
-   [Formatos de dispositivo](device-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



