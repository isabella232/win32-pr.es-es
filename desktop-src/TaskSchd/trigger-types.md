---
title: Tipos de desencadenador
description: Los desencadenadores basados en tiempo y en eventos que se describen a continuación le permiten iniciar tareas de diversas maneras.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- desencadenadores Programador de tareas, tipos
- Programador de tareas de desencadenador de arranque
- Programador de tareas de desencadenador de arranque, descrito
- Programador de tareas de desencadenador de registro
- Programador de tareas de desencadenador de registro, descrito
- Programador de tareas de desencadenador de calendario
- Programador de tareas de desencadenador de calendario, descrito
- Programador de tareas de desencadenador diario
- Programador de tareas de desencadenador diario, descrito
- Programador de tareas de desencadenador semanal
- Programador de tareas de desencadenador semanal, descrito
- Programador de tareas de desencadenador mensual
- Programador de tareas de desencadenador mensual, descrito
- Programador de tareas de desencadenador monthlyDOW
- Programador de tareas de desencadenador monthlyDOW, descrito
- desencadenador de evento Programador de tareas
- desencadenador de eventos Programador de tareas, descrito
- Programador de tareas de desencadenador Logon
- Programador de tareas de desencadenador Logon, descrito
- desencadenador inactivo Programador de tareas
- desencadenador inactivo Programador de tareas, descrito
- Programador de tareas del desencadenador del día de la semana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee1e846e4b2fa8138f675cdd39e926884d2bfae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685778"
---
# <a name="trigger-types"></a>Tipos de desencadenador

Los desencadenadores basados en tiempo y en eventos que se describen a continuación le permiten iniciar tareas de diversas maneras.

## <a name="task-scheduler-20-triggers"></a>Desencadenadores Programador de tareas 2,0

Los siguientes tipos de desencadenadores se definen mediante la enumeración [**\_ \_ tipo2 del desencadenador de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .

| Desencadenador                                                                                                                                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desencadenador de eventos (desencadenador basado en eventos) para el desarrollo de scripting, vea [**EventTrigger**](eventtrigger.md).<br/> Para el desarrollo de C++, vea [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Para el desarrollo de XML, vea [**elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Inicia la tarea cuando se produce un evento de sistema específico.                                                                                                                                         |
| Desencadenador de tiempo (desencadenador basado en tiempo) para el desarrollo de scripting, vea [**TimeTrigger**](timetrigger.md).<br/> Para el desarrollo de C++, vea [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Para el desarrollo de XML, vea [**elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Inicia la tarea en una fecha y hora específicas.                                                                                                                                                 |
| Desencadenador diario (desencadenador de calendario basado en el tiempo) para el desarrollo de scripts, vea [**DailyTrigger**](dailytrigger.md).<br/> Para el desarrollo de C++, vea [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Para el desarrollo de XML, vea [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Inicia la tarea a una hora específica en una programación diaria. Por ejemplo, la tarea comienza a las 8:00 AM cada día o cada día.                                                                |
| Desencadenador semanal (desencadenador de calendario basado en el tiempo) para el desarrollo de scripts, vea [**WeeklyTrigger**](weeklytrigger.md).<br/> Para el desarrollo de C++, vea [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Para el desarrollo de XML, vea [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Inicia la tarea a una hora específica según una programación semanal. Por ejemplo, la tarea comienza a las 8:00 A.M. en un día concreto de la semana cada semana o en un día concreto de la semana, cada dos semanas. |
| Desencadenador mensual (desencadenador de calendario basado en el tiempo) para el desarrollo de scripts, vea [**MonthlyTrigger**](monthlytrigger.md).<br/> Para el desarrollo de C++, vea [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Para el desarrollo de XML, vea [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Inicia la tarea a una hora específica según una programación mensual. Por ejemplo, la tarea comienza a las 8:00 AM en días específicos del mes en meses específicos.                                          |
| Desencadenador de día de la semana (DOW) mensual (desencadenador de calendario basado en el tiempo) para el desarrollo de scripts, vea [**MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Para el desarrollo de C++, vea [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Para el desarrollo de XML, vea [**elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Inicia la tarea a una hora específica en una programación mensual de día de la semana. Por ejemplo, la tarea comienza a las 8:00 AM en días específicos de la semana, semanas del mes y meses del año.      |
| Desencadenador inactivo (desencadenador basado en eventos) para el desarrollo de scripting, vea [**IdleTrigger**](idletrigger.md).<br/> Para el desarrollo de C++, vea [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger).<br/> Para el desarrollo de XML, vea [**elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia la tarea cuando el equipo entra en un estado de inactividad.                                                                                                                                      |
| Desencadenador de registro (desencadenador basado en eventos) para el desarrollo de scripting, vea [**RegistrationTrigger**](registrationtrigger.md).<br/> Para el desarrollo de C++, vea [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger).<br/> Para el desarrollo de XML, vea [**elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Inicia la tarea cuando la tarea se registra o se actualiza.                                                                                                                                      |
| Desencadenador de arranque (desencadenador basado en eventos) para el desarrollo de scripting, vea [**BootTrigger**](boottrigger.md).<br/> Para el desarrollo de C++, vea [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Para el desarrollo de XML, vea [**elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia la tarea cuando se inicia el sistema.                                                                                                                                                   |
| Desencadenador de inicio de sesión (desencadenador basado en eventos) para el desarrollo de scripts, vea [**LogonTrigger**](logontrigger.md).<br/> Para el desarrollo de C++, vea [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Para el desarrollo de XML, vea [**elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Inicia la tarea cuando un usuario inicia sesión.                                                                                                                                                         |
| Desencadenador de cambios de estado de sesión (desencadenador basado en eventos) para el desarrollo de scripts, vea [**SessionStateChangeTrigger**](sessionstatechangetrigger.md).<br/> Para el desarrollo de C++, vea [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger).<br/> Para el desarrollo de XML, vea [**elemento SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Inicia la tarea cuando se cambia el estado de una sesión de Terminal Server.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Desencadenadores Programador de tareas 1,0

Los siguientes tipos de desencadenadores se definen mediante la enumeración de [**\_ \_ tipo de desencadenador de tarea**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) . Para implementar cualquiera de los siguientes desencadenadores, consulte la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea.

-   Desencadenador once: inicia la tarea una sola vez.
-   Desencadenador diario: inicia la tarea en un intervalo diario.
-   Desencadenador semanal: inicia la tarea según una programación semanal.
-   Desencadenador mensual: inicia la tarea con una programación mensual.
-   Desencadenador de DOW mensual: inicia la tarea en un programa de día de la semana mensual.
-   En el desencadenador inactivo: inicia la tarea cuando el equipo está en un estado de inactividad.
-   Desencadenador de inicio del sistema: inicia la tarea cuando se inicia el equipo.
-   Desencadenador Logon: inicia la tarea cuando un usuario específico inicia sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> <dt>

[Interfaces de desencadenador](trigger-interfaces.md)
</dt> <dt>

[Estructuras de desencadenador](trigger-structures.md)
</dt> </dl>

 

