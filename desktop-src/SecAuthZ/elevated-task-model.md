---
description: Una aplicación que se ejecuta como usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modelo de tareas elevado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361385"
---
# <a name="elevated-task-model"></a><span data-ttu-id="34d63-103">Modelo de tareas elevado</span><span class="sxs-lookup"><span data-stu-id="34d63-103">Elevated Task Model</span></span>

<span data-ttu-id="34d63-104">En el modelo de tareas elevado, una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador iniciando una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="34d63-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="34d63-105">**Windows Server 2003 y Windows XP:** No se admite el modelo de tareas elevado.</span><span class="sxs-lookup"><span data-stu-id="34d63-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="34d63-106">Las tareas no consumen tantos recursos del sistema como servicios y las tareas se cierran automáticamente cuando finalizan.</span><span class="sxs-lookup"><span data-stu-id="34d63-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="34d63-107">Considere la posibilidad de usar este modelo en lugar del [modelo de servicio del sistema operativo](operating-system-service-model.md) , a menos que sea necesaria la compatibilidad con versiones anteriores de los sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="34d63-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="34d63-108">Para utilizar una tarea para realizar operaciones con privilegios en una aplicación de usuario estándar, deben cumplirse las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="34d63-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="34d63-109">La tarea debe estar establecida en ejecutar como **sistema**.</span><span class="sxs-lookup"><span data-stu-id="34d63-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="34d63-110">El [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) asociado a la tarea debe configurarse para permitir que los usuarios estándar inicien la tarea.</span><span class="sxs-lookup"><span data-stu-id="34d63-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="34d63-111">El servicio Programador de tareas debe estar en ejecución.</span><span class="sxs-lookup"><span data-stu-id="34d63-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="34d63-112">Para obtener información sobre cómo crear e iniciar tareas, vea [programador de tareas](/windows/desktop/TaskSchd/task-scheduler-start-page).</span><span class="sxs-lookup"><span data-stu-id="34d63-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34d63-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34d63-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34d63-114">Desarrollo de aplicaciones que requieren privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="34d63-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="34d63-115">Modelo de agente de administrador</span><span class="sxs-lookup"><span data-stu-id="34d63-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="34d63-116">Modelo de objetos COM de administrador</span><span class="sxs-lookup"><span data-stu-id="34d63-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="34d63-117">Modelo de servicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="34d63-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
