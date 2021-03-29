---
title: Iniciar un archivo ejecutable en el arranque del sistema
description: La escritura de una tarea que inicia un ejecutable cuando se arranca un sistema se realiza mediante la definición de un desencadenador de arranque y una acción ejecutable.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Programador de tareas ejemplos Programador de tareas, desencadenador de arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778114"
---
# <a name="starting-an-executable-on-system-boot"></a>Iniciar un archivo ejecutable en el arranque del sistema

La escritura de una tarea que inicia un ejecutable cuando se arranca un sistema se realiza mediante la definición de un desencadenador de arranque y una acción ejecutable.

## <a name="boot-trigger"></a>Desencadenador de arranque

Los desencadenadores de arranque se activan por su límite de inicio, pero no inician el ejecutable hasta que se inicia el sistema. También puede especificar un tiempo de retraso en el desencadenador de arranque que especifica la cantidad de tiempo que transcurre entre el momento en que se arranca el sistema y el momento en que se inicia la tarea. Se define mediante la propiedad [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) en la interfaz [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (objeto [**BootTrigger**](boottrigger.md) para scripting).

## <a name="boot-trigger-examples"></a>Ejemplos de desencadenadores de arranque

En los siguientes ejemplos se inicia el Bloc de notas después de arrancar el sistema:

-   [Ejemplo de desencadenador de arranque (scripting)](boot-trigger-example--scripting-.md)
-   [Ejemplo de desencadenador de arranque (C++)](boot-trigger-example--c---.md)
-   [Ejemplo de desencadenador de arranque (XML)](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




