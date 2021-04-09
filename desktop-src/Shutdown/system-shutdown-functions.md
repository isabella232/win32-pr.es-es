---
description: Las siguientes funciones se usan con el cierre del sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funciones de cierre del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002070"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="8983b-103">Funciones de cierre del sistema</span><span class="sxs-lookup"><span data-stu-id="8983b-103">System Shutdown Functions</span></span>

<span data-ttu-id="8983b-104">Las siguientes funciones se usan con el cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="8983b-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="8983b-105">Función</span><span class="sxs-lookup"><span data-stu-id="8983b-105">Function</span></span>                                                         | <span data-ttu-id="8983b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8983b-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8983b-107">**AbortSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="8983b-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="8983b-108">Detiene el cierre del sistema que se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="8983b-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="8983b-109">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="8983b-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="8983b-110">Cierra la sesión del usuario interactivo.</span><span class="sxs-lookup"><span data-stu-id="8983b-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="8983b-111">**ExitWindowsEx**</span><span class="sxs-lookup"><span data-stu-id="8983b-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="8983b-112">Cierra la sesión del usuario interactivo, apaga el sistema o apaga y reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="8983b-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="8983b-113">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="8983b-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="8983b-114">Inicia el apagado y el reinicio del equipo especificado y reinicia las aplicaciones que se han registrado para reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="8983b-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="8983b-115">**InitiateSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="8983b-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="8983b-116">Inicia el cierre y el reinicio opcional del equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="8983b-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="8983b-117">**InitiateSystemShutdownEx**</span><span class="sxs-lookup"><span data-stu-id="8983b-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="8983b-118">Inicia el cierre y el reinicio opcional del equipo especificado y, opcionalmente, registra el motivo del cierre.</span><span class="sxs-lookup"><span data-stu-id="8983b-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="8983b-119">**LockWorkStation**</span><span class="sxs-lookup"><span data-stu-id="8983b-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="8983b-120">Bloquea la pantalla de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="8983b-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="8983b-121">**ShutdownBlockReasonCreate**</span><span class="sxs-lookup"><span data-stu-id="8983b-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="8983b-122">Indica que no se puede apagar el sistema y establece una cadena de motivo que se mostrará al usuario si se inicia el cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="8983b-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="8983b-123">**ShutdownBlockReasonDestroy**</span><span class="sxs-lookup"><span data-stu-id="8983b-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="8983b-124">Indica que el sistema se puede apagar y libera la cadena de motivo.</span><span class="sxs-lookup"><span data-stu-id="8983b-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="8983b-125">**ShutdownBlockReasonQuery**</span><span class="sxs-lookup"><span data-stu-id="8983b-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="8983b-126">Recupera la cadena de motivo establecida por la función [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="8983b-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 



