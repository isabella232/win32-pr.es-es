---
title: Propiedad IVMGuestOS ScreenLocked (VPCCOMInterfaces. h)
description: Indica si la pantalla del sistema operativo invitado está bloqueada.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Propiedad ScreenLocked Virtual PC
- Propiedad ScreenLocked Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad ScreenLocked
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079472"
---
# <a name="ivmguestosscreenlocked-property"></a><span data-ttu-id="8fb1e-106">IVMGuestOS:: ScreenLocked (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8fb1e-106">IVMGuestOS::ScreenLocked property</span></span>

<span data-ttu-id="8fb1e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8fb1e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8fb1e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8fb1e-109">Indica si la pantalla del sistema operativo invitado está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-109">Indicates whether the screen in the guest operating system is locked.</span></span>

<span data-ttu-id="8fb1e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb1e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fb1e-111">Syntax</span></span>


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a><span data-ttu-id="8fb1e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8fb1e-112">Property value</span></span>

<span data-ttu-id="8fb1e-113">**Variante \_ TRUE** si la pantalla está bloqueada en el sistema operativo invitado, **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-113">**VARIANT\_TRUE** if screen is locked in guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8fb1e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8fb1e-114">Error codes</span></span>



| <span data-ttu-id="8fb1e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="8fb1e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="8fb1e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8fb1e-116">Meaning</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fb1e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8fb1e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8fb1e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-118">The operation was successful.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="8fb1e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8fb1e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="8fb1e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-120">The parameter is **NULL**.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="8fb1e-121"><dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8fb1e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8fb1e-122">La máquina virtual (VM) debe estar en ejecución para esta operación.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-122">The virtual machine (VM) must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="8fb1e-123"><dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="8fb1e-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8fb1e-124">La característica componentes de integración no está habilitada en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-124">The integration components feature is not enabled in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="8fb1e-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8fb1e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8fb1e-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="8fb1e-126">An unexpected error has occurred.</span></span><br/>                                                |



## <a name="requirements"></a><span data-ttu-id="8fb1e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fb1e-127">Requirements</span></span>



| <span data-ttu-id="8fb1e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb1e-128">Requirement</span></span> | <span data-ttu-id="8fb1e-129">Value</span><span class="sxs-lookup"><span data-stu-id="8fb1e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb1e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fb1e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb1e-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fb1e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fb1e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fb1e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb1e-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8fb1e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8fb1e-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8fb1e-134">End of client support</span></span><br/>    | <span data-ttu-id="8fb1e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8fb1e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8fb1e-136">Producto</span><span class="sxs-lookup"><span data-stu-id="8fb1e-136">Product</span></span><br/>                  | <span data-ttu-id="8fb1e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8fb1e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8fb1e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fb1e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb1e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb1e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8fb1e-140">IID</span><span class="sxs-lookup"><span data-stu-id="8fb1e-140">IID</span></span><br/>                      | <span data-ttu-id="8fb1e-141">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8fb1e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8fb1e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fb1e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb1e-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8fb1e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

