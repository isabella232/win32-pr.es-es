---
description: Tenga en cuenta que no puede especificar el orden en el que el instalador registra o anula el registro de los archivos dll de registro automático mediante las acciones SelfRegModules y SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Especificar el orden de registro automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497788"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="87e1d-103">Especificar el orden de registro automático</span><span class="sxs-lookup"><span data-stu-id="87e1d-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="87e1d-104">Tenga en cuenta que no puede especificar el orden en el que el instalador registra o anula el registro de los archivos dll de registro automático mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="87e1d-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="87e1d-105">Estas acciones registran todos los módulos que se enumeran en la [tabla SelfReg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="87e1d-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="87e1d-106">El instalador no registra automáticamente los archivos. exe.</span><span class="sxs-lookup"><span data-stu-id="87e1d-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="87e1d-107">Para especificar el orden en el que el instalador registra o anula el registro de módulos, debe usar dos [acciones personalizadas](custom-actions.md) para cada módulo.</span><span class="sxs-lookup"><span data-stu-id="87e1d-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="87e1d-108">Una acción personalizada para DllRegisterServer y otro para DllUnregisterServer.</span><span class="sxs-lookup"><span data-stu-id="87e1d-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="87e1d-109">Estas acciones personalizadas se deben crear en la [tabla InstallExecuteSequence](installexecutesequence-table.md) en el punto de la secuencia en el que se va a registrar o anular el registro del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="87e1d-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="87e1d-110">En el ejemplo siguiente se muestra cómo crear la base de datos para programar el registro automático de un archivo DLL en un punto determinado de la secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="87e1d-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="87e1d-111">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="87e1d-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="87e1d-112">Archivo</span><span class="sxs-lookup"><span data-stu-id="87e1d-112">File</span></span>  | <span data-ttu-id="87e1d-113">Componente\_</span><span class="sxs-lookup"><span data-stu-id="87e1d-113">Component\_</span></span> | <span data-ttu-id="87e1d-114">FileName</span><span class="sxs-lookup"><span data-stu-id="87e1d-114">FileName</span></span>  | <span data-ttu-id="87e1d-115">Secuencia</span><span class="sxs-lookup"><span data-stu-id="87e1d-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="87e1d-116">MYDLL</span><span class="sxs-lookup"><span data-stu-id="87e1d-116">mydll</span></span> | <span data-ttu-id="87e1d-117">myComponent</span><span class="sxs-lookup"><span data-stu-id="87e1d-117">myComponent</span></span> | <span data-ttu-id="87e1d-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="87e1d-118">Mydll.dll</span></span> | <span data-ttu-id="87e1d-119">13</span><span class="sxs-lookup"><span data-stu-id="87e1d-119">13</span></span>       |



 

<span data-ttu-id="87e1d-120">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="87e1d-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="87e1d-121">Componente</span><span class="sxs-lookup"><span data-stu-id="87e1d-121">Component</span></span>   | <span data-ttu-id="87e1d-122">ComponentId</span><span class="sxs-lookup"><span data-stu-id="87e1d-122">ComponentId</span></span> | <span data-ttu-id="87e1d-123">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="87e1d-123">Directory\_</span></span> | <span data-ttu-id="87e1d-124">Rutas</span><span class="sxs-lookup"><span data-stu-id="87e1d-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="87e1d-125">myComponent</span><span class="sxs-lookup"><span data-stu-id="87e1d-125">myComponent</span></span> | <span data-ttu-id="87e1d-126">{*un GUID*}</span><span class="sxs-lookup"><span data-stu-id="87e1d-126">{*a GUID*}</span></span>  | <span data-ttu-id="87e1d-127">myFolder</span><span class="sxs-lookup"><span data-stu-id="87e1d-127">myFolder</span></span>    | <span data-ttu-id="87e1d-128">MYDLL</span><span class="sxs-lookup"><span data-stu-id="87e1d-128">mydll</span></span>   |



 

