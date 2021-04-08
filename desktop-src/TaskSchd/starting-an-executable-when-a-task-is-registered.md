---
title: Iniciar un archivo ejecutable cuando se registra una tarea
description: La escritura de una tarea que inicia un ejecutable cuando se registra una tarea se realiza mediante la definición de un desencadenador de registro y una acción ejecutable.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Programador de tareas ejemplos Programador de tareas, desencadenador de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994341"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Iniciar un archivo ejecutable cuando se registra una tarea

La escritura de una tarea que inicia un ejecutable cuando se registra una tarea se realiza mediante la definición de un desencadenador de registro y una acción ejecutable.

## <a name="registration-trigger"></a>Desencadenador de registro

Los desencadenadores de registro inician una tarea en cuanto se registra. También puede especificar un retraso para el desencadenador de registro, que inicia una tarea después de un período de tiempo específico (retraso) una vez registrada la tarea. El retraso se especifica en la propiedad [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) de la interfaz [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) para scripting).

> [!Note]  
> Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.

 

## <a name="registration-trigger-examples"></a>Ejemplos de desencadenadores de registro

En los siguientes ejemplos se inicia el Bloc de notas cuando se registra una tarea:

-   [Ejemplo de desencadenador de registro (scripting)](registration-trigger-example--scripting-.md)
-   [Ejemplo de desencadenador de registro (C++)](registration-trigger-example--c---.md)
-   [Ejemplo de desencadenador de registro (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




