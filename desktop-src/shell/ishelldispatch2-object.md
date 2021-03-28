---
description: Extiende el objeto IShellDispatch con una variedad de nuevas funciones.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objeto IShellDispatch2 (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984675"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="fe819-103">Objeto IShellDispatch2</span><span class="sxs-lookup"><span data-stu-id="fe819-103">IShellDispatch2 object</span></span>

<span data-ttu-id="fe819-104">Extiende el objeto [**IShellDispatch**](ishelldispatch.md) con una variedad de nuevas funciones.</span><span class="sxs-lookup"><span data-stu-id="fe819-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="fe819-105">**IShellDispatch2** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="fe819-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="fe819-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe819-106">Members</span></span>

<span data-ttu-id="fe819-107">El objeto **IShellDispatch2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fe819-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="fe819-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe819-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe819-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe819-109">Methods</span></span>

<span data-ttu-id="fe819-110">El objeto **IShellDispatch2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fe819-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="fe819-111">Método</span><span class="sxs-lookup"><span data-stu-id="fe819-111">Method</span></span>                                                               | <span data-ttu-id="fe819-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe819-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fe819-113">**CanStartStopService**</span><span class="sxs-lookup"><span data-stu-id="fe819-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="fe819-114">Determina si el usuario actual puede iniciar y detener el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="fe819-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="fe819-115">**FindPrinter**</span><span class="sxs-lookup"><span data-stu-id="fe819-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="fe819-116">Muestra el cuadro de diálogo **Buscar impresora** .</span><span class="sxs-lookup"><span data-stu-id="fe819-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="fe819-117">**GetSystemInformation**</span><span class="sxs-lookup"><span data-stu-id="fe819-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="fe819-118">Recupera información del sistema.</span><span class="sxs-lookup"><span data-stu-id="fe819-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="fe819-119">**IsRestricted**</span><span class="sxs-lookup"><span data-stu-id="fe819-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="fe819-120">Recupera el valor de restricción de un grupo del registro.</span><span class="sxs-lookup"><span data-stu-id="fe819-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="fe819-121">**IsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="fe819-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="fe819-122">Devuelve un valor que indica si se está ejecutando un servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="fe819-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="fe819-123">**ServiceStart**</span><span class="sxs-lookup"><span data-stu-id="fe819-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="fe819-124">Inicia un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="fe819-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="fe819-125">**ServiceStop**</span><span class="sxs-lookup"><span data-stu-id="fe819-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="fe819-126">Detiene un servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="fe819-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="fe819-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="fe819-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="fe819-128">Realiza una operación especificada en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fe819-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="fe819-129">**ShowBrowserBar**</span><span class="sxs-lookup"><span data-stu-id="fe819-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="fe819-130">Muestra una barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="fe819-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="fe819-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe819-131">Remarks</span></span>

<span data-ttu-id="fe819-132">Para obtener una explicación de los servicios de Windows, consulte la documentación de los [servicios](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="fe819-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe819-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe819-133">Requirements</span></span>



| <span data-ttu-id="fe819-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe819-134">Requirement</span></span> | <span data-ttu-id="fe819-135">Value</span><span class="sxs-lookup"><span data-stu-id="fe819-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe819-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe819-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fe819-137">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fe819-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe819-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe819-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fe819-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe819-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fe819-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe819-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe819-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe819-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fe819-142">IDL</span><span class="sxs-lookup"><span data-stu-id="fe819-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe819-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe819-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fe819-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe819-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe819-145"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fe819-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe819-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe819-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe819-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="fe819-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="fe819-148">**Objeto de Shell**</span><span class="sxs-lookup"><span data-stu-id="fe819-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="fe819-149">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="fe819-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
