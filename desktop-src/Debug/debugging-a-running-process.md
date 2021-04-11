---
description: Para depurar un proceso que ya se está ejecutando, el depurador debe usar DebugActiveProcess con el identificador de proceso. Para recuperar una lista de identificadores de proceso, utilice la función EnumProcesses o Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Depurar un proceso en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152741"
---
# <a name="debugging-a-running-process"></a><span data-ttu-id="16082-104">Depurar un proceso en ejecución</span><span class="sxs-lookup"><span data-stu-id="16082-104">Debugging a Running Process</span></span>

<span data-ttu-id="16082-105">Para depurar un proceso que ya se está ejecutando, el depurador debe usar [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) con el identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="16082-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="16082-106">Para recuperar una lista de identificadores de proceso, utilice la función [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) o [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="16082-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="16082-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) asocia el depurador al proceso activo.</span><span class="sxs-lookup"><span data-stu-id="16082-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="16082-108">En este caso, solo se puede depurar el proceso activo. sus procesos secundarios no pueden.</span><span class="sxs-lookup"><span data-stu-id="16082-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="16082-109">El depurador debe tener el acceso adecuado al proceso de ejecución para utilizar **DebugActiveProcess**.</span><span class="sxs-lookup"><span data-stu-id="16082-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="16082-110">Para obtener más información sobre los derechos de acceso, consulte [Access Control](../secauthz/access-control.md).</span><span class="sxs-lookup"><span data-stu-id="16082-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="16082-111">Una vez que el depurador se ha creado o adjuntado al proceso que intenta depurar, el sistema notifica al depurador todos los eventos de depuración que se producen en el proceso y, si se especifica, en los procesos secundarios.</span><span class="sxs-lookup"><span data-stu-id="16082-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="16082-112">Para obtener más información sobre la depuración de eventos, vea [depuración de eventos](debugging-events.md).</span><span class="sxs-lookup"><span data-stu-id="16082-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="16082-113">Para desasociar del proceso que se está depurando, el depurador debe utilizar la función [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .</span><span class="sxs-lookup"><span data-stu-id="16082-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
