---
title: Desencadenadores de tareas
description: Un desencadenador es un conjunto de criterios que, si se cumplen, inicia la ejecución de una tarea.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- crear desencadenadores Programador de tareas
- desencadenadores Programador de tareas
- desencadenadores Programador de tareas , descrito
- desencadenadores Programador de tareas , basado en el tiempo
- desencadenadores Programador de tareas , basado en eventos
- desencadenadores basados en eventos Programador de tareas
- desencadenadores basados en tiempo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0060511556615c638eb8385a757e9c44147720b659bb11bfe4f0849e4499ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002303"
---
# <a name="task-triggers"></a>Desencadenadores de tareas

Un desencadenador es un conjunto de criterios que, si se cumplen, inicia la ejecución de una tarea. Programador de tareas proporciona desencadenadores basados en eventos y basados en tiempo que pueden iniciar una tarea de varias maneras diferentes. Una tarea determinada se puede iniciar mediante uno o varios desencadenadores. Una tarea puede tener un máximo de 48 desencadenadores.

## <a name="time-based-triggers"></a>Desencadenadores basados en tiempo

Los desencadenadores basados en el tiempo inician tareas en momentos especificados. Esto incluye iniciar la tarea una vez a una hora específica o iniciar la tarea varias veces en una programación diaria, semanal, mensual o mensual del día de la semana.

## <a name="event-based-triggers"></a>Desencadenadores basados en eventos

Los desencadenadores basados en eventos inician una tarea en respuesta a unos determinados eventos del sistema. Por ejemplo, los desencadenadores basados en eventos se pueden establecer para iniciar una tarea cuando se inicia el sistema, cuando un usuario inicia sesión en el equipo local o cuando el sistema se vuelve inactivo.

## <a name="multiple-triggers"></a>Desencadenadores múltiples

Cada tarea se puede iniciar mediante uno o varios desencadenadores, lo que permite que la tarea se pueda iniciar de varias maneras. Sin embargo, varios desencadenadores se implementan de forma diferente en Programador de tareas 1.0 y Programador de tareas 2.0.

En Programador de tareas 2.0, cada desencadenador se define mediante una API de desencadenador independiente que está asociada a la tarea a través de la colección de desencadenadores.

En Programador de tareas 1.0, se pueden pensar en varios desencadenadores como una programación, un conjunto de horas en las que se inicia la tarea. En este caso, la programación es el conjunto de horas (especificadas por la unión de todos los desencadenadores asociados al elemento de trabajo) en las que se ejecutará un elemento de trabajo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Repetir una tarea](repeating-a-task.md)
</dt> <dt>

[Tipos de desencadenador](trigger-types.md)
</dt> <dt>

[Interfaces de desencadenador](trigger-interfaces.md)
</dt> <dt>

[Acerca de la Programador de tareas](about-the-task-scheduler.md)
</dt> </dl>

 

 




