---
title: Ejemplo de desencadenador de arranque (XML)
description: En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas al arrancar el sistema.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104358613"
---
# <a name="boot-trigger-example-xml"></a>Ejemplo de desencadenador de arranque (XML)

En el código XML de este ejemplo se define una tarea que inicia el Bloc de notas al arrancar el sistema.

Para registrar una tarea que se define en XML, puede usar la función [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (que se encuentra en el directorio C: \\ Windows \\ system32), puede usar el siguiente comando para registrar la tarea: **Schtasks/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Para definir una tarea para iniciar el Bloc de notas en el arranque del sistema

En el ejemplo de XML siguiente se muestra cómo definir una tarea con una única acción de ejecución (iniciando el Bloc de notas), un único desencadenador de arranque que inicia la tarea cuando se arranca el sistema y otras opciones de configuración de tareas que afectan al modo en que la tarea la controla el Programador de tareas.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contiene información de registro sobre la tarea.
-   [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md): define el desencadenador que inicia la tarea.
-   [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): define el desencadenador de arranque. En este caso, solo se usan dos elementos secundarios: los límites inicial y final que especifican Cuándo se activa y desactiva el desencadenador.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): define el contexto de seguridad en el que se ejecuta una tarea.
-   [**Configuración**](taskschedulerschema-settings-tasktype-element.md): define la configuración de la tarea que utiliza el programador de tareas para realizar la tarea.
-   [**Acciones**](taskschedulerschema-actions-tasktype-element.md): define las acciones que realiza la tarea. En este caso, se ejecuta el Bloc de notas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




