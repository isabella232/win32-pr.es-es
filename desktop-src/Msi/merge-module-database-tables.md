---
description: Las tablas siguientes son necesarias en un módulo de combinación estándar.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Tablas de base de datos de módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678251"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="07124-103">Tablas de base de datos de módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="07124-103">Merge Module Database Tables</span></span>

<span data-ttu-id="07124-104">Las tablas siguientes son necesarias en un módulo de combinación estándar.</span><span class="sxs-lookup"><span data-stu-id="07124-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="07124-105">Nombre de la tabla</span><span class="sxs-lookup"><span data-stu-id="07124-105">Table name</span></span>                                       | <span data-ttu-id="07124-106">Comentario</span><span class="sxs-lookup"><span data-stu-id="07124-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07124-107">Componente</span><span class="sxs-lookup"><span data-stu-id="07124-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="07124-108">DESEE</span><span class="sxs-lookup"><span data-stu-id="07124-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="07124-109">Directorio</span><span class="sxs-lookup"><span data-stu-id="07124-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="07124-110">DESEE</span><span class="sxs-lookup"><span data-stu-id="07124-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="07124-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="07124-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="07124-112">DESEE</span><span class="sxs-lookup"><span data-stu-id="07124-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="07124-113">Archivo</span><span class="sxs-lookup"><span data-stu-id="07124-113">File</span></span>](file-table.md)                           | <span data-ttu-id="07124-114">DESEE</span><span class="sxs-lookup"><span data-stu-id="07124-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="07124-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="07124-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="07124-116">DESEE Combinados en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="07124-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="07124-117">Muestra la información que identifica un módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="07124-118">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="07124-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="07124-119">DESEE Combinados en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="07124-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="07124-120">Enumera todos los componentes del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="07124-121">Las tablas siguientes solo se producen en módulos de combinación u otras bases de datos de instalador que ya se han combinado con un módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="07124-122">Nombre de la tabla</span><span class="sxs-lookup"><span data-stu-id="07124-122">Table name</span></span>                                     | <span data-ttu-id="07124-123">Comentario</span><span class="sxs-lookup"><span data-stu-id="07124-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07124-124">ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="07124-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="07124-125">Combinados en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="07124-125">Merged into the installer database.</span></span> <span data-ttu-id="07124-126">Enumera otros módulos de combinación requeridos por este módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="07124-127">ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="07124-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="07124-128">Combinados en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="07124-128">Merged into the installer database.</span></span> <span data-ttu-id="07124-129">Enumera otros módulos de combinación que no son compatibles con este módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="07124-130">Las siguientes tablas ModuleSequence solo se producen en los módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="07124-131">Nombre de la tabla</span><span class="sxs-lookup"><span data-stu-id="07124-131">Table name</span></span>                                                             | <span data-ttu-id="07124-132">Comentario</span><span class="sxs-lookup"><span data-stu-id="07124-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07124-133">ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="07124-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="07124-134">Combina acciones en la [tabla AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="07124-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="07124-135">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07124-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="07124-136">Combina acciones en la [tabla AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="07124-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="07124-137">ModuleAdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="07124-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="07124-138">No use esta tabla.</span><span class="sxs-lookup"><span data-stu-id="07124-138">Do not use this table.</span></span> <span data-ttu-id="07124-139">Para obtener más información, consulte [tabla AdvtUISequence](advtuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="07124-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="07124-140">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07124-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="07124-141">Combina acciones en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="07124-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="07124-142">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="07124-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="07124-143">Muestra las tablas del módulo que no se combinan en el archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="07124-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="07124-144">ModuleInstallUISequence</span><span class="sxs-lookup"><span data-stu-id="07124-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="07124-145">Combina acciones en la [tabla InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="07124-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="07124-146">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07124-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="07124-147">Combina acciones en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="07124-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="07124-148">Las tablas siguientes son necesarias en cada módulo de combinación configurable.</span><span class="sxs-lookup"><span data-stu-id="07124-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="07124-149">Se requiere Mergemod.dll 2,0 o una versión posterior para crear un módulo de combinación configurable.</span><span class="sxs-lookup"><span data-stu-id="07124-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="07124-150">Para obtener más información, consulte [módulos de combinación configurables](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="07124-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="07124-151">Nombre de la tabla</span><span class="sxs-lookup"><span data-stu-id="07124-151">Table name</span></span>                                                 | <span data-ttu-id="07124-152">Comentario</span><span class="sxs-lookup"><span data-stu-id="07124-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07124-153">Tabla ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="07124-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="07124-154">DESEE Esta tabla no se combina en la base de datos de instalación de destino.</span><span class="sxs-lookup"><span data-stu-id="07124-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="07124-155">Especifica los campos configurables en la base de datos de destino y proporciona una plantilla para la configuración de cada campo.</span><span class="sxs-lookup"><span data-stu-id="07124-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="07124-156">Tabla ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="07124-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="07124-157">DESEE Esta tabla no se combina en la base de datos de instalación de destino.</span><span class="sxs-lookup"><span data-stu-id="07124-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="07124-158">Identifica los atributos configurables del módulo.</span><span class="sxs-lookup"><span data-stu-id="07124-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="07124-159">Las siguientes tablas de instalador no se pueden producir en un módulo de combinación estándar.</span><span class="sxs-lookup"><span data-stu-id="07124-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="07124-160">BBControl</span><span class="sxs-lookup"><span data-stu-id="07124-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="07124-161">Valla</span><span class="sxs-lookup"><span data-stu-id="07124-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="07124-162">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="07124-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="07124-163">Error</span><span class="sxs-lookup"><span data-stu-id="07124-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="07124-164">Característica</span><span class="sxs-lookup"><span data-stu-id="07124-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="07124-165">Tabla LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="07124-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="07124-166">Elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="07124-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="07124-167">Revisión</span><span class="sxs-lookup"><span data-stu-id="07124-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="07124-168">Actualización</span><span class="sxs-lookup"><span data-stu-id="07124-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="07124-169">Las siguientes tablas de instalador son opcionales en los módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="07124-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="07124-170">ActionText</span><span class="sxs-lookup"><span data-stu-id="07124-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="07124-171">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07124-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="07124-172">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="07124-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="07124-173">AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07124-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="07124-174">AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="07124-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="07124-175">AppId</span><span class="sxs-lookup"><span data-stu-id="07124-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="07124-176">AppSearch</span><span class="sxs-lookup"><span data-stu-id="07124-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="07124-177">BindImage</span><span class="sxs-lookup"><span data-stu-id="07124-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="07124-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="07124-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="07124-179">Clase</span><span class="sxs-lookup"><span data-stu-id="07124-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="07124-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="07124-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="07124-181">CompLocator</span><span class="sxs-lookup"><span data-stu-id="07124-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="07124-182">Control</span><span class="sxs-lookup"><span data-stu-id="07124-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="07124-183">ControlCondition</span><span class="sxs-lookup"><span data-stu-id="07124-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="07124-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="07124-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="07124-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="07124-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="07124-186">Diálogo</span><span class="sxs-lookup"><span data-stu-id="07124-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="07124-187">DrLocator</span><span class="sxs-lookup"><span data-stu-id="07124-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="07124-188">DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="07124-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="07124-189">Entorno</span><span class="sxs-lookup"><span data-stu-id="07124-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="07124-190">EventMapping</span><span class="sxs-lookup"><span data-stu-id="07124-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="07124-191">Extensión</span><span class="sxs-lookup"><span data-stu-id="07124-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="07124-192">Fuente</span><span class="sxs-lookup"><span data-stu-id="07124-192">Font</span></span>](font-table.md)
-   [<span data-ttu-id="07124-193">Icono</span><span class="sxs-lookup"><span data-stu-id="07124-193">Icon</span></span>](icon-table.md)
-   [<span data-ttu-id="07124-194">IniFile</span><span class="sxs-lookup"><span data-stu-id="07124-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="07124-195">IniLocator</span><span class="sxs-lookup"><span data-stu-id="07124-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="07124-196">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07124-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="07124-197">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="07124-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="07124-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="07124-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="07124-199">ListView</span><span class="sxs-lookup"><span data-stu-id="07124-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="07124-200">Mine</span><span class="sxs-lookup"><span data-stu-id="07124-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="07124-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="07124-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="07124-202">ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="07124-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="07124-203">ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="07124-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="07124-204">ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="07124-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="07124-205">ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="07124-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="07124-206">ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="07124-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="07124-207">Tabla ProgID</span><span class="sxs-lookup"><span data-stu-id="07124-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="07124-208">Propiedad</span><span class="sxs-lookup"><span data-stu-id="07124-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="07124-209">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="07124-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="07124-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="07124-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="07124-211">Tabla del registro</span><span class="sxs-lookup"><span data-stu-id="07124-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="07124-212">RegLocator</span><span class="sxs-lookup"><span data-stu-id="07124-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="07124-213">RemoveFile</span><span class="sxs-lookup"><span data-stu-id="07124-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="07124-214">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="07124-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="07124-215">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="07124-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="07124-216">ReserveCost</span><span class="sxs-lookup"><span data-stu-id="07124-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="07124-217">SelfReg</span><span class="sxs-lookup"><span data-stu-id="07124-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="07124-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="07124-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="07124-219">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="07124-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="07124-220">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="07124-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="07124-221">Signature</span><span class="sxs-lookup"><span data-stu-id="07124-221">Signature</span></span>](signature-table.md)
-   <span data-ttu-id="07124-222">[Estilo]](textstyle-table.md)</span><span class="sxs-lookup"><span data-stu-id="07124-222">[TextStyle](textstyle-table.md)</span></span>
-   [<span data-ttu-id="07124-223">TypeLib</span><span class="sxs-lookup"><span data-stu-id="07124-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="07124-224">UIText</span><span class="sxs-lookup"><span data-stu-id="07124-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="07124-225">Verbo</span><span class="sxs-lookup"><span data-stu-id="07124-225">Verb</span></span>](verb-table.md)

 

 



