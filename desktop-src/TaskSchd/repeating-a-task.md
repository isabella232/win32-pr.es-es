---
title: Repetir una tarea
description: Programador de tareas puede ejecutar una tarea cualquier número de veces después de que se desencadene un desencadenador.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- patrón de repetición Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357410"
---
# <a name="repeating-a-task"></a>Repetir una tarea

Programador de tareas puede ejecutar una tarea cualquier número de veces después de que se desencadene un desencadenador. Para ello, el desencadenador define un patrón de repetición que indica Programador de tareas cuánto tiempo debe continuar repitiendo la tarea y el intervalo de tiempo entre cada repetición de tarea.

## <a name="repetition-pattern"></a>Patrón de repetición

En la ilustración siguiente se muestra un patrón de repetición con una duración de 60 minutos y un intervalo de 25 minutos. Tenga en cuenta que, en este caso, Programador de tareas ejecuta la tarea cuando se activa el desencadenador, vuelve a ejecutar la tarea después de 25 minutos y, a continuación, vuelve a ejecutar la tarea después de 50 minutos, según el valor de la [**propiedad StopAtDurationEnd de IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) para scripting). Si la propiedad **StopAtDurationEnd** está establecida en True, programador de tareas detiene la última instancia de la tarea si todavía se está ejecutando después de 60 minutos. Si la propiedad **StopAtDurationEnd** se establece en false, la última instancia de la tarea se ejecuta independientemente de la duración.

![patrón de repetición de desencadenador](images/repetition-pattern.png)

Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cinco veces. Las cinco repeticiones se pueden definir con el siguiente patrón:

1.  Una tarea comienza al principio del primer minuto.
2.  La siguiente tarea comienza al final del primer minuto.
3.  La siguiente tarea comienza al final del segundo minuto.
4.  La siguiente tarea comienza al final del tercer minuto.
5.  La siguiente tarea comienza al final del cuarto minuto.

**Windows Server 2003, Windows XP y windows 2000:** Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cuatro veces.

## <a name="objects-interfaces-and-xml-elements"></a>Objetos, interfaces y elementos XML

Para el desarrollo de scripting, el patrón de repetición se define mediante el objeto [**RepetitionPattern**](repetitionpattern.md) .

En el desarrollo de C++, el patrón de repetición se define mediante la interfaz [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .

Al leer o escribir XML para una tarea, el patrón de repetición se especifica en el elemento [**repite**](taskschedulerschema-repetition-triggerbasetype-element.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desencadenadores de tareas](task-triggers.md)
</dt> </dl>

 

 




