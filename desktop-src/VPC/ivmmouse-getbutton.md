---
title: Método IVMMouse GetButton (VPCCOMInterfaces. h)
description: Recupera el estado actual del botón del mouse especificado.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Método GetButton Virtual PC
- Método GetButton Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, método GetButton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803745"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="e8e39-106">IVMMouse:: GetButton (método)</span><span class="sxs-lookup"><span data-stu-id="e8e39-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="e8e39-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8e39-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8e39-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8e39-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8e39-109">Recupera el estado actual (arriba o abajo) del botón del mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="e8e39-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e39-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8e39-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="e8e39-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8e39-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e39-112">*buttonIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8e39-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8e39-113">Índice del botón cuyo estado se va a solicitar.</span><span class="sxs-lookup"><span data-stu-id="e8e39-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="e8e39-114">Para obtener una lista de valores, vea [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="e8e39-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8e39-115">*isDown* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e8e39-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e8e39-116">Estado del botón indicado.</span><span class="sxs-lookup"><span data-stu-id="e8e39-116">The state of the indicated button.</span></span> <span data-ttu-id="e8e39-117">**True** si el botón está inactivo actualmente en la máquina virtual; en caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="e8e39-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e39-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8e39-118">Return value</span></span>

<span data-ttu-id="e8e39-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e8e39-119">This method can return one of these values.</span></span>



| <span data-ttu-id="e8e39-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8e39-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="e8e39-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8e39-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8e39-122"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="e8e39-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8e39-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e8e39-124"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="e8e39-125">El parámetro *isDown* es **null**.</span><span class="sxs-lookup"><span data-stu-id="e8e39-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="e8e39-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="e8e39-127">El parámetro *buttonIndex* no es válido.</span><span class="sxs-lookup"><span data-stu-id="e8e39-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e8e39-128"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="e8e39-129">La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e8e39-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="e8e39-130"><dt>**Máquina virtual \_ E \_ mouse \_ no \_ activo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="e8e39-131">No se ha encendido el dispositivo de mouse.</span><span class="sxs-lookup"><span data-stu-id="e8e39-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e8e39-132"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="e8e39-133">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e8e39-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="e8e39-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8e39-134">Requirements</span></span>



| <span data-ttu-id="e8e39-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e39-135">Requirement</span></span> | <span data-ttu-id="e8e39-136">Value</span><span class="sxs-lookup"><span data-stu-id="e8e39-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e39-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e39-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e39-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8e39-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8e39-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e39-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e39-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e8e39-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8e39-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e8e39-141">End of client support</span></span><br/>    | <span data-ttu-id="e8e39-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8e39-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8e39-143">Producto</span><span class="sxs-lookup"><span data-stu-id="e8e39-143">Product</span></span><br/>                  | <span data-ttu-id="e8e39-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8e39-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8e39-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8e39-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e39-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e39-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8e39-147">IID</span><span class="sxs-lookup"><span data-stu-id="e8e39-147">IID</span></span><br/>                      | <span data-ttu-id="e8e39-148">IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="e8e39-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="e8e39-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e39-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e39-150">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="e8e39-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

