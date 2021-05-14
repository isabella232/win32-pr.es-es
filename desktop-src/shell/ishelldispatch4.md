---
description: Extiende el objeto IShellDispatch3.
title: Objeto IShellDispatch4 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843066"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="9dc7e-103">Objeto IShellDispatch4</span><span class="sxs-lookup"><span data-stu-id="9dc7e-103">IShellDispatch4 object</span></span>

<span data-ttu-id="9dc7e-104">Extiende el [**objeto IShellDispatch3.**](ishelldispatch3.md)</span><span class="sxs-lookup"><span data-stu-id="9dc7e-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="9dc7e-105">Además de las propiedades y los métodos admitidos por **IShellDispatch3,** **IShellDispatch4** admite cuatro métodos adicionales.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="9dc7e-106">**IShellDispatch4** se implementa y se accede a través del [**objeto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="9dc7e-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="9dc7e-107">Members</span><span class="sxs-lookup"><span data-stu-id="9dc7e-107">Members</span></span>

<span data-ttu-id="9dc7e-108">El **objeto IShellDispatch4** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9dc7e-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="9dc7e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9dc7e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9dc7e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9dc7e-110">Methods</span></span>

<span data-ttu-id="9dc7e-111">El **objeto IShellDispatch4** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="9dc7e-112">Método</span><span class="sxs-lookup"><span data-stu-id="9dc7e-112">Method</span></span>                                                     | <span data-ttu-id="9dc7e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dc7e-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="9dc7e-114">**ExplorerPolicy**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="9dc7e-115">Obtiene el valor de una directiva Internet Explorer especificada.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="9dc7e-116">**GetSetting**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="9dc7e-117">Recupera una configuración de Shell global.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="9dc7e-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="9dc7e-119">Muestra u oculta el escritorio.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="9dc7e-120">**WindowsSeguridad**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="9dc7e-121">Muestra el **cuadro Seguridad de Windows** de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="9dc7e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dc7e-122">Remarks</span></span>

<span data-ttu-id="9dc7e-123">Para obtener una explicación de los servicios de Windows, consulte la [documentación de](../services/services.md) Servicios.</span><span class="sxs-lookup"><span data-stu-id="9dc7e-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc7e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc7e-124">Requirements</span></span>



| <span data-ttu-id="9dc7e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc7e-125">Requirement</span></span> | <span data-ttu-id="9dc7e-126">Value</span><span class="sxs-lookup"><span data-stu-id="9dc7e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc7e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dc7e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc7e-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9dc7e-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9dc7e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dc7e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc7e-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dc7e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9dc7e-131">Header</span><span class="sxs-lookup"><span data-stu-id="9dc7e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dc7e-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9dc7e-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9dc7e-133">Idl</span><span class="sxs-lookup"><span data-stu-id="9dc7e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9dc7e-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9dc7e-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9dc7e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9dc7e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dc7e-136"><dt>Shell32.dll (versión 6.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9dc7e-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dc7e-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9dc7e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc7e-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="9dc7e-139">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="9dc7e-140">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="9dc7e-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="9dc7e-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="9dc7e-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
