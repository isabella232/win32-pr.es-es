---
title: Eventos de entrada de voz
description: Eventos de entrada de voz
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3babdfb38f302bd2ca5934fec4d8b54a84f7452befbec0dfba45b078747f532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746266"
---
# <a name="speech-input-events"></a>Eventos de entrada de voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Además, a [](command-event.md) la notificación de eventos Command, el Agente también notifica al cliente activo de entrada cuando el servidor activa o desactiva el modo de escucha, mediante los eventos [**ListenStart**](listenstart-event.md) y [**ListenComplete**](listencomplete-event.md) ([**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md)). Sin embargo, si el usuario presiona la tecla Modo de escucha y no hay ningún motor de reconocimiento de voz correspondiente disponible para el carácter superior del cliente activo de entrada, el servidor inicia el tiempo de espera del modo de tecla de acceso rápido De escucha, pero no genera un evento **ListenStart** para el cliente activo del carácter. Si, antes de que finalice el tiempo de espera, el usuario activa otro carácter con compatibilidad con el motor de reconocimiento de voz, el servidor intenta activar la entrada de voz y genera el **evento ListenStart.**

Del mismo modo, si un cliente intenta activar el modo de escucha mediante el método [**Listen**](listen-method.md) y no hay ningún motor de reconocimiento de voz correspondiente disponible, se produce un error en la llamada y el servidor no genera un evento [**ListenStart.**](listenstart-event.md) En el control Microsoft Agent, el **método Listen** devuelve **False,** pero la llamada no genera un error.

Cuando el modo de clave de escucha está activado y el usuario cambia a un carácter que usa un motor de reconocimiento de voz diferente, el servidor cambia a ese motor y lo activa y desencadena un [**evento ListenComplete**](listencomplete-event.md) y, a continuación, [**un evento ListenStart.**](listenstart-event.md) Si el carácter activado no tiene un motor de reconocimiento de voz disponible (porque uno no está instalado o ninguno coincide con la configuración del identificador de idioma del carácter activado), el servidor desencadenará el evento **ListenComplete** para el carácter activado previamente y pasará un valor en el parámetro **Cause.** Sin embargo, el servidor no genera eventos **ListenStart** o **ListenComplete** para los clientes que no tienen compatibilidad con el reconocimiento de voz.

Si un cliente llama correctamente al método [**Listen**](listen-method.md) y un carácter sin compatibilidad con el motor de reconocimiento de voz se convierte en entrada-activa antes de que finalice el tiempo de espera del modo de escucha y, a continuación, el usuario vuelve al carácter del cliente original, el servidor generará un evento [**ListenStart**](listenstart-event.md) para ese cliente.

Si el cliente activo de entrada cambia los motores de reconocimiento de voz cambiando [**SRModeID**](srmodeid-property.md) mientras está en modo de escucha, el servidor cambia a ese motor y lo activa sin volver a desencadenar el evento [**ListenStart.**](listenstart-event.md) Sin embargo, si el motor especificado no está disponible, se produce un error en la llamada (genera un error en el control ) y el servidor también llama al [**evento ListenComplete.**](listencomplete-event.md)

 

 




