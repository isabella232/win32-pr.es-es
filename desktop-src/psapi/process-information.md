---
title: Información del proceso
description: El sistema mantiene una lista de procesos en ejecución. Puede recuperar los identificadores para estos procesos mediante una llamada a la función EnumProcesses. Esta función rellena una matriz de valores DWORD con los identificadores de todos los procesos del sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359113"
---
# <a name="process-information"></a><span data-ttu-id="9d88a-105">Información del proceso</span><span class="sxs-lookup"><span data-stu-id="9d88a-105">Process Information</span></span>

<span data-ttu-id="9d88a-106">El sistema mantiene una lista de procesos en ejecución.</span><span class="sxs-lookup"><span data-stu-id="9d88a-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="9d88a-107">Puede recuperar los identificadores para estos procesos mediante una llamada a la función [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="9d88a-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="9d88a-108">Esta función rellena una matriz de valores **DWORD** con los identificadores de todos los procesos del sistema.</span><span class="sxs-lookup"><span data-stu-id="9d88a-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="9d88a-109">Muchas funciones de PSAPI requieren un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="9d88a-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="9d88a-110">Para obtener un identificador de proceso para un proceso en ejecución, pase su identificador de proceso (Obtenido de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) a la función [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) .</span><span class="sxs-lookup"><span data-stu-id="9d88a-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="9d88a-111">Recuerde llamar a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) cuando termine con el identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="9d88a-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 