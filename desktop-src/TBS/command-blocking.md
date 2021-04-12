---
title: Bloqueo de comandos
description: Para conservar la integridad de las operaciones, el software de la plataforma no puede ejecutar determinados comandos de TPM.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "104420496"
---
# <a name="command-blocking"></a><span data-ttu-id="5c7b0-103">Bloqueo de comandos</span><span class="sxs-lookup"><span data-stu-id="5c7b0-103">Command Blocking</span></span>

<span data-ttu-id="5c7b0-104">Para conservar la integridad de las operaciones, el software de la plataforma no puede ejecutar determinados comandos de TPM.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="5c7b0-105">Por ejemplo, algunos comandos solo se ejecutan mediante software del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="5c7b0-106">Cuando el TBS bloquea un comando, se devuelve un error según corresponda.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="5c7b0-107">De forma predeterminada, TBS bloquea los comandos que podrían afectar a la privacidad, la seguridad y la estabilidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="5c7b0-108">TBS también presupone que otras partes de la pila de software pueden restringir el acceso a determinados comandos a las entidades autorizadas.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="5c7b0-109">En el caso de los comandos de la versión 1,2 de TPM, hay tres listas de comandos bloqueados: una lista controlada por la Directiva de grupo, una lista controlada por administradores locales y una lista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="5c7b0-110">Un comando de TPM se bloquea si está en cualquiera de las listas.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="5c7b0-111">Sin embargo, hay marcas de directiva de grupo que permiten a TBS omitir la lista local y la lista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="5c7b0-112">Las marcas de directiva de grupo se pueden editar directamente o se puede obtener acceso a ellas mediante el Editor de objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="5c7b0-113">La lista de comandos bloqueados localmente no se conserva después de una actualización al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="5c7b0-114">Se conservan los comandos bloqueados en la lista de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="5c7b0-115">En el caso de los comandos de la versión 2,0 de TPM, se invierte la lógica para el bloqueo; usa una lista de comandos permitidos.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="5c7b0-116">Esta lógica bloqueará automáticamente los comandos que no se conocían cuando la lista se realizó por primera vez.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="5c7b0-117">Cuando se agregan comandos a la especificación de TPM después de que se haya enviado una versión de Windows, estos nuevos comandos se bloquean automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="5c7b0-118">Solo una actualización del registro agregará estos nuevos comandos a la lista de comandos permitidos.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="5c7b0-119">A partir de Windows 10 1809 (Windows Server 2019), los comandos de TPM 2,0 permitidos ya no se pueden manipular a través de la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="5c7b0-120">Para estas versiones de Windows 10, los comandos de TPM 2,0 permitidos se han corregido en el controlador de TPM.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="5c7b0-121">Los comandos de TPM 1,2 se pueden bloquear y desbloquear a través de los cambios del registro.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="5c7b0-122">Acceso directo al registro</span><span class="sxs-lookup"><span data-stu-id="5c7b0-122">Direct Registry Access</span></span>

<span data-ttu-id="5c7b0-123">Las marcas de directiva de grupo se encuentran en la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="5c7b0-124">Para determinar qué listas deben usarse para bloquear comandos de TPM, hay dos valores **DWORD** que se usan como marcas booleanas:</span><span class="sxs-lookup"><span data-stu-id="5c7b0-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="5c7b0-125">"IgnoreDefaultList"</span><span class="sxs-lookup"><span data-stu-id="5c7b0-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="5c7b0-126">Si se establece (el valor existe y es distinto de cero), TBS omite la lista de comandos bloqueados predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="5c7b0-127">"IgnoreLocalList"</span><span class="sxs-lookup"><span data-stu-id="5c7b0-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="5c7b0-128">Si se establece (el valor existe y es distinto de cero), TBS omite la lista local de comandos bloqueados.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="5c7b0-129">Editor de objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="5c7b0-129">Group Policy Object Editor</span></span>

<span data-ttu-id="5c7b0-130">**Para tener acceso al editor de objetos de directiva de grupo**</span><span class="sxs-lookup"><span data-stu-id="5c7b0-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="5c7b0-131">Haga clic en **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-131">Click **Start**.</span></span>
2.  <span data-ttu-id="5c7b0-132">Haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-132">Click **Run**.</span></span>
3.  <span data-ttu-id="5c7b0-133">En el cuadro **Abrir** , escriba **gpedit.msc**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="5c7b0-134">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-134">Click **OK**.</span></span> <span data-ttu-id="5c7b0-135">Se abre el editor de objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="5c7b0-136">Expanda **configuración del equipo**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="5c7b0-137">Expanda **plantillas administrativas**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="5c7b0-138">Expanda **sistema**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-138">Expand **System**.</span></span>
7.  <span data-ttu-id="5c7b0-139">Expanda **módulo de plataforma segura Services**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="5c7b0-140">Las listas de comandos de TPM 1.2 bloqueados específicos se pueden editar directamente en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="5c7b0-141">Lista de directivas de Grupo:</span><span class="sxs-lookup"><span data-stu-id="5c7b0-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="5c7b0-142">Lista local:</span><span class="sxs-lookup"><span data-stu-id="5c7b0-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="5c7b0-143">Lista predeterminada:</span><span class="sxs-lookup"><span data-stu-id="5c7b0-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="5c7b0-144">En cada una de estas claves del registro hay una lista de valores de registro de \_ tipo REG SZ.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="5c7b0-145">Cada valor representa un comando de TPM bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="5c7b0-146">Cada clave del registro tiene un campo "nombre del valor" y un campo "datos del valor".</span><span class="sxs-lookup"><span data-stu-id="5c7b0-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="5c7b0-147">Ambos campos ("nombre del valor" y "datos del valor"), deben coincidir exactamente con el valor decimal del ordinal del comando TPM que se va a bloquear.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="5c7b0-148">La lista de comandos de TPM 2,0 específicos permitidos se puede editar directamente en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="5c7b0-149">En la clave del registro hay una lista de valores de registro de \_ tipo REG DWORD.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="5c7b0-150">Cada valor representa un comando de TPM 2,0 permitido.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="5c7b0-151">Cada valor del registro tiene un **nombre** y un campo de **valor** .</span><span class="sxs-lookup"><span data-stu-id="5c7b0-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="5c7b0-152">El **nombre** coincide con el ordinal del comando TPM 2,0 hexadecimal que se debe permitir.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="5c7b0-153">El **valor** tiene un valor de 1 si se permite el comando.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="5c7b0-154">Si el ordinal de un comando no está presente o tiene un valor de 0, se bloqueará el comando.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="5c7b0-155">Lista predeterminada:</span><span class="sxs-lookup"><span data-stu-id="5c7b0-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="5c7b0-156">En Windows 8, Windows Server 2012 y versiones posteriores, las claves del registro **BlockedCommands** y **AllowedW8Commands** determinan respectivamente los comandos de TPM bloqueados o permitidos para las cuentas de administrador.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="5c7b0-157">Las cuentas de usuario tienen una lista de comandos de TPM bloqueados o permitidos en las claves del registro **BlockedUserCommands** y **AllowedW8UserCommands** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="5c7b0-158">En Windows 10, versión 1607, se han incorporado nuevas claves del registro para las aplicaciones AppContainer: **BlockedAppContainerCommands** y **AllowedW8AppContainerCommands**.</span><span class="sxs-lookup"><span data-stu-id="5c7b0-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




