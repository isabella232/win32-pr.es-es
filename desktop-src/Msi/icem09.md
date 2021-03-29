---
description: ICEM09 comprueba que el módulo de mezcla controla los directorios predefinidos de forma segura.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277748"
---
# <a name="icem09"></a><span data-ttu-id="825d6-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="825d6-103">ICEM09</span></span>

<span data-ttu-id="825d6-104">ICEM09 comprueba que el módulo de mezcla controla los directorios predefinidos de forma segura.</span><span class="sxs-lookup"><span data-stu-id="825d6-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="825d6-105">Para ello, comprueba que ningún componente del módulo instala un directorio en un directorio del sistema predefinido como "ProgramFilesFolder" o "StartMenuFolder".</span><span class="sxs-lookup"><span data-stu-id="825d6-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="825d6-106">En su lugar, los módulos deben usar directorios con nombres únicos (creados con la Convención de nomenclatura del módulo de combinación) y usar acciones personalizadas para el directorio de destino adecuado.</span><span class="sxs-lookup"><span data-stu-id="825d6-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="825d6-107">Este enfoque impide que los módulos entren en conflicto con una estructura de directorios existente en la base de datos final.</span><span class="sxs-lookup"><span data-stu-id="825d6-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="825d6-108">ICEM09 comprueba que las acciones personalizadas necesarias para que funcione esta técnica no existan (para que la herramienta de combinación pueda generarlas) o que existan en el formato correcto (de modo que funcionen según lo esperado).</span><span class="sxs-lookup"><span data-stu-id="825d6-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="825d6-109">Si no se corrige una advertencia o un error informados por ICEM09, podrían producirse problemas en los clientes del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="825d6-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="825d6-110">Las filas de la tabla de directorio con claves principales como ProgramFilesFolder suelen existir en una base de datos; por lo tanto, si los componentes del módulo se instalan directamente en directorios predefinidos como ProgramFilesFolder, las entradas de directorio del módulo pueden entrar en conflicto con las filas ya existentes.</span><span class="sxs-lookup"><span data-stu-id="825d6-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="825d6-111">Esta condición requeriría que el usuario del módulo dividira los archivos de origen del módulo para que coincidan con el directorio de origen existente.</span><span class="sxs-lookup"><span data-stu-id="825d6-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="825d6-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="825d6-112">Result</span></span>

<span data-ttu-id="825d6-113">ICEM09 informa de un error o una advertencia cuando un componente de módulo instala un directorio en un directorio del sistema predefinido, lo que provoca un conflicto de nombres con la estructura de directorios existente.</span><span class="sxs-lookup"><span data-stu-id="825d6-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="825d6-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="825d6-114">Example</span></span>

<span data-ttu-id="825d6-115">ICEM09 envía las siguientes advertencias para un módulo que contiene las entradas de base de datos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="825d6-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="825d6-116">Cambie el nombre del directorio del módulo de combinación para que no coincida con una propiedad de Windows Installer y, por tanto, sea único.</span><span class="sxs-lookup"><span data-stu-id="825d6-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="825d6-117">A continuación, establezca una propiedad con el mismo nombre en el valor del directorio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="825d6-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="825d6-118">Cuando tiene lugar la resolución del directorio, el directorio tiene una propiedad con el mismo nombre, por lo que la ubicación de instalación del directorio es el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="825d6-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="825d6-119">Los archivos se mueven de la ubicación de origen distinta a la misma ubicación de destino.</span><span class="sxs-lookup"><span data-stu-id="825d6-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="825d6-120">Este proceso debe quitar por completo los conflictos de combinación.</span><span class="sxs-lookup"><span data-stu-id="825d6-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="825d6-121">Si la acción no tiene el número de secuencia 1, es posible que no se mezcle en la base de datos de destino lo suficientemente pronto en la secuencia para que funcione de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="825d6-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="825d6-122">Para corregir esta advertencia, establezca el número de secuencia en 1.</span><span class="sxs-lookup"><span data-stu-id="825d6-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="825d6-123">Tenga en cuenta que la mayoría de las herramientas de combinación más recientes (pero no algunas versiones anteriores) generarán estas acciones personalizadas en el momento de la combinación, por lo que no siempre es necesario crear explícitamente las acciones en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="825d6-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="825d6-124">Dado que la columna CustomAction es la clave principal de la tabla CustomAction, algunas herramientas de combinación pueden generar acciones duplicadas porque el nombre de la acción previamente creada es diferente.</span><span class="sxs-lookup"><span data-stu-id="825d6-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="825d6-125">Para corregir esta advertencia, asigne a la acción el mismo nombre que el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="825d6-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="825d6-126">Tenga en cuenta que la mayoría de las herramientas de combinación más recientes (pero no algunas versiones anteriores) generan estas acciones personalizadas en el momento de la combinación, por lo que no siempre es necesario crear explícitamente las acciones en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="825d6-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="825d6-127">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="825d6-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="825d6-128">Directorio</span><span class="sxs-lookup"><span data-stu-id="825d6-128">Directory</span></span>          | <span data-ttu-id="825d6-129">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="825d6-129">Directory\_Parent</span></span> | <span data-ttu-id="825d6-130">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="825d6-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="825d6-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-131">ProgramFilesFolder</span></span> | <span data-ttu-id="825d6-132">Directory1</span><span class="sxs-lookup"><span data-stu-id="825d6-132">Directory1</span></span>        | <span data-ttu-id="825d6-133">A</span><span class="sxs-lookup"><span data-stu-id="825d6-133">A</span></span>          |
| <span data-ttu-id="825d6-134">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-134">StartMenuFolder</span></span>    | <span data-ttu-id="825d6-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="825d6-135">Directory2</span></span>        | <span data-ttu-id="825d6-136">B:C</span><span class="sxs-lookup"><span data-stu-id="825d6-136">B:C</span></span>        |
| <span data-ttu-id="825d6-137">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-137">AppDataFolder</span></span>      | <span data-ttu-id="825d6-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="825d6-138">Directory3</span></span>        | <span data-ttu-id="825d6-139">D</span><span class="sxs-lookup"><span data-stu-id="825d6-139">D</span></span>          |
| <span data-ttu-id="825d6-140">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-140">MyPicturesFolder</span></span>   | <span data-ttu-id="825d6-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="825d6-141">Directory4</span></span>        | <span data-ttu-id="825d6-142">E</span><span class="sxs-lookup"><span data-stu-id="825d6-142">E</span></span>          |



 

