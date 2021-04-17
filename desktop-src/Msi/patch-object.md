---
description: El objeto patch representa una instancia única de una revisión que se ha registrado o aplicado. Se puede crear una instancia del objeto con la propiedad patch como &\# 0034; WindowsInstaller. Installer. patch (PatchCode, ProductCode, UserSid, context) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653373"
---
# <a name="patch-object"></a><span data-ttu-id="dcc74-103">Patch (objeto)</span><span class="sxs-lookup"><span data-stu-id="dcc74-103">Patch object</span></span>

<span data-ttu-id="dcc74-104">El objeto **patch** representa una instancia única de una revisión que se ha registrado o aplicado.</span><span class="sxs-lookup"><span data-stu-id="dcc74-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="dcc74-105">Se puede crear una instancia del objeto con la propiedad **patch** como "WindowsInstaller. Installer. patch (*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span><span class="sxs-lookup"><span data-stu-id="dcc74-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="dcc74-106">En el contexto de un equipo, el parámetro *UserSid* debe ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="dcc74-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="dcc74-107">*ProductCode* se puede establecer en una cadena vacía para las revisiones que solo se registran y aún no se aplican a ningún producto.</span><span class="sxs-lookup"><span data-stu-id="dcc74-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="dcc74-108">*ProductCode* se puede establecer en una cadena vacía cuando solo se lee o se actualiza la información de la lista de origen de una revisión.</span><span class="sxs-lookup"><span data-stu-id="dcc74-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="dcc74-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dcc74-109">Members</span></span>

<span data-ttu-id="dcc74-110">El objeto **patch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dcc74-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="dcc74-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dcc74-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dcc74-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dcc74-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dcc74-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dcc74-113">Methods</span></span>

<span data-ttu-id="dcc74-114">El objeto **patch** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dcc74-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="dcc74-115">Método</span><span class="sxs-lookup"><span data-stu-id="dcc74-115">Method</span></span>                                                               | <span data-ttu-id="dcc74-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcc74-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcc74-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="dcc74-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="dcc74-118">Agregue un disco al conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="dcc74-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="dcc74-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="dcc74-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="dcc74-120">Agregue una red o un origen de URL a la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dcc74-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="dcc74-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="dcc74-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="dcc74-122">Borra la lista de origen completa del tipo de orígenes especificado.</span><span class="sxs-lookup"><span data-stu-id="dcc74-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="dcc74-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="dcc74-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="dcc74-124">Quitar un disco del conjunto de discos registrados de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dcc74-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="dcc74-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="dcc74-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="dcc74-126">Quite una red o un origen de la dirección URL de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dcc74-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="dcc74-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="dcc74-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="dcc74-128">Borra el origen usado por última vez de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="dcc74-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="dcc74-129">Esto fuerza la resolución de una lista de origen la próxima vez que se requiera el origen.</span><span class="sxs-lookup"><span data-stu-id="dcc74-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dcc74-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dcc74-130">Properties</span></span>

<span data-ttu-id="dcc74-131">El objeto **patch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dcc74-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="dcc74-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dcc74-132">Property</span></span>                                                  | <span data-ttu-id="dcc74-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcc74-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcc74-134">**Context**</span><span class="sxs-lookup"><span data-stu-id="dcc74-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="dcc74-135">El contexto de esta instancia de Patch es un valor de MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="dcc74-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="dcc74-136">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="dcc74-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="dcc74-137">Enumera todos los discos multimedia para esta instancia de patch.</span><span class="sxs-lookup"><span data-stu-id="dcc74-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="dcc74-138">**PatchCode**</span><span class="sxs-lookup"><span data-stu-id="dcc74-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="dcc74-139">Devuelve el código de revisión.</span><span class="sxs-lookup"><span data-stu-id="dcc74-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="dcc74-140">**PatchProperty**</span><span class="sxs-lookup"><span data-stu-id="dcc74-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="dcc74-141">Obtiene información de propiedades sobre una revisión específica aplicada a una instancia específica del producto.</span><span class="sxs-lookup"><span data-stu-id="dcc74-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="dcc74-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="dcc74-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="dcc74-143">Devuelve el código de producto.</span><span class="sxs-lookup"><span data-stu-id="dcc74-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="dcc74-144">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="dcc74-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="dcc74-145">Obtiene y establece las propiedades de información de origen.</span><span class="sxs-lookup"><span data-stu-id="dcc74-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="dcc74-146">Se trata de una propiedad de lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="dcc74-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="dcc74-147">**Orígenes**</span><span class="sxs-lookup"><span data-stu-id="dcc74-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="dcc74-148">Enumera todos los orígenes de esta instancia de patch.</span><span class="sxs-lookup"><span data-stu-id="dcc74-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="dcc74-149">**State**</span><span class="sxs-lookup"><span data-stu-id="dcc74-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="dcc74-150">Estado de instalación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="dcc74-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="dcc74-151">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="dcc74-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="dcc74-152">Devuelve el SID de usuario, en la cuenta que esta instancia de revisión está disponible.</span><span class="sxs-lookup"><span data-stu-id="dcc74-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="dcc74-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcc74-153">Requirements</span></span>



| <span data-ttu-id="dcc74-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc74-154">Requirement</span></span> | <span data-ttu-id="dcc74-155">Value</span><span class="sxs-lookup"><span data-stu-id="dcc74-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc74-156">Versión</span><span class="sxs-lookup"><span data-stu-id="dcc74-156">Version</span></span><br/> | <span data-ttu-id="dcc74-157">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dcc74-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dcc74-158">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dcc74-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dcc74-159">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="dcc74-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="dcc74-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dcc74-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="dcc74-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcc74-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="dcc74-162">IID</span><span class="sxs-lookup"><span data-stu-id="dcc74-162">IID</span></span><br/>     | <span data-ttu-id="dcc74-163">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dcc74-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="dcc74-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcc74-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc74-165">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dcc74-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




