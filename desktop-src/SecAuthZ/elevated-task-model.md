---
description: Una aplicación que se ejecuta como usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modelo de tareas elevado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361385"
---
# <a name="elevated-task-model"></a>Modelo de tareas elevado

En el modelo de tareas elevado, una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.

**Windows Server 2003 y Windows XP:** No se admite el modelo de tareas elevado.

Las tareas no consumen tantos recursos del sistema como servicios y las tareas se cierran automáticamente cuando finalizan. Considere la posibilidad de usar este modelo en lugar del [modelo de servicio del sistema operativo](operating-system-service-model.md) , a menos que sea necesaria la compatibilidad con versiones anteriores de los sistemas operativos anteriores.

Para utilizar una tarea para realizar operaciones con privilegios en una aplicación de usuario estándar, deben cumplirse las siguientes condiciones:

-   La tarea debe estar establecida en ejecutar como **sistema**.
-   El [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) asociado a la tarea debe configurarse para permitir que los usuarios estándar inicien la tarea.
-   El servicio Programador de tareas debe estar en ejecución.

Para obtener información sobre cómo crear e iniciar tareas, vea [programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de agente de administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de objetos COM de administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de servicio del sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
