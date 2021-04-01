---
title: Interfaz IVMMouse (VPCCOMInterfaces. h)
description: Controla el dispositivo de mouse dentro de una máquina virtual.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Interfaz IVMMouse Virtual PC
- Interfaz IVMMouse Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905532"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="e4c4e-105">Interfaz IVMMouse</span><span class="sxs-lookup"><span data-stu-id="e4c4e-105">IVMMouse interface</span></span>

<span data-ttu-id="e4c4e-106">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e4c4e-107">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e4c4e-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e4c4e-108">Controla el dispositivo de mouse dentro de una máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="e4c4e-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="e4c4e-109">El **IVMMouse** de una máquina virtual se puede recuperar mediante la propiedad [**IVMVirtualMachine:: mouse**](ivmvirtualmachine-mouse.md) .</span><span class="sxs-lookup"><span data-stu-id="e4c4e-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="e4c4e-110">Las coordenadas del dispositivo de mouse se pueden representar en coordenadas absolutas o en coordenadas diferenciales.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="e4c4e-111">Use la propiedad [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) para distinguir entre los dos métodos de representación de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="e4c4e-112">Tenga en cuenta que la recuperación de la posición actual del cursor y el uso de coordenadas absolutas solo se admiten si el sistema operativo invitado tiene instalados los componentes de integración.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="e4c4e-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4c4e-113">Members</span></span>

<span data-ttu-id="e4c4e-114">La interfaz **IVMMouse** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="e4c4e-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e4c4e-115">**IVMMouse** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e4c4e-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="e4c4e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4c4e-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4c4e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4c4e-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4c4e-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4c4e-118">Methods</span></span>

<span data-ttu-id="e4c4e-119">La interfaz **IVMMouse** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="e4c4e-120">Método</span><span class="sxs-lookup"><span data-stu-id="e4c4e-120">Method</span></span>                                  | <span data-ttu-id="e4c4e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4c4e-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e4c4e-122">**Hizo**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="e4c4e-123">Simula un clic del botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="e4c4e-124">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="e4c4e-125">Recupera el estado actual (arriba o abajo) del botón del mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="e4c4e-126">**SetButton**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="e4c4e-127">Establece el estado actual (arriba o abajo) del botón del mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="e4c4e-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4c4e-128">Properties</span></span>

<span data-ttu-id="e4c4e-129">La interfaz **IVMMouse** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="e4c4e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e4c4e-130">Property</span></span>                                                                         | <span data-ttu-id="e4c4e-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="e4c4e-131">Access type</span></span>           | <span data-ttu-id="e4c4e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4c4e-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4c4e-133">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="e4c4e-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e4c4e-134">Read/write</span></span><br/> | <span data-ttu-id="e4c4e-135">Coordenada x absoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="e4c4e-136">**ScrollWheelPosition**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="e4c4e-137">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="e4c4e-137">Write-only</span></span><br/> | <span data-ttu-id="e4c4e-138">Coordenada z del mouse (solo relativo).</span><span class="sxs-lookup"><span data-stu-id="e4c4e-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="e4c4e-139">**UsingAbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="e4c4e-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e4c4e-140">Read/write</span></span><br/> | <span data-ttu-id="e4c4e-141">Indica si las coordenadas del mouse representan coordenadas absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="e4c4e-142">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="e4c4e-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="e4c4e-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e4c4e-143">Read/write</span></span><br/> | <span data-ttu-id="e4c4e-144">Coordenada y absoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="e4c4e-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="e4c4e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4c4e-145">Requirements</span></span>



| <span data-ttu-id="e4c4e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c4e-146">Requirement</span></span> | <span data-ttu-id="e4c4e-147">Value</span><span class="sxs-lookup"><span data-stu-id="e4c4e-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c4e-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4c4e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c4e-149">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4c4e-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4c4e-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4c4e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c4e-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e4c4e-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e4c4e-152">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e4c4e-152">End of client support</span></span><br/>    | <span data-ttu-id="e4c4e-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4c4e-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e4c4e-154">Producto</span><span class="sxs-lookup"><span data-stu-id="e4c4e-154">Product</span></span><br/>                  | <span data-ttu-id="e4c4e-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e4c4e-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e4c4e-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4c4e-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c4e-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4c4e-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e4c4e-158">IID</span><span class="sxs-lookup"><span data-stu-id="e4c4e-158">IID</span></span><br/>                      | <span data-ttu-id="e4c4e-159">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="e4c4e-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 

