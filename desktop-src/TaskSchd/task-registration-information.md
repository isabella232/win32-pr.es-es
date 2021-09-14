---
title: Información de registro de tareas
description: La información de registro proporciona una manera de identificar una tarea de varias maneras diferentes. Por ejemplo, el autor puede identificar una tarea, cómo se hizo (denominada origen de la tarea) y la fecha de registro.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- información de registro Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886452"
---
# <a name="task-registration-information"></a>Información de registro de tareas

La información de registro proporciona una manera de identificar una tarea de varias maneras diferentes. Por ejemplo, el autor puede identificar una tarea, cómo se hizo (denominada origen de la tarea) y la fecha de registro.

## <a name="using-registration-information"></a>Uso de la información de registro

La información de registro se especifica normalmente cuando se crea la tarea y, a continuación, se usa de las maneras siguientes:

-   Mostrado por la interfaz Programador de tareas usuario.
-   Obtiene o establece mediante scripts o aplicaciones de C++.
-   En un entorno empresarial, se usa como criterio de búsqueda al enumerar todas las tareas registradas.

## <a name="types-of-registration-information"></a>Tipos de información de registro

La información de registro de tareas se define mediante las propiedades del objeto [**RegistrationInfo**](registrationinfo.md) para las aplicaciones de scripting, las propiedades de la interfaz [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) para aplicaciones de C++ y los elementos secundarios del elemento [**RegistrationInfo (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) para leer o escribir XML.

Estas propiedades permiten el acceso a los siguientes tipos de información de registro:

-   Autor de la tarea

    Programador de tareas establece el autor de la tarea cuando se crea.

-   Fecha de registro de la tarea

    Programador de tareas establece esta fecha cuando se registra la tarea.

-   Descripción de la tarea

    Descripción definida por el usuario que puede incluir qué desencadenadores se usan para iniciar la tarea o qué acciones realiza la tarea.

-   Documentación de tareas

    Documentación proporcionada por el usuario que necesita la tarea.

-   Descriptor de seguridad de tareas

    Descriptor de seguridad proporcionado por el usuario.

-   Origen de la tarea

    Información proporcionada por el usuario que describe de dónde se originó la tarea. Por ejemplo, una tarea puede originarse en un componente, servicio, aplicación o usuario.

-   URI de tarea

    Identificador uniforme de recursos (URI) para la tarea.

-   Versión de la tarea

    Información proporcionada por el usuario que se usa cuando existen varias versiones de una tarea.

-   Texto XML

    Versión con formato XML de la información de registro. Tenga en cuenta que puede establecer o modificar la información de registro directamente a través de este XML y las propiedades de interfaz y objeto adecuadas se actualizarán en consecuencia.

## <a name="registering-tasks"></a>Registro de tareas

Una tarea se puede registrar después de crear las definiciones de tarea y el usuario proporciona la información de registro y los valores de configuración. Una tarea se registra mediante el [**método TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para crear scripts de aplicaciones o el método [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) para aplicaciones de C++. Si desea registrar una tarea mediante XML para definir la tarea, use el método [**TaskFolder.RegisterTask**](taskfolder-registertask.md) para crear scripts de aplicaciones y el método [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) para aplicaciones de C++.

En los métodos mencionados anteriormente, puede especificar el contexto de seguridad para ejecutar la tarea. Debe ser administrador en el sistema para programar trabajos que se ejecuten en contextos distintos de los suyos propios. Para obtener más información sobre los contextos de seguridad para ejecutar tareas, vea [Contextos de seguridad para ejecutar tareas](security-contexts-for-running-tasks.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 




