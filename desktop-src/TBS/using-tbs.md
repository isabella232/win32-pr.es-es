---
title: Uso de TBS
description: Cada comando enviado a TBS está asociado a una entidad específica. Esto se logra mediante la creación de uno o más contextos para una entidad, que después se asocian a cada comando subsiguiente enviado por esa entidad.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- Servicios base de TPM TBS, ejemplos
- Servicios base de TPM TBS, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994277"
---
# <a name="using-tbs"></a><span data-ttu-id="781a0-106">Uso de TBS</span><span class="sxs-lookup"><span data-stu-id="781a0-106">Using TBS</span></span>

<span data-ttu-id="781a0-107">La característica servicios base de TPM se divide en cuatro áreas funcionales:</span><span class="sxs-lookup"><span data-stu-id="781a0-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="781a0-108">Virtualización de recursos</span><span class="sxs-lookup"><span data-stu-id="781a0-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="781a0-109">Programación de comandos</span><span class="sxs-lookup"><span data-stu-id="781a0-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="781a0-110">Administración de energía</span><span class="sxs-lookup"><span data-stu-id="781a0-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="781a0-111">Bloqueo de comandos</span><span class="sxs-lookup"><span data-stu-id="781a0-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="781a0-112">Para asegurarse de que las distintas entidades no puedan tener acceso a los recursos de los demás, cada comando enviado a TBS está asociado a una entidad específica.</span><span class="sxs-lookup"><span data-stu-id="781a0-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="781a0-113">Esto se logra mediante la creación de uno o más contextos para una entidad, que después se asocian a cada comando subsiguiente enviado por esa entidad.</span><span class="sxs-lookup"><span data-stu-id="781a0-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="781a0-114">Cada comando incluye un objeto de contexto, que permite a TBS ejecutar comandos de TPM en el contexto adecuado.</span><span class="sxs-lookup"><span data-stu-id="781a0-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="781a0-115">Todos los objetos creados por los comandos se vacían desde el TPM cuando se cierra el contexto.</span><span class="sxs-lookup"><span data-stu-id="781a0-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="781a0-116">Una entidad crea el contexto antes de obtener acceso por primera vez a TBS y mantiene el contexto hasta que finaliza la realización de los accesos a TBS.</span><span class="sxs-lookup"><span data-stu-id="781a0-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="781a0-117">Por ejemplo, en el caso de una TSS, la característica de servicios principales de TCG (TCS) de TSS crearía un contexto de TBS cuando se iniciaba y mantener ese contexto activo hasta que se cierre.</span><span class="sxs-lookup"><span data-stu-id="781a0-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="781a0-118">En el caso de Windows Server 2008 y Windows Vista, el TBS restringe el acceso a la API de TBS a las cuentas de administrador, NT AUTHORITY \\ LocalService y NT Authority \\ .</span><span class="sxs-lookup"><span data-stu-id="781a0-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="781a0-119">De forma predeterminada, estas cuentas son las únicas que se pueden conectar a TBS y crear contextos.</span><span class="sxs-lookup"><span data-stu-id="781a0-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="781a0-120">Las restricciones de acceso se pueden modificar mediante la creación de un **acceso** de clave del registro con **un nombre de** valor de registro de cadena (**reg \_ SZ**).</span><span class="sxs-lookup"><span data-stu-id="781a0-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="781a0-121">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="781a0-121">Data type</span></span>
</dt> <dd><span data-ttu-id="781a0-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="781a0-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="781a0-123">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="781a0-123">Example:</span></span>

<span data-ttu-id="781a0-124">**O:BAG: BAD: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**</span><span class="sxs-lookup"><span data-stu-id="781a0-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="781a0-125">De forma predeterminada, el número máximo de contextos admitidos por TBS es 25.</span><span class="sxs-lookup"><span data-stu-id="781a0-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="781a0-126">Este número puede modificarse mediante la creación o modificación de un valor del registro **DWORD** denominado **MaxContexts** en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**.</span><span class="sxs-lookup"><span data-stu-id="781a0-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="781a0-127">El uso del contexto de TBS en tiempo real se puede observar mediante la herramienta Monitor de rendimiento para realizar el seguimiento del número de contextos de TBS.</span><span class="sxs-lookup"><span data-stu-id="781a0-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="781a0-128">En Windows 8, Windows Server 2012 y versiones posteriores, el TBS permite el acceso a los usuarios estándar y a los administradores.</span><span class="sxs-lookup"><span data-stu-id="781a0-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="781a0-129">Las claves del registro **SecurityDescriptor** y **MaxContexts** se han quedado obsoletas.</span><span class="sxs-lookup"><span data-stu-id="781a0-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="781a0-130">En Windows 8, Windows Server 2012 y versiones posteriores, TBS restringe el acceso a determinados comandos mediante el bloqueo de comandos.</span><span class="sxs-lookup"><span data-stu-id="781a0-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="781a0-131">Para Windows 10, versión 1607, el TBS permite el acceso desde aplicaciones AppContainer.</span><span class="sxs-lookup"><span data-stu-id="781a0-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="781a0-132">Para cada versión de TPM, se han agregado las claves **BlockedAppContainerCommands** y **AllowedW8AppContainerCommands** con las listas coincidentes de comandos de TPM bloqueados y permitidos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="781a0-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="781a0-133">En Windows 10, versión 1803, ya no se admiten las claves del registro en **AllowedW8AppContainerCommands** .</span><span class="sxs-lookup"><span data-stu-id="781a0-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




