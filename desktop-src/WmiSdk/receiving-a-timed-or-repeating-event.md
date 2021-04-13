---
description: Un evento de tiempo o repetición es un evento que se produce en una fecha y hora específicas, o repetidamente a intervalos regulares. Por ejemplo, un evento puede producirse a medianoche solo en el 2 de diciembre de 2015 o una vez cada semana los martes a las 2:31 P.M.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Recibir un evento de tiempo o repetición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276149"
---
# <a name="receiving-a-timed-or-repeating-event"></a>Recibir un evento de tiempo o repetición

Un evento de tiempo o repetición es un evento que se produce en una fecha y hora específicas, o repetidamente a intervalos regulares. Por ejemplo, un evento puede producirse a medianoche solo en el 2 de diciembre de 2015 o una vez cada semana los martes a las 2:31 P.M.

En la tabla siguiente se enumeran las distintas clases que se usan para crear un evento de tiempo o repetición.



| Clase                                                                                            | Descripción                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | Modelo de eventos estándar de Microsoft.<br/> Para obtener más información, vea [crear un evento de temporizador con Win32 \_ localtime o Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).<br/> |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                               | Técnica heredada.<br/> Para obtener más información, vea [crear un evento de temporizador con \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).<br/>                                             |



 

Si desea programar una tarea o un trabajo para que se produzca en un momento determinado o de forma repetida, utilice la clase [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) y sus métodos. Esta clase representa un trabajo creado con el comando AT en una ventana de comandos desde el **Inicio** y después **Ejecutar**, o desde las **tareas programadas** del **Panel de control**.

 

