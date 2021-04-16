---
title: Interfaz IVMKeyboard (VPCCOMInterfaces. h)
description: Controla el dispositivo de teclado dentro de una máquina virtual. El IVMKeyboard de una máquina virtual se puede recuperar mediante la propiedad de teclado IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Interfaz IVMKeyboard Virtual PC
- Interfaz IVMKeyboard Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696042"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="0b6e3-106">Interfaz IVMKeyboard</span><span class="sxs-lookup"><span data-stu-id="0b6e3-106">IVMKeyboard interface</span></span>

<span data-ttu-id="0b6e3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b6e3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b6e3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b6e3-109">Controla el dispositivo de teclado dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="0b6e3-110">El **IVMKeyboard** de una máquina virtual se puede recuperar mediante la propiedad [**IVMVirtualMachine:: Keyboard**](ivmvirtualmachine-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="0b6e3-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="0b6e3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b6e3-111">Members</span></span>

<span data-ttu-id="0b6e3-112">La interfaz **IVMKeyboard** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0b6e3-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0b6e3-113">**IVMKeyboard** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b6e3-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="0b6e3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b6e3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b6e3-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b6e3-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b6e3-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b6e3-116">Methods</span></span>

<span data-ttu-id="0b6e3-117">La interfaz **IVMKeyboard** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="0b6e3-118">Método</span><span class="sxs-lookup"><span data-stu-id="0b6e3-118">Method</span></span>                                                       | <span data-ttu-id="0b6e3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b6e3-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="0b6e3-120">**IsPressed**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="0b6e3-121">Determina si la tecla especificada está presionada.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="0b6e3-122">**PressAndReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="0b6e3-123">Simula que se presiona una tecla y luego se libera.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="0b6e3-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="0b6e3-125">Simula que se presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="0b6e3-126">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="0b6e3-127">Simula una clave que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="0b6e3-128">**TypeAsciiText**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="0b6e3-129">Simula una serie de claves ASCII que se escriben en el invitado.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="0b6e3-130">**TypeKeySequence**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="0b6e3-131">Simula una lista delimitada por comas de las claves que se escriben en el invitado.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0b6e3-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b6e3-132">Properties</span></span>

<span data-ttu-id="0b6e3-133">La interfaz **IVMKeyboard** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="0b6e3-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b6e3-134">Property</span></span>                                                                | <span data-ttu-id="0b6e3-135">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0b6e3-135">Access type</span></span>           | <span data-ttu-id="0b6e3-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b6e3-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b6e3-137">**HasExclusiveAccess**</span><span class="sxs-lookup"><span data-stu-id="0b6e3-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="0b6e3-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b6e3-138">Read/write</span></span><br/> | <span data-ttu-id="0b6e3-139">Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b6e3-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b6e3-140">Remarks</span></span>

<span data-ttu-id="0b6e3-141">Las claves se pueden escribir en la máquina virtual de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="0b6e3-142">Para escribir una secuencia ASCII normal de caracteres, utilice el método [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) .</span><span class="sxs-lookup"><span data-stu-id="0b6e3-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="0b6e3-143">Si se requiere una mayor flexibilidad, **IVMKeyboard** tiene varios métodos que están diseñados para usarse con los códigos de tecla de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="0b6e3-144">El método [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) puede aceptar una cadena delimitada por comas de códigos de tecla, que se presionarán y liberarán, en orden, dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="0b6e3-145">Además de estos códigos de tecla, se pueden usar las palabras clave hacia arriba y hacia abajo para forzar que una clave se presione solamente o se libere.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="0b6e3-146">Las palabras clave UP y DOWN solo se aplican al código de tecla que sigue directamente a la palabra clave.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="0b6e3-147">Para evitar que varios scripts, aplicaciones o usuarios intenten acceder simultáneamente al mismo dispositivo de teclado, establezca la propiedad [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="0b6e3-148">Si un proceso adquiere acceso exclusivo, cualquier intento por parte de otros procesos para enviar entradas al dispositivo de teclado se omitirá hasta que se libere el acceso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0b6e3-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6e3-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6e3-149">Requirements</span></span>



| <span data-ttu-id="0b6e3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6e3-150">Requirement</span></span> | <span data-ttu-id="0b6e3-151">Value</span><span class="sxs-lookup"><span data-stu-id="0b6e3-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6e3-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b6e3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6e3-153">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b6e3-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b6e3-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b6e3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6e3-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b6e3-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b6e3-156">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0b6e3-156">End of client support</span></span><br/>    | <span data-ttu-id="0b6e3-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b6e3-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b6e3-158">Producto</span><span class="sxs-lookup"><span data-stu-id="0b6e3-158">Product</span></span><br/>                  | <span data-ttu-id="0b6e3-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b6e3-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b6e3-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b6e3-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b6e3-161"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b6e3-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b6e3-162">IID</span><span class="sxs-lookup"><span data-stu-id="0b6e3-162">IID</span></span><br/>                      | <span data-ttu-id="0b6e3-163">IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="0b6e3-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0b6e3-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b6e3-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6e3-165">Interfaces de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b6e3-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0b6e3-166">Secuencias de claves</span><span class="sxs-lookup"><span data-stu-id="0b6e3-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

