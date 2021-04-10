---
title: Desencadenadores de tareas
description: Un desencadenador es un conjunto de criterios que, si se cumplen, inicia la ejecución de una tarea.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- crear desencadenadores Programador de tareas
- desencadenadores Programador de tareas
- desencadenadores Programador de tareas, descritos
- desencadenadores Programador de tareas, basados en el tiempo
- desencadenadores Programador de tareas, basados en eventos
- desencadenadores basados en eventos Programador de tareas
- desencadenadores basados en tiempo Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268419"
---
# <a name="task-triggers"></a>Desencadenadores de tareas

Un desencadenador es un conjunto de criterios que, si se cumplen, inicia la ejecución de una tarea. Programador de tareas proporciona desencadenadores basados en tiempo y basados en eventos que pueden iniciar una tarea de varias maneras diferentes. Una tarea determinada puede iniciarse mediante uno o varios desencadenadores. Una tarea puede tener un máximo de 48 desencadenadores.

## <a name="time-based-triggers"></a>Desencadenadores basados en tiempo

Los desencadenadores basados en tiempo inician las tareas a las horas especificadas. Esto incluye el inicio de la tarea una vez a una hora específica o el inicio de la tarea varias veces en una programación diaria, semanal, mensual o mensual.

## <a name="event-based-triggers"></a>Desencadenadores basados en eventos

Los desencadenadores basados en eventos inician una tarea en respuesta a unos determinados eventos del sistema. Por ejemplo, los desencadenadores basados en eventos se pueden establecer para iniciar una tarea cuando se inicia el sistema, cuando un usuario inicia sesión en el equipo local o cuando el sistema se queda inactivo.

## <a name="multiple-triggers"></a>Desencadenadores múltiples

Cada tarea se puede iniciar mediante uno o varios desencadenadores, lo que permite iniciar la tarea de varias maneras. Sin embargo, se implementan varios desencadenadores de manera diferente en Programador de tareas 1,0 y Programador de tareas 2,0.

En Programador de tareas 2,0, cada desencadenador se define mediante una API de desencadenador independiente que está asociada a la tarea a través de la colección de desencadenadores.

En Programador de tareas 1,0, se pueden considerar varios desencadenadores como una programación, un conjunto de veces en que se inicia la tarea. En este caso, la programación es el conjunto de horas (especificado por la Unión de todos los desencadenadores asociados al elemento de trabajo) en el que se ejecutará un elemento de trabajo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Repetir una tarea](repeating-a-task.md)
</dt> <dt>

[Tipos de desencadenador](trigger-types.md)
</dt> <dt>

[Interfaces de desencadenador](trigger-interfaces.md)
</dt> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
</dt> </dl>

 

 




