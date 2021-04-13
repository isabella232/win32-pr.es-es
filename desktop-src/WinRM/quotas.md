---
title: Administración de cuotas para shells remotos
description: La administración de cuotas permite a los usuarios administrar los recursos del sistema de forma más eficaz.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357543"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="720d9-103">Administración de cuotas para shells remotos</span><span class="sxs-lookup"><span data-stu-id="720d9-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="720d9-104">La administración de cuotas permite a los usuarios administrar los recursos del sistema de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="720d9-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="720d9-105">Administración remota de Windows (WinRM) ha agregado un conjunto específico de cuotas que proporcionan una mejor calidad de servicio, ayudan a evitar los problemas de denegación de servicio y asignan recursos del servidor a los usuarios simultáneos.</span><span class="sxs-lookup"><span data-stu-id="720d9-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="720d9-106">El conjunto de cuotas de WinRM se basa en la infraestructura de cuota que se implementa para el servicio Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="720d9-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="720d9-107">La implementación de cuotas ayudará a evitar la degradación del rendimiento y los problemas de denegación de servicio al hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="720d9-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="720d9-108">Limitar el número de shells y procesos de Shell que un usuario puede crear</span><span class="sxs-lookup"><span data-stu-id="720d9-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="720d9-109">Limitar el número máximo de usuarios simultáneos</span><span class="sxs-lookup"><span data-stu-id="720d9-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="720d9-110">Administrar la cantidad de memoria que se asigna a un shell</span><span class="sxs-lookup"><span data-stu-id="720d9-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="720d9-111">Establecer un tiempo de espera para los shells inactivos</span><span class="sxs-lookup"><span data-stu-id="720d9-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="720d9-112">Configuración de cuota</span><span class="sxs-lookup"><span data-stu-id="720d9-112">Quota Settings</span></span>

<span data-ttu-id="720d9-113">Las siguientes cuotas deben aplicarse para la administración remota de Shell.</span><span class="sxs-lookup"><span data-stu-id="720d9-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="720d9-114">Estas cuotas se pueden configurar a través de la utilidad WinRM o a través de la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="720d9-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="720d9-115">Los valores configurados por una directiva de grupo sustituyen a las cuotas establecidas por la utilidad WinRM.</span><span class="sxs-lookup"><span data-stu-id="720d9-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="720d9-116">Para obtener más información sobre la configuración de directivas de grupo para WinRM, consulte [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="720d9-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="720d9-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="720d9-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="720d9-118">Tiempo máximo en milisegundos antes de que se elimine un shell remoto inactivo.</span><span class="sxs-lookup"><span data-stu-id="720d9-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="720d9-119">El valor predeterminado es 180000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="720d9-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="720d9-120">El tiempo mínimo es de 1000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="720d9-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="720d9-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="720d9-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="720d9-122">Número máximo de procesos permitidos por Shell, incluidos los procesos secundarios del shell.</span><span class="sxs-lookup"><span data-stu-id="720d9-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="720d9-123">El valor predeterminado es 25.</span><span class="sxs-lookup"><span data-stu-id="720d9-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="720d9-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="720d9-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="720d9-125">Cantidad máxima de memoria asignada por Shell, incluidos los procesos secundarios del shell.</span><span class="sxs-lookup"><span data-stu-id="720d9-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="720d9-126">El valor predeterminado es 1024 MB.</span><span class="sxs-lookup"><span data-stu-id="720d9-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="720d9-127">No se admite el comportamiento si MaxMemoryPerShellMB está establecido en un valor que es menor que el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="720d9-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="720d9-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="720d9-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="720d9-129">Número máximo de shells por usuario.</span><span class="sxs-lookup"><span data-stu-id="720d9-129">The maximum number of shells per user.</span></span> <span data-ttu-id="720d9-130">El valor predeterminado es 30.</span><span class="sxs-lookup"><span data-stu-id="720d9-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="720d9-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="720d9-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="720d9-132">Número máximo de usuarios simultáneos que pueden abrir shells.</span><span class="sxs-lookup"><span data-stu-id="720d9-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="720d9-133">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="720d9-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="720d9-134">Cuotas desusadas</span><span class="sxs-lookup"><span data-stu-id="720d9-134">Deprecated Quotas</span></span>

<span data-ttu-id="720d9-135">WinRM 2,0 establece la cuota de MaxShellRunTime en solo lectura.</span><span class="sxs-lookup"><span data-stu-id="720d9-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="720d9-136">Cambiar el valor de esta cuota no tendrá ningún efecto en los shells remotos.</span><span class="sxs-lookup"><span data-stu-id="720d9-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="720d9-137">Recuperando información de configuración de cuota</span><span class="sxs-lookup"><span data-stu-id="720d9-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="720d9-138">Para comprobar la configuración de la cuota, escriba **WinRM Get WinRM/config**.</span><span class="sxs-lookup"><span data-stu-id="720d9-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="720d9-139">El siguiente fragmento de código es un ejemplo basado en texto de una configuración de WinRM con la configuración de cuota predeterminada.</span><span class="sxs-lookup"><span data-stu-id="720d9-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="720d9-140">Configuración de cuotas de Shell</span><span class="sxs-lookup"><span data-stu-id="720d9-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="720d9-141">Las cuotas se pueden establecer a través de un valor directiva de grupo o manualmente.</span><span class="sxs-lookup"><span data-stu-id="720d9-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="720d9-142">Para obtener más información sobre las opciones de configuración específicas, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="720d9-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="720d9-143">**Para establecer una cuota con directiva de grupo**</span><span class="sxs-lookup"><span data-stu-id="720d9-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="720d9-144">Abra una ventana de símbolo del sistema como administrador.</span><span class="sxs-lookup"><span data-stu-id="720d9-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="720d9-145">En el símbolo del sistema, escriba **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="720d9-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="720d9-146">Se abre la ventana **Editor de objetos de directiva de grupo** .</span><span class="sxs-lookup"><span data-stu-id="720d9-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="720d9-147">Busque el **administración remota de Windows** y los objetos de directiva de grupo de **Shell remoto de Windows** (GPO) en **configuración del equipo \\ plantillas administrativas componentes de \\ Windows**.</span><span class="sxs-lookup"><span data-stu-id="720d9-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="720d9-148">En la pestaña **extendido** , seleccione una opción para ver una descripción.</span><span class="sxs-lookup"><span data-stu-id="720d9-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="720d9-149">Haga doble clic en un valor para editarlo.</span><span class="sxs-lookup"><span data-stu-id="720d9-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="720d9-150">**Para establecer una cuota manualmente**</span><span class="sxs-lookup"><span data-stu-id="720d9-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="720d9-151">Abra una ventana de símbolo del sistema como administrador.</span><span class="sxs-lookup"><span data-stu-id="720d9-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="720d9-152">En el símbolo del sistema, escriba **WinRM Set WinRM/config/Winrs ' @ { ***<Quota>*** = " ***<Value>*** "} '**</span><span class="sxs-lookup"><span data-stu-id="720d9-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="720d9-153">Por ejemplo, para aumentar el número máximo de shells por usuario de 5 a 7, escriba **WinRM Set WinRM/config/Winrs ' @ {MaxShellsPerUser = "7"} '**.</span><span class="sxs-lookup"><span data-stu-id="720d9-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




