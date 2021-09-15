---
title: Iniciar un ejecutable en un momento específico
description: La escritura de una tarea que inicia un ejecutable en un momento específico se realiza mediante la definición de un desencadenador de hora y una acción ejecutable.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Programador de tareas ejemplos Programador de tareas , desencadenador de tiempo
- Programador de tareas ejemplos Programador de tareas , iniciar un archivo ejecutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474664"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Iniciar un ejecutable en un momento específico

La escritura de una tarea que inicia un ejecutable en un momento específico se realiza mediante la definición de un desencadenador de hora y una acción ejecutable.

## <a name="start-boundary"></a>Límite de inicio

Es importante tener en cuenta que un desencadenador de hora es diferente de otros desencadenadores basados en el tiempo en que se desencadena cuando el desencadenador se activa por su límite de inicio. Otros desencadenadores basados en tiempo se activan por su límite de inicio, pero no comienzan a realizar sus acciones (en este caso, iniciando un ejecutable) hasta que se alcanza una fecha programada.

## <a name="time-trigger-examples"></a>Ejemplos de desencadenador de tiempo

Los ejemplos siguientes comienzan Bloc de notas 30 segundos después de activar la tarea:

-   [Ejemplo de desencadenador de tiempo (C++)](time-trigger-example--c---.md)
-   [Ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md)
-   [Ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




