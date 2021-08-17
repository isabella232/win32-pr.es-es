---
title: Notificaciones informativos
description: Para los estados de conexión conocidos como estados en ejecución, no se requiere ninguna acción del controlador de notificaciones a menos que se produzca un error.
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f526dcd0cd52eaa15929f970debe3ba78788fdb7525e734ee2e26e348b32552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790999"
---
# <a name="informational-notifications"></a>Notificaciones informativos

Para los [estados de conexión](connection-states.md) conocidos como estados en ejecución, no se requiere ninguna acción del controlador de notificaciones a menos que se produzca un error. Los estados en ejecución se producen durante las partes de la operación de conexión que RAS controla automáticamente, como conectarse a los dispositivos necesarios, autenticar al usuario y esperar una devolución de llamada desde el servidor remoto. La notificación es simplemente un informe de progreso para el cliente.

El cliente puede optar por pasar estas notificaciones informativos al usuario. En algunos estados en ejecución, es posible que el cliente quiera mostrar información adicional. Por ejemplo, un controlador de notificaciones que recibe una notificación CONNECTDevice de RASCS puede llamar a la \_ [**función RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el nombre y el tipo del dispositivo al que se está conectando. Otro ejemplo es cuando el cliente recibe una notificación \_ proyectada de RASCS. Esto ocurre cuando se ha completado la fase de proyección RAS de la operación de conexión. El cliente puede llamar a la [**función RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) para obtener información adicional sobre la proyección. El cliente puede usar esta información para notificar al usuario qué protocolos de red puede usar esta conexión.

Debe evitar escribir código que dependa del orden o la aparición de determinados estados informativos, ya que esto puede variar entre plataformas.

 

 




