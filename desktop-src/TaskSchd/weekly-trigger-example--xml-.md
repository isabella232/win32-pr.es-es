---
title: Ejemplo de desencadenador semanal (XML)
description: El XML de este ejemplo define una tarea que inicia el Bloc de notas semanalmente.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104420124"
---
# <a name="weekly-trigger-example-xml"></a>Ejemplo de desencadenador semanal (XML)

El XML de este ejemplo define una tarea que inicia el Bloc de notas semanalmente.

Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Para definir una tarea para iniciar el Bloc de notas cada dos semanas el lunes a las 8:00 A.M.

En el ejemplo de XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (iniciando el Bloc de notas), un único desencadenador de calendario (inicia la tarea cada dos semanas el lunes a las 8:00 A.M.) y otras opciones de configuración de tareas que afectan al modo en que la tarea se controla mediante Programador de tareas.


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

Estos son algunos elementos importantes que se deben tener en cuenta al usar este ejemplo.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contiene información de registro sobre la tarea.

-   [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md)

    Define el desencadenador que inicia la tarea.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Define el desencadenador de calendario semanal. En este caso, solo se usan cuatro elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador, la programación semanal y los días de la semana en los que se ejecutará la tarea. El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de calendario.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Define la programación semanal. En este caso, el intervalo se establece para realizar la tarea cada dos semanas el lunes.

-   [**Principal**](taskschedulerschema-principal-principaltype-element.md)

    Define el contexto de seguridad en el que se ejecuta una tarea.

-   [**Configuración**](taskschedulerschema-settings-tasktype-element.md)

    Define la configuración de la tarea que Programador de tareas usa para realizar la tarea.

-   [**Acciones**](taskschedulerschema-actions-tasktype-element.md)

    Define las acciones que realiza la tarea (en este caso, ejecutar el Bloc de notas).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