[<span data-ttu-id="87e1d-129">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="87e1d-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="87e1d-130">Directorio</span><span class="sxs-lookup"><span data-stu-id="87e1d-130">Directory</span></span> | <span data-ttu-id="87e1d-131">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="87e1d-131">Directory\_Parent</span></span> | <span data-ttu-id="87e1d-132">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="87e1d-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="87e1d-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="87e1d-133">TARGETDIR</span></span> |                   | <span data-ttu-id="87e1d-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="87e1d-134">SourceDir</span></span>           |
| <span data-ttu-id="87e1d-135">myFolder</span><span class="sxs-lookup"><span data-stu-id="87e1d-135">myFolder</span></span>  | <span data-ttu-id="87e1d-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="87e1d-136">TARGETDIR</span></span>         | <span data-ttu-id="87e1d-137">carpeta \| mi carpeta</span><span class="sxs-lookup"><span data-stu-id="87e1d-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="87e1d-138">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="87e1d-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="87e1d-139">Acción</span><span class="sxs-lookup"><span data-stu-id="87e1d-139">Action</span></span>     | <span data-ttu-id="87e1d-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="87e1d-140">Type</span></span> | <span data-ttu-id="87e1d-141">Source</span><span class="sxs-lookup"><span data-stu-id="87e1d-141">Source</span></span>   | <span data-ttu-id="87e1d-142">Destino</span><span class="sxs-lookup"><span data-stu-id="87e1d-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="87e1d-143">mydllREG</span><span class="sxs-lookup"><span data-stu-id="87e1d-143">mydllREG</span></span>   | <span data-ttu-id="87e1d-144">3170</span><span class="sxs-lookup"><span data-stu-id="87e1d-144">3170</span></span> | <span data-ttu-id="87e1d-145">myFolder</span><span class="sxs-lookup"><span data-stu-id="87e1d-145">myFolder</span></span> | <span data-ttu-id="87e1d-146">" \[ Carpetadelsistema \] msiexec"/y " \[ \# MYDLL \] "</span><span class="sxs-lookup"><span data-stu-id="87e1d-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="87e1d-147">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="87e1d-147">mydllUNREG</span></span> | <span data-ttu-id="87e1d-148">3170</span><span class="sxs-lookup"><span data-stu-id="87e1d-148">3170</span></span> | <span data-ttu-id="87e1d-149">myFolder</span><span class="sxs-lookup"><span data-stu-id="87e1d-149">myFolder</span></span> | <span data-ttu-id="87e1d-150">" \[ Carpetadelsistema \] msiexec"/z " \[ \# MYDLL \] "</span><span class="sxs-lookup"><span data-stu-id="87e1d-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="87e1d-151">[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="87e1d-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="87e1d-152">Acción</span><span class="sxs-lookup"><span data-stu-id="87e1d-152">Action</span></span>           | <span data-ttu-id="87e1d-153">Condición</span><span class="sxs-lookup"><span data-stu-id="87e1d-153">Condition</span></span>         | <span data-ttu-id="87e1d-154">Secuencia</span><span class="sxs-lookup"><span data-stu-id="87e1d-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="87e1d-155">SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="87e1d-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="87e1d-156">2200</span><span class="sxs-lookup"><span data-stu-id="87e1d-156">2200</span></span>     |
| <span data-ttu-id="87e1d-157">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="87e1d-157">mydllUNREG</span></span>       | <span data-ttu-id="87e1d-158">$myComponent = 2</span><span class="sxs-lookup"><span data-stu-id="87e1d-158">$myComponent=2</span></span>    | <span data-ttu-id="87e1d-159">2201</span><span class="sxs-lookup"><span data-stu-id="87e1d-159">2201</span></span>     |
| <span data-ttu-id="87e1d-160">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="87e1d-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="87e1d-161">3500</span><span class="sxs-lookup"><span data-stu-id="87e1d-161">3500</span></span>     |
| <span data-ttu-id="87e1d-162">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="87e1d-162">InstallFiles</span></span>     |                   | <span data-ttu-id="87e1d-163">4000</span><span class="sxs-lookup"><span data-stu-id="87e1d-163">4000</span></span>     |
| <span data-ttu-id="87e1d-164">SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="87e1d-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="87e1d-165">6500</span><span class="sxs-lookup"><span data-stu-id="87e1d-165">6500</span></span>     |
| <span data-ttu-id="87e1d-166">mydllREG</span><span class="sxs-lookup"><span data-stu-id="87e1d-166">mydllREG</span></span>         | <span data-ttu-id="87e1d-167">$myComponent>2</span><span class="sxs-lookup"><span data-stu-id="87e1d-167">$myComponent>2</span></span> | <span data-ttu-id="87e1d-168">6501</span><span class="sxs-lookup"><span data-stu-id="87e1d-168">6501</span></span>     |



 

 

 



