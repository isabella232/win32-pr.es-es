---
description: Representa un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.
title: Objeto FolderItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840986"
---
# <a name="folderitem-object"></a><span data-ttu-id="a260c-104">Objeto FolderItem</span><span class="sxs-lookup"><span data-stu-id="a260c-104">FolderItem object</span></span>

<span data-ttu-id="a260c-105">Representa un elemento de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="a260c-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="a260c-106">Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="a260c-107">Members</span><span class="sxs-lookup"><span data-stu-id="a260c-107">Members</span></span>

<span data-ttu-id="a260c-108">El **objeto FolderItem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a260c-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="a260c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a260c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a260c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a260c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a260c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a260c-111">Methods</span></span>

<span data-ttu-id="a260c-112">El **objeto FolderItem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a260c-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="a260c-113">Método</span><span class="sxs-lookup"><span data-stu-id="a260c-113">Method</span></span>                                      | <span data-ttu-id="a260c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a260c-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a260c-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="a260c-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="a260c-116">Ejecuta un verbo en el elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="a260c-117">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="a260c-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="a260c-118">Recupera el objeto [**FolderItemVerbs del**](folderitemverbs.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="a260c-119">Este objeto es la colección de verbos que se pueden ejecutar en el elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a260c-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a260c-120">Properties</span></span>

<span data-ttu-id="a260c-121">El **objeto FolderItem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a260c-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="a260c-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a260c-122">Property</span></span>                                                   | <span data-ttu-id="a260c-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a260c-123">Access type</span></span>           | <span data-ttu-id="a260c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a260c-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a260c-125">**Application**</span><span class="sxs-lookup"><span data-stu-id="a260c-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="a260c-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-126">Read-only</span></span><br/>  | <span data-ttu-id="a260c-127">Contiene el [**objeto Application**](folderitem-application.md) del elemento de carpeta.</span><span class="sxs-lookup"><span data-stu-id="a260c-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="a260c-128">**Getfolder**</span><span class="sxs-lookup"><span data-stu-id="a260c-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="a260c-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-129">Read-only</span></span><br/>  | <span data-ttu-id="a260c-130">Contiene el objeto [**Folder del**](folder.md) elemento, si el elemento es una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a260c-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="a260c-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="a260c-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="a260c-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-132">Read-only</span></span><br/>  | <span data-ttu-id="a260c-133">Contiene el objeto [**ShellLinkObject del**](shelllinkobject-object.md) elemento, si el elemento es un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="a260c-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="a260c-134">**IsBrowsable**</span><span class="sxs-lookup"><span data-stu-id="a260c-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="a260c-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-135">Read-only</span></span><br/>  | <span data-ttu-id="a260c-136">Indica si el elemento se puede hospedar dentro de un explorador o Explorador de Windows marco.</span><span class="sxs-lookup"><span data-stu-id="a260c-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="a260c-137">**IsFileSystem**</span><span class="sxs-lookup"><span data-stu-id="a260c-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="a260c-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-138">Read-only</span></span><br/>  | <span data-ttu-id="a260c-139">Indica si el elemento forma parte del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a260c-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="a260c-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="a260c-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="a260c-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-141">Read-only</span></span><br/>  | <span data-ttu-id="a260c-142">Indica si el elemento es una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a260c-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="a260c-143">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="a260c-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="a260c-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-144">Read-only</span></span><br/>  | <span data-ttu-id="a260c-145">Indica si el elemento es un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="a260c-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="a260c-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="a260c-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="a260c-147">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a260c-147">Read/write</span></span><br/> | <span data-ttu-id="a260c-148">Establece u obtiene la fecha y hora en que se modificó por última vez un archivo.</span><span class="sxs-lookup"><span data-stu-id="a260c-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="a260c-149">[**ModifyDate**](folderitem-modifydate.md) se puede usar para recuperar la fecha y hora en que se modificó por última vez una carpeta, pero no se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="a260c-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="a260c-150">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a260c-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="a260c-151">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="a260c-151">Read/write</span></span><br/> | <span data-ttu-id="a260c-152">Establece u obtiene el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="a260c-153">**Parent**</span><span class="sxs-lookup"><span data-stu-id="a260c-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="a260c-154">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-154">Read-only</span></span><br/>  | <span data-ttu-id="a260c-155">Obtiene un objeto que representa el elemento primario del elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="a260c-156">**Camino**</span><span class="sxs-lookup"><span data-stu-id="a260c-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="a260c-157">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-157">Read-only</span></span><br/>  | <span data-ttu-id="a260c-158">Contiene la ruta de acceso completa y el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="a260c-159">**Size**</span><span class="sxs-lookup"><span data-stu-id="a260c-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="a260c-160">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-160">Read-only</span></span><br/>  | <span data-ttu-id="a260c-161">Contiene el tamaño del elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="a260c-162">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a260c-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="a260c-163">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a260c-163">Read-only</span></span><br/>  | <span data-ttu-id="a260c-164">Contiene una representación de cadena del tipo del elemento.</span><span class="sxs-lookup"><span data-stu-id="a260c-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="a260c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a260c-165">Requirements</span></span>



| <span data-ttu-id="a260c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="a260c-166">Requirement</span></span> | <span data-ttu-id="a260c-167">Value</span><span class="sxs-lookup"><span data-stu-id="a260c-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a260c-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a260c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a260c-169">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="a260c-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a260c-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a260c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a260c-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a260c-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a260c-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a260c-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="a260c-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a260c-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a260c-174">Idl</span><span class="sxs-lookup"><span data-stu-id="a260c-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a260c-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a260c-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a260c-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a260c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a260c-177"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a260c-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




