---
title: Propiedad IVMVirtualMachine Guests (VPCCOMInterfaces. h)
description: Recupera el sistema operativo invitado de esta máquina virtual.
ms.assetid: 9cca2a4a-e3bb-4c41-873c-e5bc4863c415
keywords:
- EQUIPO virtual de propiedad de invitados
- Propiedad de invitados Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad Guests
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GuestOS
- IVMVirtualMachine.get_GuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1042d63ebfbd62192cfbf97ff44d2226b6e4ac40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905318"
---
# <a name="ivmvirtualmachineguestos-property"></a><span data-ttu-id="a99d2-106">IVMVirtualMachine:: Guests (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a99d2-106">IVMVirtualMachine::GuestOS property</span></span>

<span data-ttu-id="a99d2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a99d2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a99d2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a99d2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a99d2-109">Recupera el sistema operativo invitado de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a99d2-109">Retrieves the guest operating system for this virtual machine.</span></span>

<span data-ttu-id="a99d2-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a99d2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99d2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a99d2-111">Syntax</span></span>


```C++
HRESULT get_GuestOS(
  [out, retval] IVMGuestOS **guestOS
);
```



## <a name="property-value"></a><span data-ttu-id="a99d2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a99d2-112">Property value</span></span>

<span data-ttu-id="a99d2-113">El objeto [**IVMGuestOS**](ivmguestos.md) .</span><span class="sxs-lookup"><span data-stu-id="a99d2-113">The [**IVMGuestOS**](ivmguestos.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a99d2-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a99d2-114">Error codes</span></span>



| <span data-ttu-id="a99d2-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="a99d2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a99d2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a99d2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a99d2-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a99d2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a99d2-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a99d2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a99d2-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a99d2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a99d2-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="a99d2-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a99d2-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a99d2-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a99d2-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="a99d2-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a99d2-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a99d2-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a99d2-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a99d2-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a99d2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a99d2-125">Requirements</span></span>



| <span data-ttu-id="a99d2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a99d2-126">Requirement</span></span> | <span data-ttu-id="a99d2-127">Value</span><span class="sxs-lookup"><span data-stu-id="a99d2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a99d2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a99d2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a99d2-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a99d2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a99d2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a99d2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a99d2-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a99d2-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a99d2-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a99d2-132">End of client support</span></span><br/>    | <span data-ttu-id="a99d2-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a99d2-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a99d2-134">Producto</span><span class="sxs-lookup"><span data-stu-id="a99d2-134">Product</span></span><br/>                  | <span data-ttu-id="a99d2-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a99d2-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a99d2-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a99d2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a99d2-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a99d2-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a99d2-138">IID</span><span class="sxs-lookup"><span data-stu-id="a99d2-138">IID</span></span><br/>                      | <span data-ttu-id="a99d2-139">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a99d2-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a99d2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a99d2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99d2-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="a99d2-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

