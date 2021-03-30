---
title: Propiedad IVMMouse ScrollWheelPosition (VPCCOMInterfaces. h)
description: Ajusta la coordenada z del mouse (solo relativo).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Propiedad ScrollWheelPosition Virtual PC
- Propiedad ScrollWheelPosition Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, propiedad ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803740"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="3977b-106">IVMMouse:: ScrollWheelPosition (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3977b-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="3977b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3977b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3977b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3977b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3977b-109">Ajusta la coordenada z del mouse (solo relativo).</span><span class="sxs-lookup"><span data-stu-id="3977b-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="3977b-110">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="3977b-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3977b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3977b-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="3977b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3977b-112">Property value</span></span>

<span data-ttu-id="3977b-113">Coordenada z que indica el número de píxeles que se va a desplace el mouse a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="3977b-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3977b-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3977b-114">Error codes</span></span>



| <span data-ttu-id="3977b-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="3977b-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="3977b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3977b-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3977b-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3977b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="3977b-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3977b-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="3977b-119"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3977b-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="3977b-120">La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3977b-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="3977b-121"><dt>Máquina virtual \_ E \_ mouse \_ no \_ activo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="3977b-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="3977b-122">El dispositivo de mouse no se ha encendido o no está activo actualmente en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3977b-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="3977b-123"><dt>Máquina virtual \_ E \_ usar \_ \_ coordenadas absolutas</dt> <dt>0xA0040801</dt></span><span class="sxs-lookup"><span data-stu-id="3977b-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="3977b-124">No se puede establecer la posición de la rueda de desplazamiento cuando el dispositivo del mouse usa coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="3977b-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="3977b-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3977b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="3977b-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3977b-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="3977b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3977b-127">Requirements</span></span>



| <span data-ttu-id="3977b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3977b-128">Requirement</span></span> | <span data-ttu-id="3977b-129">Value</span><span class="sxs-lookup"><span data-stu-id="3977b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3977b-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3977b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3977b-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3977b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3977b-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3977b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3977b-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3977b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3977b-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3977b-134">End of client support</span></span><br/>    | <span data-ttu-id="3977b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3977b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3977b-136">Producto</span><span class="sxs-lookup"><span data-stu-id="3977b-136">Product</span></span><br/>                  | <span data-ttu-id="3977b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3977b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3977b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3977b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3977b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3977b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3977b-140">IID</span><span class="sxs-lookup"><span data-stu-id="3977b-140">IID</span></span><br/>                      | <span data-ttu-id="3977b-141">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="3977b-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="3977b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="3977b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3977b-143">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="3977b-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