[<span data-ttu-id="825d6-143">Tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="825d6-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="825d6-144">Componente</span><span class="sxs-lookup"><span data-stu-id="825d6-144">Component</span></span>               | <span data-ttu-id="825d6-145">Directorio</span><span class="sxs-lookup"><span data-stu-id="825d6-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="825d6-146">Component1.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-146">Component1.<GUID></span></span> | <span data-ttu-id="825d6-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="825d6-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-148">Component2.<GUID></span></span> | <span data-ttu-id="825d6-149">StartMenuFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="825d6-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-150">Component3.<GUID></span></span> | <span data-ttu-id="825d6-151">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-151">AppDataFolder</span></span>      |
| <span data-ttu-id="825d6-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-152">Component4.<GUID></span></span> | <span data-ttu-id="825d6-153">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="825d6-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="825d6-154">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="825d6-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="825d6-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="825d6-155">CustomAction</span></span>                 | <span data-ttu-id="825d6-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="825d6-156">Type</span></span> | <span data-ttu-id="825d6-157">Source</span><span class="sxs-lookup"><span data-stu-id="825d6-157">Source</span></span>                       | <span data-ttu-id="825d6-158">Destino</span><span class="sxs-lookup"><span data-stu-id="825d6-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="825d6-159">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="825d6-160">51</span><span class="sxs-lookup"><span data-stu-id="825d6-160">51</span></span>   | <span data-ttu-id="825d6-161">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="825d6-162">\[StartMenuFolder\]</span><span class="sxs-lookup"><span data-stu-id="825d6-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="825d6-163">MyAppDataFolderAction</span><span class="sxs-lookup"><span data-stu-id="825d6-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="825d6-164">51</span><span class="sxs-lookup"><span data-stu-id="825d6-164">51</span></span>   | <span data-ttu-id="825d6-165">AppDataFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="825d6-166">\[AppDataFolder\]</span><span class="sxs-lookup"><span data-stu-id="825d6-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="825d6-167">Tabla ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="825d6-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="825d6-168">Acción</span><span class="sxs-lookup"><span data-stu-id="825d6-168">Action</span></span>                       | <span data-ttu-id="825d6-169">Secuencia</span><span class="sxs-lookup"><span data-stu-id="825d6-169">Sequence</span></span> | <span data-ttu-id="825d6-170">BaseAction</span><span class="sxs-lookup"><span data-stu-id="825d6-170">BaseAction</span></span> | <span data-ttu-id="825d6-171">Después</span><span class="sxs-lookup"><span data-stu-id="825d6-171">After</span></span> | <span data-ttu-id="825d6-172">Condición</span><span class="sxs-lookup"><span data-stu-id="825d6-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="825d6-173">StartMenuFolder.<GUID></span><span class="sxs-lookup"><span data-stu-id="825d6-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="825d6-174">100</span><span class="sxs-lookup"><span data-stu-id="825d6-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="825d6-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="825d6-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825d6-176">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="825d6-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



