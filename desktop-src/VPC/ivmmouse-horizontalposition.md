---
title: Propiedad IVMMouse HorizontalPosition (VPCCOMInterfaces. h)
description: Coordenada x absoluta del mouse.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Propiedad HorizontalPosition del equipo virtual
- Propiedad HorizontalPosition Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, propiedad HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8506ad0d4583b9829ca2b1832686d32e67ded261
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997043"
---
# <a name="ivmmousehorizontalposition-property"></a><span data-ttu-id="20f7b-106">IVMMouse:: HorizontalPosition (propiedad)</span><span class="sxs-lookup"><span data-stu-id="20f7b-106">IVMMouse::HorizontalPosition property</span></span>

<span data-ttu-id="20f7b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20f7b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="20f7b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="20f7b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="20f7b-109">Recupera la coordenada x absoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="20f7b-109">Retrieves the absolute x-coordinate of the mouse.</span></span>

<span data-ttu-id="20f7b-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="20f7b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f7b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20f7b-111">Syntax</span></span>


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="20f7b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="20f7b-112">Property value</span></span>

<span data-ttu-id="20f7b-113">Coordenada x que indica la nueva posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="20f7b-113">The x-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="20f7b-114">Cuando se usan coordenadas absolutas, este valor especifica la nueva coordenada x del mouse.</span><span class="sxs-lookup"><span data-stu-id="20f7b-114">When using absolute coordinates, this value specifies the new x-coordinate of the mouse.</span></span> <span data-ttu-id="20f7b-115">Cuando se usan coordenadas relativas, este valor especifica el número de píxeles que el mouse debe moverse en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="20f7b-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the x direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20f7b-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="20f7b-116">Error codes</span></span>



| <span data-ttu-id="20f7b-117">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="20f7b-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="20f7b-118">Significado</span><span class="sxs-lookup"><span data-stu-id="20f7b-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20f7b-119"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="20f7b-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="20f7b-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="20f7b-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="20f7b-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="20f7b-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="20f7b-123"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="20f7b-124">La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="20f7b-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="20f7b-125"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="20f7b-126">Los componentes de integración deben instalarse para recuperar la posición del mouse o para establecer la posición del mouse cuando se usan coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="20f7b-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="20f7b-127"><dt>Máquina virtual \_ E \_ usar \_ \_ coordenadas relativas</dt> <dt>0xA0040802</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="20f7b-128">El dispositivo de mouse está establecido actualmente para usar coordenadas relativas del mouse.</span><span class="sxs-lookup"><span data-stu-id="20f7b-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="20f7b-129"><dt>Máquina virtual \_ E \_ mouse \_ no \_ activo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="20f7b-130">No se pueden recuperar las coordenadas absolutas si el dispositivo del mouse no está encendido o si no está activo actualmente en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="20f7b-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="20f7b-131"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="20f7b-132">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="20f7b-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="20f7b-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20f7b-133">Remarks</span></span>

<span data-ttu-id="20f7b-134">No se puede recuperar esta propiedad cuando se usan coordenadas relativas.</span><span class="sxs-lookup"><span data-stu-id="20f7b-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f7b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f7b-135">Requirements</span></span>



| <span data-ttu-id="20f7b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f7b-136">Requirement</span></span> | <span data-ttu-id="20f7b-137">Value</span><span class="sxs-lookup"><span data-stu-id="20f7b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f7b-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20f7b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="20f7b-139">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="20f7b-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20f7b-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20f7b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="20f7b-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="20f7b-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="20f7b-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="20f7b-142">End of client support</span></span><br/>    | <span data-ttu-id="20f7b-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20f7b-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="20f7b-144">Producto</span><span class="sxs-lookup"><span data-stu-id="20f7b-144">Product</span></span><br/>                  | <span data-ttu-id="20f7b-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="20f7b-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="20f7b-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20f7b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="20f7b-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f7b-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="20f7b-148">IID</span><span class="sxs-lookup"><span data-stu-id="20f7b-148">IID</span></span><br/>                      | <span data-ttu-id="20f7b-149">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="20f7b-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="20f7b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="20f7b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f7b-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="20f7b-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

