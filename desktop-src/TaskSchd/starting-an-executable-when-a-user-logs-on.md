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
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="aede7-104">Iniciar un archivo ejecutable cuando un usuario inicia sesión</span><span class="sxs-lookup"><span data-stu-id="aede7-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="aede7-105">La escritura de una tarea que inicia un ejecutable cuando un usuario inicia sesión se realiza mediante la definición de un desencadenador Logon y una acción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="aede7-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="aede7-106">Desencadenador Logon</span><span class="sxs-lookup"><span data-stu-id="aede7-106">Logon Trigger</span></span>

<span data-ttu-id="aede7-107">Los desencadenadores de inicio de sesión se activan por su límite de inicio, pero no inician el ejecutable hasta que un usuario especificado inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="aede7-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="aede7-108">Puede especificar el desencadenador Logon para que se inicie cuando un determinado usuario inicie sesión especificando el usuario en la propiedad [**userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) de la interfaz [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**LogonTrigger**](logontrigger.md) para scripting).</span><span class="sxs-lookup"><span data-stu-id="aede7-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="aede7-109">Ejemplos de LogonTrigger</span><span class="sxs-lookup"><span data-stu-id="aede7-109">LogonTrigger Examples</span></span>

<span data-ttu-id="aede7-110">En los siguientes ejemplos se inicia el Bloc de notas después de que un usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="aede7-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="aede7-111">Ejemplo de desencadenador Logon (scripting)</span><span class="sxs-lookup"><span data-stu-id="aede7-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="aede7-112">Ejemplo de desencadenador Logon (C++)</span><span class="sxs-lookup"><span data-stu-id="aede7-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="aede7-113">Ejemplo de desencadenador Logon (XML)</span><span class="sxs-lookup"><span data-stu-id="aede7-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="aede7-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aede7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aede7-115">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="aede7-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




