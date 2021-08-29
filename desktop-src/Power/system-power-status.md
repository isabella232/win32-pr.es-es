---
description: El estado de energía del sistema indica si la fuente de alimentación de un equipo es una batería del sistema o una alimentación de CA. En el caso de los equipos que usan baterías, el estado de energía del sistema también indica cuánta duración de la batería permanece y si la batería se está cargando.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Estado de energía del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc73f022d54536272b51c58f8fa601e65a2c1b042968d2db8324bfb63449f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143298"
---
# <a name="system-power-status"></a>Estado de energía del sistema

El estado de energía del sistema indica si la fuente de alimentación de un equipo es una batería del sistema o una alimentación de CA. En el caso de los equipos que usan baterías, el estado de energía del sistema también indica cuánta duración de la batería permanece y si la batería se está cargando.

La información de energía se recupera mediante el registro de las notificaciones de configuración de energía a través de [**la función RegisterPowerSettingNotification.**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) Esta función permite que las aplicaciones se registren para una configuración de energía específica y se les notifique cuando cambien.

> [!Note]  
> Para consultar la información de estado de energía sin notificaciones, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).

 

Las aplicaciones y los controladores instalables suelen usar el estado de energía del sistema para determinar si la operación continuada es factible. Por ejemplo, antes de que una aplicación realice operaciones en segundo plano, como comprimir o paginar un archivo, debe comprobar si el sistema está en baterías. Como otro ejemplo, una aplicación que está iniciando una operación larga debe comprobar el estado para determinar si existe suficiente batería para completar la operación.

De forma predeterminada, el sistema no consulta las aplicaciones ni los controladores durante las transiciones de suspensión.

> [!Note]  
> Si la energía es baja, una aplicación puede solicitar la intervención del usuario o solicitar que el sistema se suspenda. Puede suspender la operación del sistema mediante la [**función SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de energía](about-power-management.md)
</dt> </dl>

 

 



