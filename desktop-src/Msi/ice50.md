---
description: ICE50 comprueba que se especifican los iconos de acceso directo para que se muestren correctamente y coincidan con la extensión del archivo de destino.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002562"
---
# <a name="ice50"></a><span data-ttu-id="681ea-103">ICE50</span><span class="sxs-lookup"><span data-stu-id="681ea-103">ICE50</span></span>

<span data-ttu-id="681ea-104">ICE50 comprueba que se especifican los iconos de acceso directo para que se muestren correctamente y coincidan con la extensión del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="681ea-104">ICE50 checks that shortcut icons are specified to display correctly and match their target file's extension.</span></span>

## <a name="result"></a><span data-ttu-id="681ea-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="681ea-105">Result</span></span>

<span data-ttu-id="681ea-106">ICE50 envía un mensaje de error si la extensión del icono y los archivos de destino no coinciden.</span><span class="sxs-lookup"><span data-stu-id="681ea-106">ICE50 posts an error message if the extension of the icon and target files do not match.</span></span> <span data-ttu-id="681ea-107">ICE50 publica una advertencia si los iconos se almacenan en archivos que no tienen una extensión. exe o. ico.</span><span class="sxs-lookup"><span data-stu-id="681ea-107">ICE50 posts a warning if icons are stored in files that do not have an .exe or .ico extension.</span></span>

## <a name="example"></a><span data-ttu-id="681ea-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="681ea-108">Example</span></span>

<span data-ttu-id="681ea-109">ICE50 notifica el siguiente error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="681ea-109">ICE50 reports the following error for the example shown.</span></span>



| <span data-ttu-id="681ea-110">Error o advertencia de ICE50</span><span class="sxs-lookup"><span data-stu-id="681ea-110">ICE50 error or warning</span></span>                                                                                                              | <span data-ttu-id="681ea-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="681ea-111">Description</span></span>                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="681ea-112">La extensión del icono ' Icon2. dat ' para el acceso directo ' Shortcut2 ' no coincide con la extensión del archivo de clave del componente ' Component2 '.</span><span class="sxs-lookup"><span data-stu-id="681ea-112">The extension of Icon 'Icon2.dat' for Shortcut 'Shortcut2' does not match the extension of the Key File for component 'Component2'.</span></span> | <span data-ttu-id="681ea-113">Si las extensiones del icono y del archivo de destino no coinciden, el acceso directo no tendrá el menú contextual correcto cuando se anuncie el componente.</span><span class="sxs-lookup"><span data-stu-id="681ea-113">If the extensions of the icon and the target file do not match, the shortcut will not have the correct context menu when the component is advertised.</span></span> <span data-ttu-id="681ea-114">Para corregir este error, cambie el nombre del icono para que coincida con la extensión del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="681ea-114">To fix this error, rename the icon to match the extension of the target file.</span></span><br/> |
| <span data-ttu-id="681ea-115">La extensión del icono ' Icon1.bat ' para el acceso directo ' Shortcut1 ' no es ' exe ' ni ' ico '.</span><span class="sxs-lookup"><span data-stu-id="681ea-115">The extension of Icon 'Icon1.bat' for Shortcut 'Shortcut1' is not "exe" or "ico".</span></span> <span data-ttu-id="681ea-116">El icono no se mostrará correctamente.</span><span class="sxs-lookup"><span data-stu-id="681ea-116">The Icon will not be displayed correctly.</span></span>         | <span data-ttu-id="681ea-117">No todas las versiones del shell muestran correctamente los iconos almacenados en archivos que no tienen extensiones de "exe" o "ICO".</span><span class="sxs-lookup"><span data-stu-id="681ea-117">Not all versions of the shell correctly display icons stored in files that do not have extensions of "exe" or "ico".</span></span> <span data-ttu-id="681ea-118">Para corregir esta advertencia, cambie el nombre del icono por la extensión "exe" o "ICO".</span><span class="sxs-lookup"><span data-stu-id="681ea-118">To fix this warning, rename the icon have an extension of "exe" or "ico".</span></span><br/>                                      |



 

