---
description: Parámetros de agrupación
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Parámetros de agrupación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfb674d4349f351ce36fe1e236d1ecd3b265d8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164974"
---
# <a name="grouping-parameters"></a>Parámetros de agrupación

Un parámetro de agrupación identifica una colección de sesiones de [audio](audio-sessions.md) controladas por un único control de volumen en el programa de control de volumen del sistema, Sndvol. El parámetro de agrupación es un GUID que identifica de forma única la colección dentro del ámbito del equipo.

El propósito de un parámetro de agrupación es similar al del GUID de sesión para una sesión entre procesos. Es decir, el parámetro de agrupación permite al usuario controlar una colección de secuencias de cualquier número de procesos como una sola unidad. Sin embargo, el parámetro de agrupación sirve para este propósito en circunstancias en las que las sesiones entre procesos no pueden proporcionar una solución.

Si varios clientes asignan sus respectivos flujos a sesiones independientes pero asignan el mismo parámetro de agrupación a todas las sesiones, Sndvol muestra un control de volumen único para estas sesiones. Para proporcionar compatibilidad con parámetros de agrupación, Sndvol o cualquier aplicación de control de volumen similar debe hacer lo siguiente:

-   Antes de mostrar los controles de volumen, compruebe los parámetros de agrupación de todas las sesiones activas. Agrupar en un control de volumen único todas las sesiones que tienen el mismo parámetro de agrupación.
-   Cuando el usuario cambie la configuración de un control de volumen para un parámetro de agrupación determinado, actualice los niveles de volumen de todas las sesiones que comparten ese parámetro de agrupación.

Los parámetros de agrupación ayudan a reducir el número de controles de volumen que muestra Sndvol. Los usuarios pueden confundirse si Sndvol abarrota su pantalla con demasiados controles. Sin compatibilidad con los parámetros de agrupación, Sndvol siempre mostraría un control de volumen independiente para cada sesión, lo que podría no ser adecuado en todas las circunstancias. Además, los parámetros de agrupación proporcionan una manera cómoda de asegurarse de que las sesiones que contienen tipos similares de contenido de audio se puedan establecer fácilmente en el mismo nivel de volumen.

Como se explicó anteriormente, las API de audio de nivel superior normalmente asignan sus secuencias a la sesión predeterminada específica del proceso (identificada por el valor GUID de sesión GUID \_ NULL). Este valor predeterminado permite a Sndvol mostrar un control de volumen independiente para cada proceso de aplicación cliente, que suele ser el comportamiento deseado. Además, si varias instancias del mismo cliente se ejecutan en procesos independientes pero requieren un único control de volumen compartido, los clientes pueden asignar simplemente sus secuencias a la misma sesión entre procesos. Ninguno de estos casos requiere el uso de parámetros de agrupación. Sin embargo, un caso importante, como se ejemplifica en Microsoft Internet Explorer, requiere el uso de parámetros de agrupación para lograr el comportamiento deseado.

Internet Explorer permite a los usuarios abrir varias ventanas del explorador y es posible que estas ventanas no se ejecuten en el mismo proceso. Los usuarios podrían confundirse si Sndvol mostrara un control de volumen independiente para cada instancia de aplicación, todos con la misma etiqueta, "Internet Explorer". Una sesión entre procesos no es una solución factible en este caso: si varias instancias de Internet Explorer se ejecutan en procesos diferentes, es posible que no puedan asignar todas sus secuencias de audio a una sola sesión entre procesos. El motivo es que las ventanas de Internet Explorer pueden estar ejecutando instancias de Reproductor de Windows Media o algún otro complemento multimedia que use una API de audio de nivel superior para reproducir sus secuencias de audio. Estas API suelen asignar las secuencias de un proceso a una sesión predeterminada específica del proceso. Internet Explorer control sobre la asignación de estos flujos a sesiones.

WASAPI resuelve este problema al permitir que cada instancia de Internet Explorer acceda a los controles de sesión de su sesión predeterminada específica del proceso y asigne un parámetro de agrupación a esa sesión. Si todas las instancias de Internet Explorer el mismo parámetro de agrupación a todas sus sesiones de audio, Sndvol mostrará un control de volumen único para estas sesiones.

De forma predeterminada, una sesión no pertenece a ninguna agrupación. Si un cliente no asigna explícitamente una sesión a una agrupación, Sndvol muestra un control de volumen dedicado para esa sesión. El valor de parámetro de agrupación \_ GUID NULL indica que una sesión no pertenece a ninguna agrupación. Si ningún cliente ha asignado explícitamente un parámetro de agrupación a una sesión, el valor del parámetro de agrupación para esa sesión es NULL \_ GUID de forma predeterminada.

Un cliente puede cambiar dinámicamente la agrupación a la que se asigna una sesión.

Una agrupación puede incluir cualquier combinación de sesiones entre procesos y sesiones específicas del proceso en un dispositivo [de punto de conexión de audio.](audio-endpoint-devices.md)

La interfaz de usuario de Sndvol permite al usuario mostrar los controles de volumen solo para un dispositivo de punto de conexión de audio a la vez. Cuando el usuario ajusta los controles de volumen de un dispositivo determinado, los niveles de volumen de las sesiones que se conectan a otros dispositivos no se ven afectados. En concreto, un control de volumen para un parámetro de agrupación determinado solo afecta a las sesiones que comparten el parámetro de agrupación y están conectadas al dispositivo seleccionado actualmente. Una sesión que tiene un parámetro de agrupación idéntico pero está conectada a otro dispositivo no se ve afectada.

Como se ha descrito anteriormente, Sndvol etiqueta cada control de volumen que muestra con un nombre para mostrar y un icono. En el caso de un control de volumen para una agrupación, Sndvol selecciona arbitrariamente una de las sesiones de la agrupación como origen del nombre para mostrar y el icono que muestra con el control de volumen. Por lo tanto, para asegurarse de que Sndvol siempre muestra el mismo nombre para mostrar e icono para una agrupación, todas las instancias de aplicación que asignan sesiones a esa agrupación deben asegurarse de que sus sesiones respectivas tengan el mismo nombre para mostrar e icono. Para obtener más información sobre los iconos y los nombres para mostrar, vea [Sesiones de audio.](audio-sessions.md)

Una aplicación como Sndvol puede registrarse para recibir notificaciones cuando cambia el parámetro de agrupación de una sesión. Estas notificaciones pueden ser útiles si la aplicación almacena en caché información sobre la asignación de sesiones a parámetros de agrupación. Una notificación informa a la aplicación de que es posible que la información almacenada en caché ya no sea válida.

Para asignar un parámetro de agrupación a una sesión, llame al [**método IAudioSessionControl::SetGroupingParam.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) Para obtener el parámetro de agrupación asignado a una sesión, llame al [**método IAudioSessionControl::GetGroupingParam.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesiones de audio](audio-sessions.md)
</dt> </dl>

 

 



