---
description: Representa los objetos en una vista y proporciona propiedades y métodos que se usan para obtener información sobre el contenido de la vista.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Objeto ShellFolderView (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997865"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="63ebc-103">Objeto ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="63ebc-103">ShellFolderView object</span></span>

<span data-ttu-id="63ebc-104">Representa los objetos en una vista y proporciona propiedades y métodos que se usan para obtener información sobre el contenido de la vista.</span><span class="sxs-lookup"><span data-stu-id="63ebc-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="63ebc-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="63ebc-105">Members</span></span>

<span data-ttu-id="63ebc-106">El objeto **ShellFolderView** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63ebc-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="63ebc-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="63ebc-107">Events</span></span>](#events)
-   [<span data-ttu-id="63ebc-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="63ebc-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="63ebc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63ebc-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="63ebc-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="63ebc-110">Events</span></span>

<span data-ttu-id="63ebc-111">El objeto **ShellFolderView** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="63ebc-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="63ebc-112">Evento</span><span class="sxs-lookup"><span data-stu-id="63ebc-112">Event</span></span>                                                        | <span data-ttu-id="63ebc-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="63ebc-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="63ebc-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="63ebc-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="63ebc-115">Se produce cuando cambia el estado de selección de cualquier elemento o elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="63ebc-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="63ebc-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="63ebc-116">Methods</span></span>

<span data-ttu-id="63ebc-117">El objeto **ShellFolderView** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="63ebc-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="63ebc-118">Método</span><span class="sxs-lookup"><span data-stu-id="63ebc-118">Method</span></span>                                                 | <span data-ttu-id="63ebc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="63ebc-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63ebc-120">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="63ebc-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="63ebc-121">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="63ebc-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="63ebc-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="63ebc-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="63ebc-123">Obtiene un objeto [**FolderItems**](folderitems.md) que representa todos los elementos seleccionados en la vista.</span><span class="sxs-lookup"><span data-stu-id="63ebc-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="63ebc-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="63ebc-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="63ebc-125">Establece el estado de selección de un elemento en la vista.</span><span class="sxs-lookup"><span data-stu-id="63ebc-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="63ebc-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63ebc-126">Properties</span></span>

<span data-ttu-id="63ebc-127">El objeto **ShellFolderView** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63ebc-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="63ebc-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63ebc-128">Property</span></span>                                                      | <span data-ttu-id="63ebc-129">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="63ebc-129">Access type</span></span>          | <span data-ttu-id="63ebc-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="63ebc-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63ebc-131">**Application**</span><span class="sxs-lookup"><span data-stu-id="63ebc-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="63ebc-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ebc-132">Read-only</span></span><br/> | <span data-ttu-id="63ebc-133">Contiene el objeto de aplicación del objeto.</span><span class="sxs-lookup"><span data-stu-id="63ebc-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="63ebc-134">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="63ebc-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="63ebc-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ebc-135">Read-only</span></span><br/> | <span data-ttu-id="63ebc-136">Obtiene un objeto [**carpeta**](folderitem.md) que representa el elemento que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="63ebc-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="63ebc-137">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="63ebc-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="63ebc-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ebc-138">Read-only</span></span><br/> | <span data-ttu-id="63ebc-139">Obtiene un objeto de [**carpeta**](folder.md) que representa la vista.</span><span class="sxs-lookup"><span data-stu-id="63ebc-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="63ebc-140">**Parent**</span><span class="sxs-lookup"><span data-stu-id="63ebc-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="63ebc-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ebc-141">Read-only</span></span><br/> | <span data-ttu-id="63ebc-142">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="63ebc-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="63ebc-143">**Script**</span><span class="sxs-lookup"><span data-stu-id="63ebc-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="63ebc-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ebc-144">Read-only</span></span><br/> | <span data-ttu-id="63ebc-145">En desuso.</span><span class="sxs-lookup"><span data-stu-id="63ebc-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="63ebc-146">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="63ebc-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="63ebc-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ebc-147">Read-only</span></span><br/> | <span data-ttu-id="63ebc-148">Obtiene un conjunto de marcas que indican las opciones actuales de la vista.</span><span class="sxs-lookup"><span data-stu-id="63ebc-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="63ebc-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ebc-149">Requirements</span></span>



| <span data-ttu-id="63ebc-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ebc-150">Requirement</span></span> | <span data-ttu-id="63ebc-151">Value</span><span class="sxs-lookup"><span data-stu-id="63ebc-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ebc-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ebc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="63ebc-153">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="63ebc-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="63ebc-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ebc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="63ebc-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63ebc-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63ebc-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63ebc-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="63ebc-157"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63ebc-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="63ebc-158">IDL</span><span class="sxs-lookup"><span data-stu-id="63ebc-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63ebc-159"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63ebc-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="63ebc-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63ebc-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63ebc-161"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="63ebc-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="63ebc-162">IID</span><span class="sxs-lookup"><span data-stu-id="63ebc-162">IID</span></span><br/>                      | <span data-ttu-id="63ebc-163">CLSID \_ ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="63ebc-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="63ebc-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ebc-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ebc-165">**Marcas de ShellFolderViewOptions**</span><span class="sxs-lookup"><span data-stu-id="63ebc-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




