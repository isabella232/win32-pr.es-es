---
title: Tipos de desencadenador
description: Los desencadenadores basados en tiempo y basados en eventos que se describen a continuación permiten iniciar tareas de varias maneras.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- desencadenadores Programador de tareas , tipos
- desencadenador de arranque Programador de tareas
- desencadenador de arranque Programador de tareas , descrito
- registro del desencadenador Programador de tareas
- desencadenador de registro Programador de tareas , descrito
- calendar trigger Programador de tareas
- desencadenador de calendario Programador de tareas , descrito
- desencadenador diario Programador de tareas
- desencadenador diario Programador de tareas , descrito
- desencadenador semanal Programador de tareas
- desencadenador semanal Programador de tareas , descrito
- desencadenador mensual Programador de tareas
- desencadenador mensual Programador de tareas , descrito
- desencadenador monthlyDOW Programador de tareas
- desencadenador monthlyDOW Programador de tareas , descrito
- desencadenador de eventos Programador de tareas
- desencadenador de eventos Programador de tareas , descrito
- inicio de sesión de desencadenador Programador de tareas
- inicio de sesión de Programador de tareas , descrito
- desencadenador inactivo Programador de tareas
- desencadenador inactivo Programador de tareas , descrito
- desencadenador del día de la semana Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0e09b6ecc1ac3c817f374e70c6756fa09afc78ccaac7e549f3f04ad074c8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099695"
---
# <a name="trigger-types"></a>Tipos de desencadenador

Los desencadenadores basados en tiempo y basados en eventos que se describen a continuación permiten iniciar tareas de varias maneras.

## <a name="task-scheduler-20-triggers"></a>Programador de tareas desencadenadores 2.0

La enumeración TASK TRIGGER [**\_ \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) define los siguientes tipos de desencadenador.

| Desencadenador                                                                                                                                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desencadenador de eventos (desencadenador basado en eventos) Para el desarrollo de scripting, vea [**EventTrigger**](eventtrigger.md).<br/> Para el desarrollo de C++, [**vea IEventTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)<br/> Para el desarrollo XML, [**vea Elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Inicia la tarea cuando se produce un evento del sistema específico.                                                                                                                                         |
| Desencadenador de tiempo (desencadenador basado en tiempo)Para el desarrollo de scripting, vea [**TimeTrigger**](timetrigger.md).<br/> Para el desarrollo de C++, vea [**ITimeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)<br/> Para el desarrollo XML, vea [**Elemento TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Inicia la tarea en una fecha y hora específicas.                                                                                                                                                 |
| Desencadenador diario (desencadenador de calendario basado en tiempo)Para el desarrollo de scripting, vea [**DailyTrigger**](dailytrigger.md).<br/> Para el desarrollo de C++, [**vea IDailyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)<br/> Para el desarrollo XML, vea [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Inicia la tarea a una hora específica según una programación diaria. Por ejemplo, la tarea se inicia a las 8:00 a. m. todos los días o cada dos días.                                                                |
| Desencadenador semanal (desencadenador de calendario basado en tiempo)Para el desarrollo de scripting, vea [**WeeklyTrigger**](weeklytrigger.md).<br/> Para el desarrollo de C++, [**vea IWeeklyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)<br/> Para el desarrollo XML, vea [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Inicia la tarea en un momento específico según una programación semanal. Por ejemplo, la tarea se inicia a las 8:00 a. m. en un día específico de la semana cada semana o en un día específico de la semana cada dos semanas. |
| Desencadenador mensual (desencadenador de calendario basado en tiempo)Para el desarrollo de scripting, [**vea MonthlyTrigger**](monthlytrigger.md).<br/> Para el desarrollo de C++, [**vea IMonthlyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)<br/> Para el desarrollo XML, vea [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Inicia la tarea a una hora específica según una programación mensual. Por ejemplo, la tarea se inicia a las 8:00 a. m. en días específicos del mes en meses específicos.                                          |
| Desencadenador mensual del día de la semana (DOW) (desencadenador de calendario basado en tiempo)Para el desarrollo de scripting, [**vea MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Para el desarrollo de C++, [**vea IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Para el desarrollo XML, vea [**Elemento CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Inicia la tarea a una hora específica según una programación mensual del día de la semana. Por ejemplo, la tarea se inicia a las 8:00 a. m. en días específicos de la semana, semanas del mes y meses del año.      |
| Desencadenador inactivo (desencadenador basado en eventos)Para el desarrollo de scripting, vea [**IdleTrigger**](idletrigger.md).<br/> Para el desarrollo de C++, vea [**IIdleTrigger.**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)<br/> Para el desarrollo XML, vea [**Elemento IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia la tarea cuando el equipo entra en un estado de inactividad.                                                                                                                                      |
| Desencadenador de registro (desencadenador basado en eventos)Para el desarrollo de scripting, vea [**RegistrationTrigger**](registrationtrigger.md).<br/> Para el desarrollo de C++, [**vea IRegistrationTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)<br/> Para el desarrollo XML, vea [**Elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Inicia la tarea cuando la tarea se registra o actualiza.                                                                                                                                      |
| Desencadenador de arranque (desencadenador basado en eventos)Para el desarrollo de scripting, vea [**BootTrigger**](boottrigger.md).<br/> Para el desarrollo de C++, [**vea IBootTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)<br/> Para el desarrollo XML, vea [**Elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Inicia la tarea cuando se arranca el sistema.                                                                                                                                                   |
| Desencadenador de inicio de sesión (desencadenador basado en eventos)Para el desarrollo de scripting, vea [**LogonTrigger**](logontrigger.md).<br/> Para el desarrollo de C++, [**vea ILogonTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)<br/> Para el desarrollo XML, vea [**Elemento LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Inicia la tarea cuando un usuario inicia sesión.                                                                                                                                                         |
| Desencadenador de cambio de estado de sesión (desencadenador basado en eventos)Para el desarrollo de scripting, vea [**SessionStateChangeTrigger**](sessionstatechangetrigger.md).<br/> Para el desarrollo de C++, [**vea ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger)<br/> Para el desarrollo XML, vea [**Elemento SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Inicia la tarea cuando una sesión de Terminal Server cambia de estado.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Programador de tareas desencadenadores 1.0

La enumeración TASK TRIGGER TYPE define los siguientes tipos [**\_ de \_ desencadenador.**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) Para implementar cualquiera de los siguientes desencadenadores, vea la [**estructura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)

-   Desencadenador una vez: inicia la tarea una sola vez.
-   Desencadenador diario: inicia la tarea en un intervalo diario.
-   Desencadenador semanal: inicia la tarea según una programación semanal.
-   Desencadenador mensual: inicia la tarea según una programación mensual.
-   Desencadenador DOW mensual: inicia la tarea según una programación mensual del día de la semana.
-   En desencadenador inactivo: inicia la tarea cuando el equipo está en estado de inactividad.
-   Desencadenador de inicio del sistema: inicia la tarea cuando se arranca el equipo.
-   Desencadenador de inicio de sesión: inicia la tarea cuando un usuario específico inicia sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> <dt>

[Interfaces de desencadenador](trigger-interfaces.md)
</dt> <dt>

[Estructuras de desencadenador](trigger-structures.md)
</dt> </dl>

 