<span data-ttu-id="681ea-119">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="681ea-119">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="681ea-120">Archivo</span><span class="sxs-lookup"><span data-stu-id="681ea-120">File</span></span>  | <span data-ttu-id="681ea-121">FileName</span><span class="sxs-lookup"><span data-stu-id="681ea-121">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="681ea-122">Archivo1</span><span class="sxs-lookup"><span data-stu-id="681ea-122">File1</span></span> | <span data-ttu-id="681ea-123">File1.bat</span><span class="sxs-lookup"><span data-stu-id="681ea-123">File1.bat</span></span> |
| <span data-ttu-id="681ea-124">Archivo2</span><span class="sxs-lookup"><span data-stu-id="681ea-124">File2</span></span> | <span data-ttu-id="681ea-125">File2.pl</span><span class="sxs-lookup"><span data-stu-id="681ea-125">File2.pl</span></span>  |



 

<span data-ttu-id="681ea-126">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="681ea-126">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="681ea-127">Característica</span><span class="sxs-lookup"><span data-stu-id="681ea-127">Feature</span></span>  |
|----------|
| <span data-ttu-id="681ea-128">Feature1</span><span class="sxs-lookup"><span data-stu-id="681ea-128">Feature1</span></span> |



 

<span data-ttu-id="681ea-129">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="681ea-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="681ea-130">Componente</span><span class="sxs-lookup"><span data-stu-id="681ea-130">Component</span></span>  | <span data-ttu-id="681ea-131">Rutas</span><span class="sxs-lookup"><span data-stu-id="681ea-131">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="681ea-132">Component1</span><span class="sxs-lookup"><span data-stu-id="681ea-132">Component1</span></span> | <span data-ttu-id="681ea-133">Archivo1</span><span class="sxs-lookup"><span data-stu-id="681ea-133">File1</span></span>   |
| <span data-ttu-id="681ea-134">Component2</span><span class="sxs-lookup"><span data-stu-id="681ea-134">Component2</span></span> | <span data-ttu-id="681ea-135">Archivo2</span><span class="sxs-lookup"><span data-stu-id="681ea-135">File2</span></span>   |



 

[<span data-ttu-id="681ea-136">Tabla de iconos</span><span class="sxs-lookup"><span data-stu-id="681ea-136">Icon Table</span></span>](icon-table.md)



| <span data-ttu-id="681ea-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="681ea-137">Name</span></span>      | <span data-ttu-id="681ea-138">Datos</span><span class="sxs-lookup"><span data-stu-id="681ea-138">Data</span></span>            |
|-----------|-----------------|
| <span data-ttu-id="681ea-139">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="681ea-139">Icon1.bat</span></span> | <span data-ttu-id="681ea-140">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="681ea-140">\[Binary Data\]</span></span> |
| <span data-ttu-id="681ea-141">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="681ea-141">Icon2.dat</span></span> | <span data-ttu-id="681ea-142">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="681ea-142">\[Binary Data\]</span></span> |



 

<span data-ttu-id="681ea-143">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="681ea-143">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="681ea-144">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="681ea-144">Shortcut</span></span>  | <span data-ttu-id="681ea-145">Componente</span><span class="sxs-lookup"><span data-stu-id="681ea-145">Component</span></span>  | <span data-ttu-id="681ea-146">Destino</span><span class="sxs-lookup"><span data-stu-id="681ea-146">Target</span></span>   | <span data-ttu-id="681ea-147">Icono\_</span><span class="sxs-lookup"><span data-stu-id="681ea-147">Icon\_</span></span>    |
|-----------|------------|----------|-----------|
| <span data-ttu-id="681ea-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="681ea-148">Shortcut1</span></span> | <span data-ttu-id="681ea-149">Component1</span><span class="sxs-lookup"><span data-stu-id="681ea-149">Component1</span></span> | <span data-ttu-id="681ea-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="681ea-150">Feature1</span></span> | <span data-ttu-id="681ea-151">Icon1.bat</span><span class="sxs-lookup"><span data-stu-id="681ea-151">Icon1.bat</span></span> |
| <span data-ttu-id="681ea-152">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="681ea-152">Shortcut2</span></span> | <span data-ttu-id="681ea-153">Component2</span><span class="sxs-lookup"><span data-stu-id="681ea-153">Component2</span></span> | <span data-ttu-id="681ea-154">Feature1</span><span class="sxs-lookup"><span data-stu-id="681ea-154">Feature1</span></span> | <span data-ttu-id="681ea-155">Icon2. dat</span><span class="sxs-lookup"><span data-stu-id="681ea-155">Icon2.dat</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="681ea-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="681ea-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="681ea-157">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="681ea-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




