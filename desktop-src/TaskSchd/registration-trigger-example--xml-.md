---
title: Ejemplo de desencadenador de registro (XML)
description: El XML de este ejemplo define una tarea que se inicia Bloc de notas cuando se registra la tarea.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172925"
---
# <a name="registration-trigger-example-xml"></a>Ejemplo de desencadenador de registro (XML)

El XML de este ejemplo define una tarea que se inicia Bloc de notas cuando se registra la tarea.

Para registrar una tarea definida en XML, puede usar la función [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) para scripting) o la herramienta de línea de comandos Schtasks.exe. Si usa la herramienta Schtasks.exe (ubicada en el directorio C: Windows System32), puede usar el siguiente comando para registrar la \\ \\ tarea: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

> [!Note]  
> Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>Para definir una tarea para iniciar Bloc de notas en el registro

En el ejemplo XML siguiente se muestra cómo definir una tarea con una sola acción de ejecución (a partir de Bloc de notas), un desencadenador de registro único que inicia la tarea cuando se registra y otras opciones de configuración de tareas que afectan a cómo controla la tarea el Programador de tareas.

> [!Note]  
> Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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

Estos son algunos elementos importantes que hay que tener en cuenta al usar este ejemplo.

-   [**RegistrationInfo:**](taskschedulerschema-registrationinfo-tasktype-element.md)contiene información de registro sobre la tarea.
-   [**Desencadenadores:**](taskschedulerschema-triggers-tasktype-element.md)define el desencadenador que inicia la tarea.
-   [**RegistrationTrigger:**](taskschedulerschema-registrationtrigger-triggergroup-element.md)define el desencadenador de registro. En este caso, solo se usan dos elementos secundarios: los límites inicial y final que especifican cuándo se activa y desactiva el desencadenador.
-   [**Entidad**](taskschedulerschema-principal-principaltype-element.md)de seguridad: define el contexto de seguridad en el que se ejecuta una tarea.
-   [**Configuración:**](taskschedulerschema-settings-tasktype-element.md)define la configuración de la tarea que Programador de tareas utiliza para realizar la tarea.
-   [**Acciones:**](taskschedulerschema-actions-tasktype-element.md)define las acciones que realiza la tarea. En este caso, se ejecuta Bloc de notas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




