---
description: Agrupar parámetros
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Agrupar parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfb674d4349f351ce36fe1e236d1ecd3b265d8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807436"
---
# <a name="grouping-parameters"></a>Agrupar parámetros

Un parámetro de agrupación identifica una colección de [sesiones de audio](audio-sessions.md) que están controladas por un único control de volumen en el programa de control de volumen del sistema, Sndvol. El parámetro de agrupación es un GUID que identifica de forma única la colección dentro del ámbito del equipo.

El propósito de un parámetro de agrupación es similar al del GUID de sesión para una sesión entre procesos. Es decir, el parámetro de agrupación permite al usuario controlar una colección de secuencias desde cualquier número de procesos como una sola unidad. Sin embargo, el parámetro de agrupación sirve para este propósito en las circunstancias en las que las sesiones entre procesos no pueden proporcionar una solución.

Si varios clientes asignan sus flujos respectivos a sesiones independientes pero asignan el mismo parámetro de agrupación a todas las sesiones, Sndvol muestra un único control de volumen para estas sesiones. Para proporcionar compatibilidad con los parámetros de agrupación, Sndvol o cualquier aplicación similar de control de volumen debe hacer lo siguiente:

-   Antes de mostrar los controles de volumen, compruebe los parámetros de agrupación de todas las sesiones activas. Agrupar en un único volumen todas las sesiones que tienen el mismo parámetro de agrupación.
-   Cuando el usuario cambie la configuración de un control de volumen para un parámetro de agrupación determinado, actualice los niveles de volumen de todas las sesiones que comparten ese parámetro de agrupación.

Los parámetros de agrupación ayudan a reducir el número de controles de volumen que se muestran en Sndvol. Los usuarios pueden confundirse si Sndvol se colapsa su presentación con demasiados controles. Sin compatibilidad con la agrupación de parámetros, Sndvol siempre mostraría un control de volumen independiente para cada sesión, lo que podría no ser adecuado en todas las circunstancias. Además, los parámetros de agrupación proporcionan una manera cómoda de asegurarse de que las sesiones que contienen tipos similares de contenido de audio se puedan establecer fácilmente en el mismo nivel de volumen.

Como se explicó anteriormente, las API de audio de nivel superior normalmente asignan sus flujos a la sesión específica predeterminada del proceso (identificada por el GUID NULL del valor GUID de la sesión \_ ). Este valor predeterminado permite a Sndvol mostrar un control de volumen independiente para cada proceso de aplicación cliente, que suele ser el comportamiento deseado. Además, si varias instancias del mismo cliente se ejecutan en procesos independientes pero requieren un único control de volumen compartido, los clientes pueden simplemente asignar sus flujos a la misma sesión entre procesos. Ninguno de estos casos requiere el uso de parámetros de agrupación. Sin embargo, un caso importante, como ejemplifica Microsoft Internet Explorer, requiere el uso de parámetros de agrupación para lograr el comportamiento deseado.

Internet Explorer permite a los usuarios abrir varias ventanas del explorador y es posible que estas ventanas no se ejecuten en el mismo proceso. Se puede confundir a los usuarios si Sndvol muestra un control de volumen independiente para cada instancia de la aplicación, todos ellos tenían la misma etiqueta, "Internet Explorer". En este caso, una sesión entre procesos no es una solución factible; si varias instancias de Internet Explorer se ejecutan en procesos diferentes, es posible que no puedan asignar todas sus secuencias de audio a una sola sesión entre procesos. La razón es que las ventanas de Internet Explorer pueden estar ejecutando instancias de Windows Media Player o algún otro complemento multimedia que use una API de audio de nivel superior para reproducir sus secuencias de audio. Estas API normalmente asignan las secuencias de un proceso a una sesión predeterminada, específica del proceso. Internet Explorer no tiene ningún control sobre la asignación de estos flujos a las sesiones.

WASAPI resuelve este problema habilitando cada instancia de Internet Explorer para tener acceso a los controles de sesión para su sesión predeterminada específica del proceso y para asignar un parámetro de agrupación a esa sesión. Si todas las instancias de Internet Explorer asignan el mismo parámetro de agrupación a todas sus sesiones de audio, Sndvol mostrará un único control de volumen para estas sesiones.

De forma predeterminada, una sesión no pertenece a ninguna agrupación. Si un cliente no asigna explícitamente una sesión a una agrupación, Sndvol muestra un control de volumen dedicado para esa sesión. El valor del parámetro de agrupación GUID \_ null indica que una sesión no pertenece a ninguna agrupación. Si ningún cliente ha asignado explícitamente un parámetro de agrupación a una sesión, el valor del parámetro de agrupación para esa sesión es GUID \_ null de forma predeterminada.

Un cliente puede cambiar dinámicamente la agrupación a la que se asigna una sesión.

Una agrupación puede incluir cualquier combinación de sesiones entre procesos y sesiones específicas del proceso en un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md).

La interfaz de usuario de Sndvol permite al usuario mostrar los controles de volumen de un solo dispositivo de punto de conexión de audio a la vez. Cuando el usuario ajusta los controles de volumen de un dispositivo determinado, los niveles de volumen de las sesiones que se conectan a otros dispositivos no se ven afectados. En concreto, un control de volumen para un parámetro de agrupación determinado solo afecta a las sesiones que comparten el parámetro de agrupación y están conectadas al dispositivo seleccionado actualmente. Una sesión que tiene un parámetro de agrupación idéntico pero que está conectada a otro dispositivo no se ve afectada.

Tal y como se ha descrito anteriormente, Sndvol etiqueta cada control de volumen que muestra con un icono y un nombre para mostrar. En el caso de un control de volumen para una agrupación, Sndvol selecciona arbitrariamente una de las sesiones de la agrupación como origen para el nombre para mostrar y el icono que muestra con el control de volumen. Por lo tanto, para asegurarse de que Sndvol siempre muestra el mismo nombre para mostrar y el icono de una agrupación, todas las instancias de la aplicación que asignan sesiones a esa agrupación deben asegurarse de que sus sesiones respectivas tengan el mismo nombre para mostrar e icono. Para obtener más información acerca de los iconos y los nombres para mostrar, consulte [sesiones de audio](audio-sessions.md).

Una aplicación como Sndvol puede registrarse para recibir notificaciones cuando cambia el parámetro de agrupación de una sesión. Estas notificaciones pueden ser útiles si la aplicación almacena en caché la información sobre la asignación de sesiones a los parámetros de agrupación. Una notificación informa A la aplicación de que es posible que la información almacenada en caché deje de ser válida.

Para asignar un parámetro de agrupación a una sesión, llame al método [**IAudioSessionControl:: SetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) . Para obtener el parámetro de agrupación que se asigna a una sesión, llame al método [**IAudioSessionControl:: GetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesiones de audio](audio-sessions.md)
</dt> </dl>

 

 



