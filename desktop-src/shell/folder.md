---
description: Representa una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objeto Folder (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539520"
---
# <a name="folder-object"></a><span data-ttu-id="0c3e7-104">Folder (objeto)</span><span class="sxs-lookup"><span data-stu-id="0c3e7-104">Folder object</span></span>

<span data-ttu-id="0c3e7-105">Representa una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-105">Represents a Shell folder.</span></span> <span data-ttu-id="0c3e7-106">Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="0c3e7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c3e7-107">Members</span></span>

<span data-ttu-id="0c3e7-108">El objeto de **carpeta** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0c3e7-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="0c3e7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c3e7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c3e7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c3e7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c3e7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c3e7-111">Methods</span></span>

<span data-ttu-id="0c3e7-112">El objeto de **carpeta** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="0c3e7-113">Método</span><span class="sxs-lookup"><span data-stu-id="0c3e7-113">Method</span></span>                                      | <span data-ttu-id="0c3e7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c3e7-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c3e7-115">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="0c3e7-116">Copia un elemento o elementos en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="0c3e7-117">**GetDetailsOf**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="0c3e7-118">Recupera los detalles sobre un elemento de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="0c3e7-119">Por ejemplo, su tamaño, tipo o la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="0c3e7-120">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="0c3e7-121">Recupera un objeto [**FolderItems**](folderitems.md) que representa la colección de elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="0c3e7-122">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="0c3e7-123">Mueve un elemento o elementos a esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="0c3e7-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="0c3e7-125">Crea una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0c3e7-126">**ParseName**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="0c3e7-127">Crea y devuelve un objeto [**carpeta**](folderitem.md) que representa un elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="0c3e7-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c3e7-128">Properties</span></span>

<span data-ttu-id="0c3e7-129">El objeto de **carpeta** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="0c3e7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c3e7-130">Property</span></span>                                               | <span data-ttu-id="0c3e7-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0c3e7-131">Access type</span></span>          | <span data-ttu-id="0c3e7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c3e7-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="0c3e7-133">**Application**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="0c3e7-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c3e7-134">Read-only</span></span><br/> | <span data-ttu-id="0c3e7-135">Contiene el objeto de aplicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="0c3e7-136">**Parent**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="0c3e7-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c3e7-137">Read-only</span></span><br/> | <span data-ttu-id="0c3e7-138">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="0c3e7-139">**ParentFolder**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="0c3e7-140">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c3e7-140">Read-only</span></span><br/> | <span data-ttu-id="0c3e7-141">Contiene el objeto de **carpeta** principal.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="0c3e7-142">**Title**</span><span class="sxs-lookup"><span data-stu-id="0c3e7-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="0c3e7-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c3e7-143">Read-only</span></span><br/> | <span data-ttu-id="0c3e7-144">Contiene el título de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="0c3e7-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c3e7-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0c3e7-146">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="0c3e7-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="0c3e7-147">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="0c3e7-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="0c3e7-148">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="0c3e7-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0c3e7-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c3e7-149">Requirements</span></span>



| <span data-ttu-id="0c3e7-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c3e7-150">Requirement</span></span> | <span data-ttu-id="0c3e7-151">Value</span><span class="sxs-lookup"><span data-stu-id="0c3e7-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3e7-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c3e7-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3e7-153">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0c3e7-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="0c3e7-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c3e7-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3e7-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c3e7-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c3e7-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c3e7-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c3e7-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c3e7-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c3e7-158">IDL</span><span class="sxs-lookup"><span data-stu-id="0c3e7-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c3e7-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c3e7-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




