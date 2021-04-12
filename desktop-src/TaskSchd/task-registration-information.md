---
title: Información de registro de tareas
description: La información de registro proporciona una manera de identificar una tarea de varias maneras diferentes. Por ejemplo, una tarea puede identificarla el autor, cómo se creó (denominada origen de la tarea) y la fecha del registro.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Programador de tareas de información de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356680"
---
# <a name="task-registration-information"></a>Información de registro de tareas

La información de registro proporciona una manera de identificar una tarea de varias maneras diferentes. Por ejemplo, una tarea puede identificarla el autor, cómo se creó (denominada origen de la tarea) y la fecha del registro.

## <a name="using-registration-information"></a>Usar información de registro

Normalmente, la información de registro se especifica cuando se crea la tarea y, a continuación, se usa de las siguientes maneras:

-   Lo muestra la interfaz de usuario de Programador de tareas.
-   Obtener o establecer por aplicaciones o scripts de C++.
-   En un entorno empresarial, se usa como criterio de búsqueda al enumerar todas las tareas registradas.

## <a name="types-of-registration-information"></a>Tipos de información de registro

La información de registro de tareas se define mediante las propiedades del objeto [**RegistrationInfo**](registrationinfo.md) para las aplicaciones de scripting, las propiedades de la interfaz [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) para las aplicaciones de C++ y los elementos secundarios del [**elemento RegistrationInfo (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) para leer o escribir en XML.

Estas propiedades permiten el acceso a los siguientes tipos de información de registro:

-   Autor de la tarea

    Programador de tareas establece el autor de la tarea cuando se crea.

-   Fecha de registro de tarea

    Programador de tareas establece esta fecha cuando se registra la tarea.

-   Descripción de la tarea

    Descripción definida por el usuario que puede incluir los desencadenadores que se usan para iniciar la tarea o las acciones que realiza la tarea.

-   Documentación de la tarea

    Documentación proporcionada por el usuario que necesita la tarea.

-   Descriptor de seguridad de tarea

    Un descriptor de seguridad proporcionado por el usuario.

-   Origen de la tarea

    Información proporcionada por el usuario que describe dónde se originó la tarea. Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.

-   URI de la tarea

    Identificador uniforme de recursos (URI) para la tarea.

-   Versión de la tarea

    Información proporcionada por el usuario que se utiliza cuando existen varias versiones de una tarea.

-   Texto XML

    Una versión con formato XML de la información de registro. Tenga en cuenta que puede establecer o modificar la información de registro directamente a través de este XML y las propiedades de interfaz y objeto adecuadas se actualizarán en consecuencia.

## <a name="registering-tasks"></a>Registro de tareas

Una tarea se puede registrar una vez que se han creado las definiciones de tarea y el usuario proporciona la información de registro y los valores de configuración. Una tarea se registra mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) para las aplicaciones de scripting o el método [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) para las aplicaciones de C++. Si desea registrar una tarea mediante XML para definir la tarea, use el método [**TaskFolder. RegisterTask**](taskfolder-registertask.md) para las aplicaciones de scripting y el método [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) para las aplicaciones de C++.

En los métodos mencionados anteriormente, puede especificar el contexto de seguridad para ejecutar la tarea. Debe ser administrador en el sistema para programar trabajos para que se ejecuten en contextos que no sean los suyos propios. Para obtener más información sobre los contextos de seguridad para ejecutar tareas, vea [contextos de seguridad para ejecutar tareas](security-contexts-for-running-tasks.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 




