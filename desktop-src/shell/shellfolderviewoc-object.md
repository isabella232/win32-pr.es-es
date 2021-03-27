---
description: Reenvía los eventos desencadenados por un objeto ShellFolderView especificado a los controladores de eventos ShellFolderViewOC correspondientes.
title: Objeto ShellFolderViewOC (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002723"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="e2453-103">Objeto ShellFolderViewOC</span><span class="sxs-lookup"><span data-stu-id="e2453-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="e2453-104">Reenvía los eventos desencadenados por un objeto [**ShellFolderView**](shellfolderview.md) especificado a los controladores de eventos **ShellFolderViewOC** correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e2453-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="e2453-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2453-105">Members</span></span>

<span data-ttu-id="e2453-106">El objeto **ShellFolderViewOC** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e2453-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="e2453-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="e2453-107">Events</span></span>](#events)
-   [<span data-ttu-id="e2453-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2453-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="e2453-109">Eventos</span><span class="sxs-lookup"><span data-stu-id="e2453-109">Events</span></span>

<span data-ttu-id="e2453-110">El objeto **ShellFolderViewOC** tiene estos eventos.</span><span class="sxs-lookup"><span data-stu-id="e2453-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="e2453-111">Evento</span><span class="sxs-lookup"><span data-stu-id="e2453-111">Event</span></span>                                                          | <span data-ttu-id="e2453-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2453-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2453-113">**EnumDone**</span><span class="sxs-lookup"><span data-stu-id="e2453-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="e2453-114">Indica que el objeto [**ShellFolderView**](shellfolderview.md) ha terminado de enumerar el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e2453-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="e2453-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="e2453-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="e2453-116">Indica que ha cambiado el estado de selección de uno o varios elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="e2453-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="e2453-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2453-117">Methods</span></span>

<span data-ttu-id="e2453-118">El objeto **ShellFolderViewOC** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e2453-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="e2453-119">Método</span><span class="sxs-lookup"><span data-stu-id="e2453-119">Method</span></span>                                                   | <span data-ttu-id="e2453-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2453-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2453-121">**SetFolderView**</span><span class="sxs-lookup"><span data-stu-id="e2453-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="e2453-122">Reenvía los eventos del objeto [**ShellFolderView**](shellfolderview.md) especificado al controlador de eventos **ShellFolderViewOC** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e2453-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2453-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2453-123">Remarks</span></span>

<span data-ttu-id="e2453-124">El objeto [**ShellFolderView**](shellfolderview.md) activa dos eventos, [**EnumDone**](shellfolderviewoc-enumdone.md) y [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), que suelen controlar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e2453-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="e2453-125">Sin embargo, algunas aplicaciones deben controlar eventos de una serie de objetos **ShellFolderView** .</span><span class="sxs-lookup"><span data-stu-id="e2453-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="e2453-126">Por ejemplo, una aplicación podría hospedar un control WebBrowser que permite a los usuarios navegar por una serie de carpetas.</span><span class="sxs-lookup"><span data-stu-id="e2453-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="e2453-127">Cada carpeta tiene su propio objeto **ShellFolderView** con sus eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="e2453-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="e2453-128">Controlar estos eventos puede ser difícil.</span><span class="sxs-lookup"><span data-stu-id="e2453-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="e2453-129">El objeto **ShellFolderViewOC** simplifica el control de eventos para tales escenarios.</span><span class="sxs-lookup"><span data-stu-id="e2453-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="e2453-130">Permite que las aplicaciones controlen eventos para todos los objetos [**ShellFolderView**](shellfolderview.md) con un solo par de controladores de eventos **ShellFolderViewOC** .</span><span class="sxs-lookup"><span data-stu-id="e2453-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="e2453-131">Cada vez que el usuario navega a una nueva carpeta, la aplicación pasa el objeto **ShellFolderView** asociado al objeto **ShellFolderViewOC** mediante una llamada a [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span><span class="sxs-lookup"><span data-stu-id="e2453-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="e2453-132">A continuación, cuando se desencadena un evento [**EnumDone**](shellfolderviewoc-enumdone.md) o [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) , el objeto **ShellFolderViewOC** reenvía el evento a su propio controlador para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e2453-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2453-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2453-133">Requirements</span></span>



| <span data-ttu-id="e2453-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2453-134">Requirement</span></span> | <span data-ttu-id="e2453-135">Value</span><span class="sxs-lookup"><span data-stu-id="e2453-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2453-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2453-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e2453-137">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e2453-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2453-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2453-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e2453-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2453-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e2453-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2453-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2453-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2453-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e2453-142">IDL</span><span class="sxs-lookup"><span data-stu-id="e2453-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2453-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2453-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e2453-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2453-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2453-145"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e2453-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2453-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2453-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2453-147">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="e2453-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




