---
description: El estado de alimentación del sistema indica si el origen de energía de un equipo es una batería de sistema o corriente alterna. En el caso de los equipos que usan baterías, el estado de alimentación del sistema también indica la duración de la batería y si la batería se está cargando.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Estado de la alimentación del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677886"
---
# <a name="system-power-status"></a>Estado de la alimentación del sistema

El estado de alimentación del sistema indica si el origen de energía de un equipo es una batería de sistema o corriente alterna. En el caso de los equipos que usan baterías, el estado de alimentación del sistema también indica la duración de la batería y si la batería se está cargando.

La información de energía se recupera registrando las notificaciones de configuración de energía a través de la función [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Esta función permite a las aplicaciones registrarse para una configuración de energía específica y recibir una notificación cuando cambien.

> [!Note]  
> Para consultar la información de estado de energía sin notificaciones, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).

 

Las aplicaciones y los controladores instalables normalmente usan el estado de alimentación del sistema para determinar si la operación continua es viable. Por ejemplo, antes de que una aplicación realice operaciones en segundo plano, como comprimir o paginar un archivo, debe comprobar si el sistema tiene baterías. Otro ejemplo: una aplicación que inicia una operación larga debe comprobar el estado para determinar si existe suficiente energía de la batería para completar la operación.

De forma predeterminada, el sistema no consulta las aplicaciones o los controladores durante las transiciones de suspensión.

> [!Note]  
> Si la alimentación es baja, una aplicación puede solicitar la intervención del usuario o solicitar que el sistema se suspenda. Puede suspender el funcionamiento del sistema mediante la función [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



