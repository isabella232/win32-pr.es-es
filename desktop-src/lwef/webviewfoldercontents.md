---
title: Objeto WebViewFolderContents (Shldisp.h)
description: Implementado por el shell para su uso dentro de un WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Objeto WebViewFolderContents características de entorno de Windows heredadas
- Objeto WebViewFolderContents características de entorno de Windows heredado, descritas
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714537"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="f0eab-105">Objeto WebViewFolderContents</span><span class="sxs-lookup"><span data-stu-id="f0eab-105">WebViewFolderContents object</span></span>

<span data-ttu-id="f0eab-106">Implementado por el shell para su uso dentro de un *WebView*.</span><span class="sxs-lookup"><span data-stu-id="f0eab-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="f0eab-107">**WebViewFolderContents** se inicializa automáticamente en la carpeta actual de WebView.</span><span class="sxs-lookup"><span data-stu-id="f0eab-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="f0eab-108">Crea una vista de carpeta de Shell que muestra el contenido de la carpeta en uno de los cinco formatos siguientes: icono pequeño, icono grande, lista, detalles o miniatura.</span><span class="sxs-lookup"><span data-stu-id="f0eab-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="f0eab-109">No es válido fuera de un WebView.</span><span class="sxs-lookup"><span data-stu-id="f0eab-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="f0eab-110">Los métodos y propiedades expuestos por **WebViewFolderContents** son idénticos a los del objeto [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .</span><span class="sxs-lookup"><span data-stu-id="f0eab-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="f0eab-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0eab-111">Members</span></span>

<span data-ttu-id="f0eab-112">El objeto **WebViewFolderContents** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0eab-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="f0eab-113">Eventos</span><span class="sxs-lookup"><span data-stu-id="f0eab-113">Events</span></span>](#events)
-   [<span data-ttu-id="f0eab-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f0eab-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="f0eab-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0eab-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="f0eab-116">Events</span><span class="sxs-lookup"><span data-stu-id="f0eab-116">Events</span></span>

<span data-ttu-id="f0eab-117">El objeto **WebViewFolderContents** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="f0eab-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="f0eab-118">Evento</span><span class="sxs-lookup"><span data-stu-id="f0eab-118">Event</span></span>                                                              | <span data-ttu-id="f0eab-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0eab-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eab-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="f0eab-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="f0eab-121">Se produce cuando cambia el estado de selección de cualquier elemento o elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="f0eab-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="f0eab-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="f0eab-122">Methods</span></span>

<span data-ttu-id="f0eab-123">El objeto **WebViewFolderContents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f0eab-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="f0eab-124">Método</span><span class="sxs-lookup"><span data-stu-id="f0eab-124">Method</span></span>                                                       | <span data-ttu-id="f0eab-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0eab-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eab-126">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="f0eab-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="f0eab-127">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f0eab-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="f0eab-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="f0eab-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="f0eab-129">Obtiene un objeto [**FolderItems**](../shell/folderitems.md) que representa todos los elementos seleccionados en la vista.</span><span class="sxs-lookup"><span data-stu-id="f0eab-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="f0eab-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="f0eab-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="f0eab-131">Establece el estado de selección de un elemento en la vista.</span><span class="sxs-lookup"><span data-stu-id="f0eab-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="f0eab-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0eab-132">Properties</span></span>

<span data-ttu-id="f0eab-133">El objeto **WebViewFolderContents** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0eab-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="f0eab-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f0eab-134">Property</span></span>                                                            | <span data-ttu-id="f0eab-135">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f0eab-135">Access type</span></span>          | <span data-ttu-id="f0eab-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0eab-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eab-137">**Application**</span><span class="sxs-lookup"><span data-stu-id="f0eab-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="f0eab-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0eab-138">Read-only</span></span><br/> | <span data-ttu-id="f0eab-139">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="f0eab-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f0eab-140">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="f0eab-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="f0eab-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0eab-141">Read-only</span></span><br/> | <span data-ttu-id="f0eab-142">Obtiene un objeto [**carpeta**](../shell/folderitem.md) que representa el elemento que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="f0eab-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="f0eab-143">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="f0eab-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="f0eab-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0eab-144">Read-only</span></span><br/> | <span data-ttu-id="f0eab-145">Obtiene un objeto de [**carpeta**](../shell/folder.md) que representa la vista.</span><span class="sxs-lookup"><span data-stu-id="f0eab-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="f0eab-146">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f0eab-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="f0eab-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0eab-147">Read-only</span></span><br/> | <span data-ttu-id="f0eab-148">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="f0eab-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f0eab-149">**Script**</span><span class="sxs-lookup"><span data-stu-id="f0eab-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="f0eab-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0eab-150">Read-only</span></span><br/> | <span data-ttu-id="f0eab-151">Obtiene el objeto de scripting para la vista.</span><span class="sxs-lookup"><span data-stu-id="f0eab-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="f0eab-152">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="f0eab-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="f0eab-153">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0eab-153">Read-only</span></span><br/> | <span data-ttu-id="f0eab-154">Obtiene un conjunto de marcas [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indican las opciones actuales de la vista.</span><span class="sxs-lookup"><span data-stu-id="f0eab-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f0eab-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0eab-155">Requirements</span></span>



| <span data-ttu-id="f0eab-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0eab-156">Requirement</span></span> | <span data-ttu-id="f0eab-157">Value</span><span class="sxs-lookup"><span data-stu-id="f0eab-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0eab-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0eab-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f0eab-159">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f0eab-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f0eab-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0eab-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f0eab-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0eab-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0eab-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0eab-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0eab-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0eab-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f0eab-164">IDL</span><span class="sxs-lookup"><span data-stu-id="f0eab-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0eab-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0eab-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f0eab-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0eab-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0eab-167"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f0eab-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

