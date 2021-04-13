---
title: Interfaces de desencadenador
description: Las API que se usan para administrar los desencadenadores varían en función de la versión de la Programador de tareas. Sin embargo, en ambos casos estas API le permiten crear nuevos desencadenadores, recuperar y actualizar los desencadenadores existentes, y eliminar los desencadenadores que ya no son necesarios.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- desencadenadores Programador de tareas, interfaces
- desencadenadores Programador de tareas, interfaces, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359534"
---
# <a name="trigger-interfaces"></a>Interfaces de desencadenador

Las API que se usan para administrar los desencadenadores varían en función de la versión de la Programador de tareas. Sin embargo, en ambos casos estas API le permiten crear nuevos desencadenadores, recuperar y actualizar los desencadenadores existentes, y eliminar los desencadenadores que ya no son necesarios.


Las aplicaciones desarrolladas con Programador de tareas 2,0 pueden utilizar objetos e interfaces para crear, recuperar, modificar y eliminar los desencadenadores de una tarea.

En la ilustración siguiente, una tarea especifica una colección de desencadenadores mediante su propiedad Triggers. Esta colección contiene una o varias API de desencadenador individual con cada API que especifica un tipo de desencadenador específico. Por ejemplo, en la ilustración siguiente, la colección de desencadenadores contiene un desencadenador de arranque, un desencadenador de inicio de sesión y un desencadenador diario.

![interfaces de desencadenador del programador de tareas 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>API de objetos para el desarrollo de scripting

Para obtener más información sobre los métodos y las propiedades de los objetos que se usan para especificar los desencadenadores, vea:

-   [**TaskDefinition**](taskdefinition.md)
-   [**TriggerCollection**](triggercollection.md)
-   [**Activado**](trigger.md)
-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>Interfaces API para el desarrollo en C++

Para obtener más información sobre los métodos y las propiedades de las interfaces que se usan para especificar los desencadenadores, vea:

-   [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Interfaces de desencadenador de Programador de tareas 1,0

Las aplicaciones existentes desarrolladas con Programador de tareas 1,0 pueden usar los métodos que están disponibles en las interfaces de Programador de tareas 1,0 para crear, recuperar, modificar y eliminar los desencadenadores de un [*elemento de trabajo*](w.md). Sin embargo, tenga en cuenta que todas las interfaces Programador de tareas 1,0, enumeraciones y estructuras están obsoletas y no deben usarse para el desarrollo de nuevas aplicaciones.

En la ilustración siguiente se muestran las dos interfaces que se usan para hacerlo. La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) se usa para administrar todos los desencadenadores asociados a un elemento de trabajo (tal administración incluye la creación de un nuevo desencadenador para el elemento de trabajo). La interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) se usa para administrar un desencadenador específico.

![interfaces de desencadenador del programador de tareas 1,0](images/tsktri2.png)

La interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) proporciona métodos para crear un nuevo desencadenador para un elemento de trabajo, recuperar el número de desencadenadores asociados a un elemento de trabajo, recuperar las [*estructuras de desencadenador*](t.md) asociadas al elemento de trabajo, recuperar cadenas de [*desencadenador*](t.md) asociadas al elemento de trabajo y eliminar desencadenadores.

Una vez que el objeto de desencadenador está disponible, puede usar la interfaz [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar la estructura del desencadenador y la cadena del desencadenador y para establecer los criterios que se utilizan para activar el desencadenador. Esta interfaz solo se usa cuando se trabaja con un [*objeto de desencadenador de tarea*](t.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> <dt>

[Tipos de desencadenador](trigger-types.md)
</dt> <dt>

[Estructuras de desencadenador](trigger-structures.md)
</dt> </dl>

 

 