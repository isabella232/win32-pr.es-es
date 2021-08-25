---
description: Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modelo de tareas con privilegios elevados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa485c47983760cc260a97cb52b58316a0d87bd4083d3ed09e72032f8fc7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672325"
---
# <a name="elevated-task-model"></a>Modelo de tareas con privilegios elevados

En el modelo de tareas con privilegios elevados, una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.

**Windows Server 2003 y Windows XP:** No se admite el modelo de tareas con privilegios elevados.

Las tareas no consumen tantos recursos del sistema como servicios y las tareas se cierran automáticamente cuando finalizan. Considere la posibilidad de usar este modelo en lugar del [modelo de servicio de sistema](operating-system-service-model.md) operativo a menos que sea necesaria la compatibilidad con versiones anteriores con sistemas operativos anteriores.

Para usar una tarea para realizar operaciones con privilegios para una aplicación de usuario estándar, deben cumplirse las condiciones siguientes:

-   La tarea debe establecerse para ejecutarse como **SYSTEM**.
-   El [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) asociado a la tarea debe configurarse para permitir que los usuarios estándar inicien la tarea.
-   El servicio del programador de tareas debe estar en ejecución.

Para obtener información sobre cómo crear e iniciar tareas, [vea Programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de agente de administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objetos COM de administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de servicio de sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
