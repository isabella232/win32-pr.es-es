---
title: Iniciar un ejecutable cuando un usuario inicia sesión
description: Escribir una tarea que inicia un ejecutable cuando un usuario inicia sesión se realiza mediante la definición de un desencadenador de inicio de sesión y una acción ejecutable.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Programador de tareas ejemplos de Programador de tareas , desencadenador de inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170657"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Iniciar un ejecutable cuando un usuario inicia sesión

Escribir una tarea que inicia un ejecutable cuando un usuario inicia sesión se realiza mediante la definición de un desencadenador de inicio de sesión y una acción ejecutable.

## <a name="logon-trigger"></a>Desencadenador de inicio de sesión

Los desencadenadores logon se activan por su límite de inicio, pero no inician el ejecutable hasta que un usuario especificado inicia sesión. Puede especificar el desencadenador de inicio de sesión para que se inicie cuando un determinado usuario inicie sesión especificando el usuario en la propiedad [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) de la interfaz [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) [**(LogonTrigger**](logontrigger.md) para scripting).

## <a name="logontrigger-examples"></a>Ejemplos de LogonTrigger

Los ejemplos siguientes comienzan Bloc de notas después de que un usuario inicie sesión.

-   [Ejemplo de desencadenador de inicio de sesión (scripting)](logon-trigger-example--scripting-.md)
-   [Ejemplo de desencadenador de inicio de sesión (C++)](logon-trigger-example--c---.md)
-   [Ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




