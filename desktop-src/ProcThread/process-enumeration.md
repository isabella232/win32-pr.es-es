---
description: Todos los usuarios tienen acceso de lectura a la lista de procesos del sistema y hay una serie de funciones diferentes que enumeran los procesos activos. La función que se debe usar dependerá de factores como la compatibilidad con la plataforma deseada.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Enumeración de procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677841"
---
# <a name="process-enumeration"></a><span data-ttu-id="23349-104">Enumeración de procesos</span><span class="sxs-lookup"><span data-stu-id="23349-104">Process Enumeration</span></span>

<span data-ttu-id="23349-105">Todos los usuarios tienen acceso de lectura a la lista de procesos del sistema y hay una serie de funciones diferentes que enumeran los procesos activos.</span><span class="sxs-lookup"><span data-stu-id="23349-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="23349-106">La función que se debe usar dependerá de factores como la compatibilidad con la plataforma deseada.</span><span class="sxs-lookup"><span data-stu-id="23349-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="23349-107">Las siguientes funciones se usan para enumerar los procesos.</span><span class="sxs-lookup"><span data-stu-id="23349-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="23349-108">Función</span><span class="sxs-lookup"><span data-stu-id="23349-108">Function</span></span>                                                    | <span data-ttu-id="23349-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="23349-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="23349-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="23349-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="23349-111">Recupera el identificador de proceso de cada objeto de proceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="23349-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="23349-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="23349-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="23349-113">Recupera información sobre el primer proceso encontrado en una instantánea del sistema.</span><span class="sxs-lookup"><span data-stu-id="23349-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="23349-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="23349-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="23349-115">Recupera información sobre el siguiente proceso registrado en una instantánea del sistema.</span><span class="sxs-lookup"><span data-stu-id="23349-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="23349-116">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="23349-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="23349-117">Recupera información sobre los procesos activos en el servidor de Terminal Server especificado.</span><span class="sxs-lookup"><span data-stu-id="23349-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="23349-118">Las funciones TOOLHELP y [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumeran todos los procesos.</span><span class="sxs-lookup"><span data-stu-id="23349-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="23349-119">Para enumerar los procesos que se están ejecutando en una cuenta de usuario específica, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) y filtre por el SID de usuario.</span><span class="sxs-lookup"><span data-stu-id="23349-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="23349-120">Puede filtrar por el ID. de sesión para ocultar los procesos que se ejecutan en otras sesiones de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="23349-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="23349-121">También puede filtrar los procesos por cuenta de usuario, independientemente de la función de enumeración, mediante una llamada a [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)y [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con **TokenUser**.</span><span class="sxs-lookup"><span data-stu-id="23349-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="23349-122">Sin embargo, no puede abrir un proceso que esté protegido por un descriptor de seguridad a menos que se le haya concedido acceso.</span><span class="sxs-lookup"><span data-stu-id="23349-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
