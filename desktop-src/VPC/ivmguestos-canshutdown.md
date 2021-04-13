---
title: Propiedad IVMGuestOS CanShutdown (VPCCOMInterfaces. h)
description: Indica si el sistema operativo invitado se puede apagar correctamente.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- Propiedad CanShutdown Virtual PC
- Propiedad CanShutdown Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad CanShutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f76e652b7a172da6f5a438f72b09443a13dcce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359847"
---
# <a name="ivmguestoscanshutdown-property"></a><span data-ttu-id="d1223-106">IVMGuestOS:: CanShutdown (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d1223-106">IVMGuestOS::CanShutdown property</span></span>

<span data-ttu-id="d1223-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1223-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1223-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1223-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1223-109">Indica si el sistema operativo invitado se puede apagar sin problemas (requiere componentes de integración).</span><span class="sxs-lookup"><span data-stu-id="d1223-109">Indicates whether the guest operating system can be cleanly shut down (requires Integration Components).</span></span>

<span data-ttu-id="d1223-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1223-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1223-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1223-111">Syntax</span></span>


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a><span data-ttu-id="d1223-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d1223-112">Property value</span></span>

<span data-ttu-id="d1223-113">**Variante \_ TRUE** si el sistema operativo admite la operación de apagado y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d1223-113">**VARIANT\_TRUE** if the operating system supports the shutdown operation and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1223-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d1223-114">Error codes</span></span>



| <span data-ttu-id="d1223-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d1223-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d1223-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d1223-116">Meaning</span></span>                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="d1223-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1223-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d1223-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d1223-118">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="d1223-119"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d1223-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="d1223-120">La máquina virtual no está activada.</span><span class="sxs-lookup"><span data-stu-id="d1223-120">The virtual machine is not turned on.</span></span><br/>   |
| <dl> <span data-ttu-id="d1223-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d1223-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d1223-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d1223-122">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="d1223-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d1223-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d1223-124">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d1223-124">The virtual machine could not be found.</span></span><br/> |
| <dl> <span data-ttu-id="d1223-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1223-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d1223-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d1223-126">An unexpected error has occurred.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="d1223-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1223-127">Requirements</span></span>



| <span data-ttu-id="d1223-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1223-128">Requirement</span></span> | <span data-ttu-id="d1223-129">Value</span><span class="sxs-lookup"><span data-stu-id="d1223-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1223-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1223-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d1223-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1223-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1223-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1223-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d1223-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1223-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1223-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d1223-134">End of client support</span></span><br/>    | <span data-ttu-id="d1223-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1223-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1223-136">Producto</span><span class="sxs-lookup"><span data-stu-id="d1223-136">Product</span></span><br/>                  | <span data-ttu-id="d1223-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1223-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1223-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1223-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1223-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1223-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1223-140">IID</span><span class="sxs-lookup"><span data-stu-id="d1223-140">IID</span></span><br/>                      | <span data-ttu-id="d1223-141">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d1223-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d1223-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1223-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1223-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="d1223-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

