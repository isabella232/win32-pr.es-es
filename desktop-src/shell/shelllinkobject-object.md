---
description: Administra vínculos de Shell. Este objeto hace que gran parte de la funcionalidad de la interfaz IShellLink esté disponible para las aplicaciones de scripting.
title: Objeto ShellLinkObject (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986026"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="7cf59-104">Objeto ShellLinkObject</span><span class="sxs-lookup"><span data-stu-id="7cf59-104">ShellLinkObject object</span></span>

<span data-ttu-id="7cf59-105">Administra vínculos de Shell.</span><span class="sxs-lookup"><span data-stu-id="7cf59-105">Manages Shell links.</span></span> <span data-ttu-id="7cf59-106">Este objeto hace que gran parte de la funcionalidad de la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) esté disponible para las aplicaciones de scripting.</span><span class="sxs-lookup"><span data-stu-id="7cf59-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="7cf59-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7cf59-107">Members</span></span>

<span data-ttu-id="7cf59-108">El objeto **ShellLinkObject** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7cf59-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="7cf59-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7cf59-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7cf59-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cf59-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7cf59-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7cf59-111">Methods</span></span>

<span data-ttu-id="7cf59-112">El objeto **ShellLinkObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7cf59-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="7cf59-113">Método</span><span class="sxs-lookup"><span data-stu-id="7cf59-113">Method</span></span>                                                     | <span data-ttu-id="7cf59-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cf59-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cf59-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="7cf59-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="7cf59-116">Obtiene la ubicación del icono asignado al vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="7cf59-117">**Resolver**</span><span class="sxs-lookup"><span data-stu-id="7cf59-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="7cf59-118">Busca el destino de un vínculo de Shell, incluso si el destino se ha quitado o cambiado de nombre.</span><span class="sxs-lookup"><span data-stu-id="7cf59-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="7cf59-119">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="7cf59-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="7cf59-120">Guarda todos los cambios realizados en el vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="7cf59-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="7cf59-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="7cf59-122">Establece la ubicación del icono asignado al vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="7cf59-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cf59-123">Properties</span></span>

<span data-ttu-id="7cf59-124">El objeto **ShellLinkObject** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7cf59-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="7cf59-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7cf59-125">Property</span></span>                                                                | <span data-ttu-id="7cf59-126">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="7cf59-126">Access type</span></span>           | <span data-ttu-id="7cf59-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cf59-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cf59-128">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="7cf59-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="7cf59-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cf59-129">Read/write</span></span><br/> | <span data-ttu-id="7cf59-130">Contiene los argumentos de un vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="7cf59-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cf59-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="7cf59-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cf59-132">Read/write</span></span><br/> | <span data-ttu-id="7cf59-133">Obtiene o establece la descripción del vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="7cf59-134">**Tecla de acceso rápido**</span><span class="sxs-lookup"><span data-stu-id="7cf59-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="7cf59-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cf59-135">Read/write</span></span><br/> | <span data-ttu-id="7cf59-136">Obtiene o establece el método abreviado de teclado para el vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="7cf59-137">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="7cf59-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="7cf59-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cf59-138">Read/write</span></span><br/> | <span data-ttu-id="7cf59-139">Obtiene o establece la ruta de acceso al objeto de vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="7cf59-140">**Información showcommand**</span><span class="sxs-lookup"><span data-stu-id="7cf59-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="7cf59-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cf59-141">Read/write</span></span><br/> | <span data-ttu-id="7cf59-142">Obtiene o establece el estado de presentación inicial (con tamaño, minimizada o maximizada) del comando del vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="7cf59-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="7cf59-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="7cf59-144">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cf59-144">Read/write</span></span><br/> | <span data-ttu-id="7cf59-145">Obtiene o establece el directorio de trabajo especificado en el vínculo.</span><span class="sxs-lookup"><span data-stu-id="7cf59-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="7cf59-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf59-146">Requirements</span></span>



| <span data-ttu-id="7cf59-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cf59-147">Requirement</span></span> | <span data-ttu-id="7cf59-148">Value</span><span class="sxs-lookup"><span data-stu-id="7cf59-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf59-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cf59-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf59-150">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7cf59-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7cf59-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cf59-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf59-152">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7cf59-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7cf59-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cf59-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cf59-154"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf59-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7cf59-155">IDL</span><span class="sxs-lookup"><span data-stu-id="7cf59-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7cf59-156"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cf59-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7cf59-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7cf59-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf59-158"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7cf59-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf59-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cf59-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf59-160">Vínculos de Shell</span><span class="sxs-lookup"><span data-stu-id="7cf59-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
