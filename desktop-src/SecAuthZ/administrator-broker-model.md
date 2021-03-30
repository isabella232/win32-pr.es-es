---
description: La aplicación se divide en dos programas. Uno de los programas se ejecuta como un usuario estándar y el otro con privilegios de administrador.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modelo de agente de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910617"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="f83dc-104">Modelo de agente de administrador</span><span class="sxs-lookup"><span data-stu-id="f83dc-104">Administrator Broker Model</span></span>

<span data-ttu-id="f83dc-105">En el modelo de agente de administrador, la aplicación se divide en dos programas.</span><span class="sxs-lookup"><span data-stu-id="f83dc-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="f83dc-106">Uno de los programas se ejecuta como un usuario estándar y el otro con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="f83dc-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="f83dc-107">Con un manifiesto de aplicación, marque el programa de usuario estándar con un **requestedExecutionLevel** de **asInvoker** y marque el programa administrativo con un **requestedExecutionLevel** de **requireAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="f83dc-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="f83dc-108">Un usuario inicia el programa de usuario estándar en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="f83dc-108">A user launches the standard user program first.</span></span> <span data-ttu-id="f83dc-109">Cuando el usuario intenta realizar una operación que requiere un token de acceso de administrador completo, el programa de usuario estándar llama a la función [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) para iniciar el programa administrativo.</span><span class="sxs-lookup"><span data-stu-id="f83dc-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="f83dc-110">La función **ShellExecute** solicita al usuario la aprobación antes de ejecutar la aplicación con el token de acceso de administrador completo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f83dc-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="f83dc-111">El programa administrativo puede realizar tareas que requieren privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="f83dc-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="f83dc-112">El programa administrativo no está completamente aislado del programa de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="f83dc-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="f83dc-113">El programa administrativo puede habilitar la comunicación entre procesos con el programa de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="f83dc-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="f83dc-114">Sin embargo, esta comunicación está limitada por la Directiva de integridad obligatoria predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f83dc-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="f83dc-115">Para obtener información sobre las consideraciones de integridad obligatorias, consulte [diseño de aplicaciones para que se ejecuten en un nivel de integridad bajo](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="f83dc-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="f83dc-116">A continuación se muestran los posibles usos del modelo de agente de administrador:</span><span class="sxs-lookup"><span data-stu-id="f83dc-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="f83dc-117">Desarrollo de asistentes.</span><span class="sxs-lookup"><span data-stu-id="f83dc-117">Developing wizards.</span></span> <span data-ttu-id="f83dc-118">Cuando un asistente de hardware determina que un controlador requerido no está instalado en el equipo o que se encuentra en la ubicación aprobada de la empresa, llama a una aplicación con privilegios elevados con la capacidad de trasladar un controlador al almacén del equipo.</span><span class="sxs-lookup"><span data-stu-id="f83dc-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="f83dc-119">Autorun.exe llamar a Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="f83dc-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="f83dc-120">Cuando un usuario ejecuta software desde un CD, Autorun.exe, que se ejecuta como un usuario estándar, inicia Setup.exe, que se ejecuta como administrador, para instalar el software en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f83dc-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="f83dc-121">A continuación se indican los inconvenientes del uso del modelo de agente de administrador:</span><span class="sxs-lookup"><span data-stu-id="f83dc-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="f83dc-122">Las transiciones de la aplicación a la aplicación pueden resultar confusas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f83dc-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="f83dc-123">Puede ser difícil informar al usuario de por qué aparece una nueva aplicación en el monitor.</span><span class="sxs-lookup"><span data-stu-id="f83dc-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="f83dc-124">Puede ser difícil pasar información de estado entre las dos aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f83dc-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="f83dc-125">Por ejemplo, no usaría este modelo para pasar información de estado entre un panel de control de usuario estándar (CPL) y su homólogo de administrador, simplemente para permitir que el mismo CPL tenga funcionalidad de usuario administrativo y estándar.</span><span class="sxs-lookup"><span data-stu-id="f83dc-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="f83dc-126">El CPL de usuario estándar tendría que almacenar su estado en algún lugar.</span><span class="sxs-lookup"><span data-stu-id="f83dc-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="f83dc-127">Puede haber una gran cantidad de código replicado al dividir la funcionalidad entre dos programas.</span><span class="sxs-lookup"><span data-stu-id="f83dc-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f83dc-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f83dc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f83dc-129">Desarrollo de aplicaciones que requieren privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="f83dc-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="f83dc-130">Modelo de objetos COM de administrador</span><span class="sxs-lookup"><span data-stu-id="f83dc-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="f83dc-131">Modelo de servicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f83dc-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="f83dc-132">Modelo de tareas elevado</span><span class="sxs-lookup"><span data-stu-id="f83dc-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
