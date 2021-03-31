---
title: Interfaz IVMDisplay (VPCCOMInterfaces. h)
description: Controla la configuración de pantalla de una máquina virtual. La interfaz IVMDisplay de una máquina virtual se puede recuperar mediante la propiedad IVMVirtualMachine display.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Interfaz IVMDisplay Virtual PC
- Interfaz IVMDisplay Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996771"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="290b5-106">Interfaz IVMDisplay</span><span class="sxs-lookup"><span data-stu-id="290b5-106">IVMDisplay interface</span></span>

<span data-ttu-id="290b5-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="290b5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="290b5-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="290b5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="290b5-109">Controla la configuración de pantalla de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="290b5-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="290b5-110">La interfaz **IVMDisplay** de una máquina virtual se puede recuperar mediante la propiedad [**IVMVirtualMachine::D**](ivmvirtualmachine-display.md) Mostrar.</span><span class="sxs-lookup"><span data-stu-id="290b5-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="290b5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="290b5-111">Members</span></span>

<span data-ttu-id="290b5-112">La interfaz **IVMDisplay** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="290b5-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="290b5-113">**IVMDisplay** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="290b5-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="290b5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="290b5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="290b5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="290b5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="290b5-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="290b5-116">Methods</span></span>

<span data-ttu-id="290b5-117">La interfaz **IVMDisplay** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="290b5-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="290b5-118">Método</span><span class="sxs-lookup"><span data-stu-id="290b5-118">Method</span></span>                                                       | <span data-ttu-id="290b5-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="290b5-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="290b5-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="290b5-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="290b5-121">Recupera una matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="290b5-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="290b5-122">**SetDimensions**</span><span class="sxs-lookup"><span data-stu-id="290b5-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="290b5-123">Establece el alto y el ancho de la pantalla de la máquina virtual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="290b5-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="290b5-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="290b5-124">Properties</span></span>

<span data-ttu-id="290b5-125">La interfaz **IVMDisplay** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="290b5-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="290b5-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="290b5-126">Property</span></span>                                             | <span data-ttu-id="290b5-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="290b5-127">Access type</span></span>          | <span data-ttu-id="290b5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="290b5-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="290b5-129">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="290b5-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="290b5-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="290b5-130">Read-only</span></span><br/> | <span data-ttu-id="290b5-131">Indica si el invitado permite cambios de resolución.</span><span class="sxs-lookup"><span data-stu-id="290b5-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="290b5-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="290b5-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="290b5-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="290b5-133">Read-only</span></span><br/> | <span data-ttu-id="290b5-134">Alto de la pantalla de la máquina virtual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="290b5-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="290b5-135">**Miniatura**</span><span class="sxs-lookup"><span data-stu-id="290b5-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="290b5-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="290b5-136">Read-only</span></span><br/> | <span data-ttu-id="290b5-137">Matriz de píxeles que representa una imagen en miniatura de la pantalla de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="290b5-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="290b5-138">**Modo**</span><span class="sxs-lookup"><span data-stu-id="290b5-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="290b5-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="290b5-139">Read-only</span></span><br/> | <span data-ttu-id="290b5-140">El modo de vídeo actual (texto, VGA, SVGA, etc.).</span><span class="sxs-lookup"><span data-stu-id="290b5-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="290b5-141">**Width**</span><span class="sxs-lookup"><span data-stu-id="290b5-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="290b5-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="290b5-142">Read-only</span></span><br/> | <span data-ttu-id="290b5-143">Ancho de la pantalla de la máquina virtual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="290b5-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="290b5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="290b5-144">Requirements</span></span>



| <span data-ttu-id="290b5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="290b5-145">Requirement</span></span> | <span data-ttu-id="290b5-146">Value</span><span class="sxs-lookup"><span data-stu-id="290b5-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="290b5-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="290b5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="290b5-148">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="290b5-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="290b5-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="290b5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="290b5-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="290b5-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="290b5-151">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="290b5-151">End of client support</span></span><br/>    | <span data-ttu-id="290b5-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="290b5-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="290b5-153">Producto</span><span class="sxs-lookup"><span data-stu-id="290b5-153">Product</span></span><br/>                  | <span data-ttu-id="290b5-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="290b5-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="290b5-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="290b5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="290b5-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="290b5-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="290b5-157">IID</span><span class="sxs-lookup"><span data-stu-id="290b5-157">IID</span></span><br/>                      | <span data-ttu-id="290b5-158">IID \_ IVMDisplay se define como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="290b5-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 

