---
title: Método IVMMouse SetButton (VPCCOMInterfaces. h)
description: Establece el estado actual (arriba o abajo) del botón del mouse especificado.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Método SetButton Virtual PC
- Método SetButton Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, método SetButton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150951"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="bf684-106">IVMMouse:: SetButton (método)</span><span class="sxs-lookup"><span data-stu-id="bf684-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="bf684-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf684-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bf684-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bf684-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bf684-109">Establece el estado actual (arriba o abajo) del botón del mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="bf684-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf684-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf684-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="bf684-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf684-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf684-112">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf684-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf684-113">Índice del botón.</span><span class="sxs-lookup"><span data-stu-id="bf684-113">The button index.</span></span> <span data-ttu-id="bf684-114">Para obtener una lista de valores, vea [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="bf684-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf684-115">*abajo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf684-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf684-116">Nuevo estado del botón.</span><span class="sxs-lookup"><span data-stu-id="bf684-116">The new button state.</span></span> <span data-ttu-id="bf684-117">Use **true** si el estado del botón se va a establecer en Down y **false** si se va a establecer en up.</span><span class="sxs-lookup"><span data-stu-id="bf684-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf684-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf684-118">Return value</span></span>

<span data-ttu-id="bf684-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="bf684-119">This method can return one of these values.</span></span>



| <span data-ttu-id="bf684-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf684-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="bf684-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf684-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf684-122"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf684-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="bf684-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf684-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="bf684-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="bf684-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="bf684-125">El parámetro *buttonIndex* no es válido.</span><span class="sxs-lookup"><span data-stu-id="bf684-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="bf684-126"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="bf684-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="bf684-127">La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="bf684-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="bf684-128"><dt>**Máquina virtual \_ E \_ mouse \_ no \_ activo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="bf684-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="bf684-129">No se pudo completar la operación porque el dispositivo del mouse no está encendido o no está activo actualmente en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bf684-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="bf684-130"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bf684-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="bf684-131">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="bf684-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="bf684-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf684-132">Requirements</span></span>



| <span data-ttu-id="bf684-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf684-133">Requirement</span></span> | <span data-ttu-id="bf684-134">Value</span><span class="sxs-lookup"><span data-stu-id="bf684-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf684-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf684-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf684-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf684-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf684-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf684-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf684-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bf684-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bf684-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bf684-139">End of client support</span></span><br/>    | <span data-ttu-id="bf684-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf684-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bf684-141">Producto</span><span class="sxs-lookup"><span data-stu-id="bf684-141">Product</span></span><br/>                  | <span data-ttu-id="bf684-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bf684-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bf684-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf684-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf684-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf684-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bf684-145">IID</span><span class="sxs-lookup"><span data-stu-id="bf684-145">IID</span></span><br/>                      | <span data-ttu-id="bf684-146">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="bf684-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="bf684-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf684-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf684-148">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="bf684-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

