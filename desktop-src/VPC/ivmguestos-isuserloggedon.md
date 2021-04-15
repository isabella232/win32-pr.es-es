---
title: Método IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Determina si la sesión solicitada está presente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Método IsUserLoggedOn Virtual PC
- Método IsUserLoggedOn Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695870"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="08b5a-106">IVMGuestOS:: IsUserLoggedOn (método)</span><span class="sxs-lookup"><span data-stu-id="08b5a-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="08b5a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="08b5a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="08b5a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="08b5a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="08b5a-109">Determina si la sesión solicitada está presente.</span><span class="sxs-lookup"><span data-stu-id="08b5a-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b5a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08b5a-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="08b5a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08b5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b5a-112">*inRailSession* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08b5a-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b5a-113">Establezca en 0 para una sesión de raíl o 1 para una sesión de RDP.</span><span class="sxs-lookup"><span data-stu-id="08b5a-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="08b5a-114">*outSessionPresent* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="08b5a-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="08b5a-115">Establézcalo en **Variant \_ true** si la sesión está presente y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="08b5a-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b5a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08b5a-116">Return value</span></span>

<span data-ttu-id="08b5a-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="08b5a-117">This method can return one of these values.</span></span>



| <span data-ttu-id="08b5a-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08b5a-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="08b5a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="08b5a-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08b5a-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="08b5a-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="08b5a-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="08b5a-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="08b5a-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="08b5a-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="08b5a-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="08b5a-125">El parámetro *outSessionPresent* no es válido o es **null**.</span><span class="sxs-lookup"><span data-stu-id="08b5a-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="08b5a-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="08b5a-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="08b5a-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="08b5a-128"><dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="08b5a-129">No hay suficiente memoria disponible para completar esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="08b5a-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="08b5a-130"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="08b5a-131">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="08b5a-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="08b5a-132"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="08b5a-133">La máquina virtual (VM) debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="08b5a-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="08b5a-134"><dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="08b5a-135">La característica componentes de integración no está instalada en esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08b5a-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="08b5a-136"><dt>**Máquina virtual \_ E/s de \_ VM en \_ pausa**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="08b5a-137">La máquina virtual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="08b5a-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="08b5a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b5a-138">Requirements</span></span>



| <span data-ttu-id="08b5a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b5a-139">Requirement</span></span> | <span data-ttu-id="08b5a-140">Value</span><span class="sxs-lookup"><span data-stu-id="08b5a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b5a-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08b5a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="08b5a-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="08b5a-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08b5a-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08b5a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="08b5a-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="08b5a-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="08b5a-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="08b5a-145">End of client support</span></span><br/>    | <span data-ttu-id="08b5a-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="08b5a-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="08b5a-147">Producto</span><span class="sxs-lookup"><span data-stu-id="08b5a-147">Product</span></span><br/>                  | <span data-ttu-id="08b5a-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="08b5a-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="08b5a-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08b5a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="08b5a-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="08b5a-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="08b5a-151">IID</span><span class="sxs-lookup"><span data-stu-id="08b5a-151">IID</span></span><br/>                      | <span data-ttu-id="08b5a-152">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="08b5a-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="08b5a-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="08b5a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b5a-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="08b5a-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

