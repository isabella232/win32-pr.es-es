---
title: Iniciar un archivo ejecutable en un momento específico
description: La escritura de una tarea que inicia un ejecutable en un momento determinado se realiza definiendo un desencadenador de tiempo y una acción ejecutable.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Programador de tareas ejemplos Programador de tareas, Time Trigger
- Programador de tareas ejemplos Programador de tareas, iniciar un archivo ejecutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903652"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Iniciar un archivo ejecutable en un momento específico

La escritura de una tarea que inicia un ejecutable en un momento determinado se realiza definiendo un desencadenador de tiempo y una acción ejecutable.

## <a name="start-boundary"></a>Límite de inicio

Es importante tener en cuenta que un desencadenador de tiempo es diferente de otros desencadenadores basados en tiempo en que se activa cuando el desencadenador se activa por su límite de inicio. Los otros desencadenadores basados en el tiempo se activan por su límite de inicio, pero no comienzan a realizar sus acciones (en este caso, iniciar un ejecutable) hasta que se alcanza una fecha programada.

## <a name="time-trigger-examples"></a>Ejemplos de desencadenadores Time

En los siguientes ejemplos se inicia el Bloc de notas 30 segundos después de activar la tarea:

-   [Ejemplo de desencadenador de tiempo (C++)](time-trigger-example--c---.md)
-   [Ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md)
-   [Ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




