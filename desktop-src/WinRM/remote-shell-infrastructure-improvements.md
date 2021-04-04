---
title: Mejoras en la infraestructura de shell remoto
description: Administración remota de Windows versión 2,0 (WinRM 2,0) ofrece muchas mejoras en la infraestructura de shell remoto.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/24/2020
ms.locfileid: "104077233"
---
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="814de-103">Mejoras en la infraestructura de shell remoto</span><span class="sxs-lookup"><span data-stu-id="814de-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="814de-104">Administración remota de Windows versión 2,0 (WinRM 2,0) ofrece muchas mejoras en la infraestructura de shell remoto.</span><span class="sxs-lookup"><span data-stu-id="814de-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="814de-105">En los temas siguientes se describen estas mejoras en detalle:</span><span class="sxs-lookup"><span data-stu-id="814de-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="814de-106">Compatibilidad con múltiples saltos</span><span class="sxs-lookup"><span data-stu-id="814de-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="814de-107">Administración de cuotas para shells remotos</span><span class="sxs-lookup"><span data-stu-id="814de-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="814de-108">Una de las mejoras de la infraestructura de shell remoto de WinRM es la adición de un administrador de Shell más robusto que mantiene la información de Shell específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="814de-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="814de-109">Los usuarios de WinRM pueden crear shells en equipos remotos para ejecutar comandos o scripts.</span><span class="sxs-lookup"><span data-stu-id="814de-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="814de-110">Además, los usuarios pueden crear varios shells en un equipo.</span><span class="sxs-lookup"><span data-stu-id="814de-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="814de-111">Los usuarios y los administradores necesitan la capacidad de administrar shells.</span><span class="sxs-lookup"><span data-stu-id="814de-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="814de-112">Los usuarios pueden enumerar, obtener y eliminar los shells que han creado.</span><span class="sxs-lookup"><span data-stu-id="814de-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="814de-113">Los administradores pueden enumerar todos los shells activos y recuperar detalles sobre shells específicos en un host local o remoto.</span><span class="sxs-lookup"><span data-stu-id="814de-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="814de-114">Los administradores también pueden eliminar cualquier Shell activo en un host local o remoto.</span><span class="sxs-lookup"><span data-stu-id="814de-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="814de-115">Cuando un usuario o administrador enumera los shells activos, el servicio WinRM puede devolver la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="814de-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="814de-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span><span class="sxs-lookup"><span data-stu-id="814de-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="814de-117">Especifica el identificador único del shell.</span><span class="sxs-lookup"><span data-stu-id="814de-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variables de entorno</span><span class="sxs-lookup"><span data-stu-id="814de-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="814de-119">Especifica las variables de entorno establecidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="814de-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="814de-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="814de-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="814de-121">Especifica el directorio de inicio del shell.</span><span class="sxs-lookup"><span data-stu-id="814de-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span><span class="sxs-lookup"><span data-stu-id="814de-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="814de-123">Especifica el URI de recurso para la operación de Shell.</span><span class="sxs-lookup"><span data-stu-id="814de-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="814de-124">El URI de recurso se puede usar para recuperar la configuración del complemento que es específica de la instancia del shell.</span><span class="sxs-lookup"><span data-stu-id="814de-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="814de-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="814de-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="814de-126">Especifica la duración máxima, en milisegundos, que el shell permanecerá abierto sin ninguna solicitud.</span><span class="sxs-lookup"><span data-stu-id="814de-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="814de-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span><span class="sxs-lookup"><span data-stu-id="814de-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="814de-128">Especifica los flujos de entrada para el shell.</span><span class="sxs-lookup"><span data-stu-id="814de-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span><span class="sxs-lookup"><span data-stu-id="814de-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="814de-130">Especifica los flujos de salida para el shell.</span><span class="sxs-lookup"><span data-stu-id="814de-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Hora de creación del shell</span><span class="sxs-lookup"><span data-stu-id="814de-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="814de-132">Especifica la marca de tiempo de creación del shell.</span><span class="sxs-lookup"><span data-stu-id="814de-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>Tiempodeinactividad</span><span class="sxs-lookup"><span data-stu-id="814de-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="814de-134">Especifica la duración, en milisegundos, que el Shell ha estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="814de-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="814de-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>Deberían</span><span class="sxs-lookup"><span data-stu-id="814de-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="814de-136">Especifica el ID. de usuario.</span><span class="sxs-lookup"><span data-stu-id="814de-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="814de-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nombre de host o dirección IP</span><span class="sxs-lookup"><span data-stu-id="814de-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="814de-138">Especifica el nombre de host o la dirección IP del equipo que creó el shell.</span><span class="sxs-lookup"><span data-stu-id="814de-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Uso de memoria de Shell</span><span class="sxs-lookup"><span data-stu-id="814de-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="814de-140">Especifica la cantidad de memoria usada por el shell.</span><span class="sxs-lookup"><span data-stu-id="814de-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="814de-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Número de procesos</span><span class="sxs-lookup"><span data-stu-id="814de-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="814de-142">Especifica el número de procesos creados por el shell.</span><span class="sxs-lookup"><span data-stu-id="814de-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="814de-143">Enumerar un shell en un host local</span><span class="sxs-lookup"><span data-stu-id="814de-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="814de-144">El siguiente comando muestra cómo usar la utilidad WinRM para enumerar los shells en un cliente WinRM: **WinRM Enumerate Shell**.</span><span class="sxs-lookup"><span data-stu-id="814de-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="814de-145">En el ejemplo de texto siguiente se muestra el resultado de la enumeración de Shell:</span><span class="sxs-lookup"><span data-stu-id="814de-145">The following text-based example displays the output for shell enumeration:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

<span data-ttu-id="814de-146">Para obtener más información, vea la ayuda en pantalla que se proporciona mediante la ejecución del siguiente comando: **WinRM Enumerate-?**.</span><span class="sxs-lookup"><span data-stu-id="814de-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="814de-147">Recuperación de información sobre un shell específico</span><span class="sxs-lookup"><span data-stu-id="814de-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="814de-148">Un administrador o un usuario también puede usar el identificador ShellId para recuperar información sobre el shell.</span><span class="sxs-lookup"><span data-stu-id="814de-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="814de-149">El siguiente comando muestra cómo usar la utilidad WinRM para obtener información sobre un shell específico: **WinRM Get Shell. ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span><span class="sxs-lookup"><span data-stu-id="814de-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="814de-150">En el ejemplo de texto siguiente se muestra el resultado de la información de Shell:</span><span class="sxs-lookup"><span data-stu-id="814de-150">The following text-based example displays the output for shell information:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

<span data-ttu-id="814de-151">Para obtener más información, vea la ayuda en pantalla proporcionada por el siguiente comando: **WinRM Get-?**.</span><span class="sxs-lookup"><span data-stu-id="814de-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="814de-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="814de-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="814de-153">Compatibilidad con múltiples saltos</span><span class="sxs-lookup"><span data-stu-id="814de-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="814de-154">Administración de cuotas para shells remotos</span><span class="sxs-lookup"><span data-stu-id="814de-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="814de-155">Referencia administrada para comandos de PowerShell de WS-Management</span><span class="sxs-lookup"><span data-stu-id="814de-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




