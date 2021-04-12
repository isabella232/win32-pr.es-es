---
title: Interfaces QMGR
description: Use las siguientes interfaces de administrador de cola (QMGR) para descargar archivos y supervisar trabajos en la cola de descarga.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268317"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="6fdc6-103">Interfaces QMGR</span><span class="sxs-lookup"><span data-stu-id="6fdc6-103">QMGR Interfaces</span></span>

<span data-ttu-id="6fdc6-104">\[Las interfaces del administrador de colas (QMGR) están disponibles para su uso en los sistemas operativos especificados en la sección requisitos de un tema.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="6fdc6-105">Podrán modificarse o no estar disponibles en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6fdc6-106">En su lugar, use las [interfaces de bits](bits-interfaces.md).\]</span><span class="sxs-lookup"><span data-stu-id="6fdc6-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="6fdc6-107">Use las siguientes interfaces de administrador de cola (QMGR) para descargar archivos y supervisar trabajos en la cola de descarga.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="6fdc6-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="6fdc6-108">Interface</span></span>                                                                 | <span data-ttu-id="6fdc6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fdc6-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fdc6-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="6fdc6-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="6fdc6-111">Implemente para recibir una notificación cuando se produzcan eventos.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="6fdc6-112">**IBackgroundCopyGroup**</span><span class="sxs-lookup"><span data-stu-id="6fdc6-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="6fdc6-113">Use para administrar el grupo.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-113">Use to manage the group.</span></span> <span data-ttu-id="6fdc6-114">Por ejemplo, agregue un trabajo al grupo, establezca las propiedades del grupo e inicie y detenga el grupo en la cola de descarga.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="6fdc6-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="6fdc6-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="6fdc6-116">Use para agregar archivos al trabajo y recuperar el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="6fdc6-117">**IBackgroundCopyQMgr**</span><span class="sxs-lookup"><span data-stu-id="6fdc6-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="6fdc6-118">Use para crear un nuevo grupo, recuperar un grupo existente o enumerar todos los grupos de la cola.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="6fdc6-119">**IEnumBackgroundCopyGroups**</span><span class="sxs-lookup"><span data-stu-id="6fdc6-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="6fdc6-120">Use para recuperar una lista de grupos en la cola de descarga.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="6fdc6-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="6fdc6-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="6fdc6-122">Use para recuperar una lista de trabajos del grupo.</span><span class="sxs-lookup"><span data-stu-id="6fdc6-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





