---
title: Ejemplo de desencadenador semanal (XML)
description: El código XML de este ejemplo define una tarea que Bloc de notas cada dos semanas.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474643"
---
# <a name="weekly-trigger-example-xml"></a>Ejemplo de desencadenador semanal (XML)

El código XML de este ejemplo define una tarea que Bloc de notas cada dos semanas.

Para registrar una tarea definida en XML, puede usar la función [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe de comandos. Si usa la herramienta Schtasks.exe (ubicada en el directorio C: Windows System32), puede usar el siguiente comando para registrar la \\ \\ tarea: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Para definir una tarea que se inicie cada Bloc de notas el lunes a las 8:00 a. m.

En el ejemplo XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (a partir de Bloc de notas), un desencadenador de calendario único (inicia la tarea cada dos semanas el lunes a las 8:00 a. m.) y otras configuraciones de tareas que afectan a la forma en que Programador de tareas controla la tarea.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
        </CalendarTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Elementos de esquema TaskScheduler

Estos son algunos elementos importantes que debe tener en cuenta al usar este ejemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contiene información de registro sobre la tarea.

-   [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md)

    Define el desencadenador que inicia la tarea.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Define el desencadenador de calendario semanal. En este caso, solo se usan cuatro elementos secundarios: los límites inicial y final que especifican cuándo se activa y desactiva el desencadenador, la programación semanal y los días de la semana en los que se ejecutará la tarea. El [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de calendario.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Define la programación semanal. En este caso, el intervalo se establece para realizar la tarea cada dos semanas en un lunes.

-   [**Principal**](taskschedulerschema-principal-principaltype-element.md)

    Define el contexto de seguridad en el que se ejecuta una tarea.

-   [**Configuración**](taskschedulerschema-settings-tasktype-element.md)

    Define la configuración de la tarea Programador de tareas utiliza para realizar la tarea.

-   [**Acciones**](taskschedulerschema-actions-tasktype-element.md)

    Define las acciones que realiza la tarea (en este caso, ejecutando Bloc de notas).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




