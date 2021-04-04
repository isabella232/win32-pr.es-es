---
title: Eventos de entrada de voz
description: Eventos de entrada de voz
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0dc75bb010286b7645c206d192913017472829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076392"
---
# <a name="speech-input-events"></a>Eventos de entrada de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Además, en el caso de la notificación de eventos de [**comandos**](command-event.md) , el agente también notifica al cliente de entrada-activo cuando el servidor activa o desactiva el modo de escucha mediante los eventos [**ListenStart**](listenstart-event.md) y [**ListenComplete**](listencomplete-event.md) ([**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md)). Sin embargo, si el usuario presiona la tecla modo de escucha y no hay ningún motor de reconocimiento de voz correspondiente disponible para el carácter superior del cliente de entrada-activo, el servidor inicia el tiempo de espera del modo de lectura rápida de escucha, pero no genera un evento **ListenStart** para el cliente activo del carácter. Si, antes de que se complete el tiempo de espera, el usuario activa otro carácter con compatibilidad con el motor de reconocimiento de voz, el servidor intenta activar la entrada de voz y genera el evento **ListenStart** .

Del mismo modo, si un cliente intenta activar el modo de escucha con el método [**Listen**](listen-method.md) y no hay ningún motor de reconocimiento de voz coincidente disponible, se produce un error en la llamada y el servidor no genera un evento [**ListenStart**](listenstart-event.md). En el control del agente de Microsoft, el método **Listen** devuelve **false**, pero la llamada no genera un error.

Cuando el modo de clave de escucha está activado y el usuario cambia a un carácter que utiliza un motor de reconocimiento de voz diferente, el servidor cambia a y activa ese motor y desencadena un [**ListenComplete**](listencomplete-event.md) y, a continuación, un evento [**ListenStart**](listenstart-event.md) . Si el carácter activado no tiene un motor de reconocimiento de voz disponible (porque uno no está instalado o ninguno coincide con la configuración de identificador de idioma del carácter activado), el servidor desencadenará el evento **ListenComplete** para el carácter activado anteriormente y devolverá un valor en el parámetro **causa** . Sin embargo, el servidor no genera eventos **ListenStart** o **ListenComplete** para los clientes que no admiten reconocimiento de voz.

Si un cliente llama correctamente al método [**Listen**](listen-method.md) y un carácter sin compatibilidad con el motor de reconocimiento de voz se convierte en entrada-activo antes de que se complete el tiempo de espera del modo de escucha y, a continuación, el usuario vuelve al carácter del cliente original, el servidor generará un evento [**ListenStart**](listenstart-event.md) para ese cliente.

Si el cliente de entrada-activo cambia los motores de reconocimiento de voz cambiando [**SRModeID**](srmodeid-property.md) mientras está en modo de escucha, el servidor cambia a y activa ese motor sin volver a desencadenar el evento [**ListenStart**](listenstart-event.md) . Sin embargo, si el motor especificado no está disponible, se produce un error en la llamada (genera un error en el control) y el servidor también llama al evento [**ListenComplete**](listencomplete-event.md) .

 

 




