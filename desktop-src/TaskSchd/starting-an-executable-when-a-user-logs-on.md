---
title: Iniciar un archivo ejecutable cuando un usuario inicia sesión
description: La escritura de una tarea que inicia un ejecutable cuando un usuario inicia sesión se realiza mediante la definición de un desencadenador Logon y una acción ejecutable.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Programador de tareas examples Programador de tareas, Logon Trigger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418345"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Iniciar un archivo ejecutable cuando un usuario inicia sesión

La escritura de una tarea que inicia un ejecutable cuando un usuario inicia sesión se realiza mediante la definición de un desencadenador Logon y una acción ejecutable.

## <a name="logon-trigger"></a>Desencadenador Logon

Los desencadenadores de inicio de sesión se activan por su límite de inicio, pero no inician el ejecutable hasta que un usuario especificado inicia sesión. Puede especificar el desencadenador Logon para que se inicie cuando un determinado usuario inicie sesión especificando el usuario en la propiedad [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) de la interfaz [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) para scripting).

## <a name="logontrigger-examples"></a>Ejemplos de LogonTrigger

En los siguientes ejemplos se inicia el Bloc de notas después de que un usuario inicie sesión.

-   [Ejemplo de desencadenador Logon (scripting)](logon-trigger-example--scripting-.md)
-   [Ejemplo de desencadenador Logon (C++)](logon-trigger-example--c---.md)
-   [Ejemplo de desencadenador Logon (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




