---
title: Funciones del administrador de reinicio
description: La API del administrador de reinicio usa las funciones que se identifican en la tabla siguiente.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Admin. de reinicio del administrador, referencia, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903385"
---
# <a name="restart-manager-functions"></a><span data-ttu-id="8864a-104">Funciones del administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="8864a-104">Restart Manager Functions</span></span>

<span data-ttu-id="8864a-105">La API del administrador de reinicio usa las funciones que se identifican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8864a-105">The Restart Manager API uses the functions identified in the following table.</span></span>



| <span data-ttu-id="8864a-106">Función</span><span class="sxs-lookup"><span data-stu-id="8864a-106">Function</span></span>                                           | <span data-ttu-id="8864a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8864a-107">Description</span></span>                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8864a-108">**RmAddFilter**</span><span class="sxs-lookup"><span data-stu-id="8864a-108">**RmAddFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | <span data-ttu-id="8864a-109">Modifica las acciones de cierre o reinicio.</span><span class="sxs-lookup"><span data-stu-id="8864a-109">Modifies shutdown or restart actions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="8864a-110">**RmStartSession**</span><span class="sxs-lookup"><span data-stu-id="8864a-110">**RmStartSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | <span data-ttu-id="8864a-111">Inicia una nueva sesión del administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="8864a-111">Starts a new Restart Manager session.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="8864a-112">**RmJoinSession**</span><span class="sxs-lookup"><span data-stu-id="8864a-112">**RmJoinSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | <span data-ttu-id="8864a-113">Une el proceso de una aplicación a una sesión del administrador de reinicio existente.</span><span class="sxs-lookup"><span data-stu-id="8864a-113">Joins the process of an application to an existing Restart Manager session.</span></span>                                                                                                                  |
| [<span data-ttu-id="8864a-114">**RmEndSession**</span><span class="sxs-lookup"><span data-stu-id="8864a-114">**RmEndSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | <span data-ttu-id="8864a-115">Finaliza la sesión del administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="8864a-115">Ends the Restart Manager session.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="8864a-116">**RmRegisterResources**</span><span class="sxs-lookup"><span data-stu-id="8864a-116">**RmRegisterResources**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | <span data-ttu-id="8864a-117">Registra los recursos, como nombres de archivo, nombres cortos de servicio o estructuras de [**\_ \_ proceso único de RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , en una sesión del administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="8864a-117">Registers resources, such as filenames, service short names, or [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structures, to a Restart Manager session.</span></span>                                   |
| [<span data-ttu-id="8864a-118">**RmGetList**</span><span class="sxs-lookup"><span data-stu-id="8864a-118">**RmGetList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | <span data-ttu-id="8864a-119">Lo usan los instaladores para obtener una lista de todas las aplicaciones afectadas por los recursos registrados y su estado actual.</span><span class="sxs-lookup"><span data-stu-id="8864a-119">Used by installers to get a list of all applications affected by registered resources and their current status.</span></span>                                                                              |
| [<span data-ttu-id="8864a-120">**RmGetFilterList**</span><span class="sxs-lookup"><span data-stu-id="8864a-120">**RmGetFilterList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | <span data-ttu-id="8864a-121">Consulta el estado de cierre y reinicio de las modificaciones que ya se han aplicado.</span><span class="sxs-lookup"><span data-stu-id="8864a-121">Queries the status of shutdown and restart modifications that have already been applied.</span></span>                                                                                                     |
| [<span data-ttu-id="8864a-122">**RmShutdown**</span><span class="sxs-lookup"><span data-stu-id="8864a-122">**RmShutdown**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | <span data-ttu-id="8864a-123">Inicia el cierre de aplicaciones y servicios.</span><span class="sxs-lookup"><span data-stu-id="8864a-123">Initiates the shut down of applications and services.</span></span>                                                                                                                                        |
| [<span data-ttu-id="8864a-124">**RmRemoveFilter**</span><span class="sxs-lookup"><span data-stu-id="8864a-124">**RmRemoveFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | <span data-ttu-id="8864a-125">Quita las modificaciones de apagado y reinicio que ya se han aplicado.</span><span class="sxs-lookup"><span data-stu-id="8864a-125">Removes shutdown and restart modifications that have already been applied.</span></span>                                                                                                                   |
| [<span data-ttu-id="8864a-126">**RmRestart**</span><span class="sxs-lookup"><span data-stu-id="8864a-126">**RmRestart**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | <span data-ttu-id="8864a-127">Reinicia las aplicaciones y los servicios que se han cerrado con la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) y que se han registrado para reiniciarse con **RegisterApplicationRestart**.</span><span class="sxs-lookup"><span data-stu-id="8864a-127">Restarts applications and services that have been shut down by the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function and that have been registered for restart using **RegisterApplicationRestart**.</span></span> |
| [<span data-ttu-id="8864a-128">**RmCancelCurrentTask**</span><span class="sxs-lookup"><span data-stu-id="8864a-128">**RmCancelCurrentTask**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | <span data-ttu-id="8864a-129">Cancela la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)o [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) actual.</span><span class="sxs-lookup"><span data-stu-id="8864a-129">Cancels the current [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown), or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>                                                            |



 

 

 




