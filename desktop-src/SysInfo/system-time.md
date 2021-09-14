---
description: La hora del sistema es la fecha y hora actuales del día.
ms.assetid: 1a1e251e-2375-4134-bbd8-1e4670b9f9d2
title: Hora del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c727e8898fc2bc973d963c3a3c90524ca50958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243902"
---
# <a name="system-time"></a>Hora del sistema

*La hora del* sistema es la fecha y hora actuales del día. El sistema mantiene el tiempo para que las aplicaciones tengan acceso listo a la hora precisa. El sistema basa la hora del sistema en *la hora universal coordinada* (UTC). La hora basada en UTC se define de forma flexible como la fecha y hora actuales del día en Greenwich, Irlanda.

Cuando el sistema se inicia por primera vez, establece la hora del sistema en un valor basado en el reloj en tiempo real del equipo y, a continuación, actualiza periódicamente la hora. Para recuperar la hora del sistema, use la [**función GetSystemTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) **GetSystemTime copia** la hora en una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contiene miembros individuales de mes, día, año, día de la semana, hora, minuto, segundo y milisegundos. Es fácil mostrar este formato a un usuario.

También puede obtener la hora del sistema en formato de hora de archivo mediante la [**función GetSystemTimeAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) **GetSystemTimeAsFileTime copia** la hora en una [**estructura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

Para establecer la hora del sistema, use la [**función SetSystemTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) **SetSystemTime** supone que ha especificado una hora basada en UTC.

Las [**funciones GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment) y [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment) sincronizan el reloj de hora del día con otro origen de hora mediante un ajuste de hora periódico aplicado en cada interrupción del reloj.

Tenga en cuenta que el sistema puede actualizar periódicamente la hora mediante la sincronización con un origen de hora. Dado que la hora del sistema se puede ajustar hacia delante o hacia atrás, no compare las lecturas de hora del sistema para determinar el tiempo transcurrido. En su lugar, use uno de los métodos descritos [en Windows Time](windows-time.md).

 

 
