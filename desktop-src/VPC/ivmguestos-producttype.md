---
title: Propiedad IVMGuestOS ProductType (VPCCOMInterfaces. h)
description: Recupera el tipo de producto del sistema operativo invitado que se ejecuta en la máquina virtual.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Propiedad ProductType Virtual PC
- Propiedad ProductType Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676745"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="96e76-106">IVMGuestOS::P propiedad roductType</span><span class="sxs-lookup"><span data-stu-id="96e76-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="96e76-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96e76-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96e76-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96e76-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96e76-109">Recupera el tipo de producto del sistema operativo invitado que se ejecuta en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="96e76-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="96e76-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="96e76-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e76-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96e76-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="96e76-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="96e76-112">Property value</span></span>

<span data-ttu-id="96e76-113">El tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="96e76-113">The product type.</span></span> <span data-ttu-id="96e76-114">Se admiten los siguientes valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="96e76-114">The following string values are supported.</span></span>



| <span data-ttu-id="96e76-115">Value</span><span class="sxs-lookup"><span data-stu-id="96e76-115">Value</span></span>                                                                                  | <span data-ttu-id="96e76-116">Significado</span><span class="sxs-lookup"><span data-stu-id="96e76-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96e76-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="96e76-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="96e76-118">El sistema es un controlador de dominio y el sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="96e76-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="96e76-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="96e76-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="96e76-120">El sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="96e76-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="96e76-121">Tenga en cuenta que un servidor que también es un controlador de dominio se indica como controlador de dominio de NT de ver, no como **\_ \_ servidor de NT**. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="96e76-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="96e76-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="96e76-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="96e76-123">El sistema operativo es Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="96e76-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="96e76-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96e76-124">Requirements</span></span>



| <span data-ttu-id="96e76-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e76-125">Requirement</span></span> | <span data-ttu-id="96e76-126">Value</span><span class="sxs-lookup"><span data-stu-id="96e76-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e76-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96e76-127">Minimum supported client</span></span><br/> | <span data-ttu-id="96e76-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="96e76-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96e76-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96e76-129">Minimum supported server</span></span><br/> | <span data-ttu-id="96e76-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="96e76-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96e76-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="96e76-131">End of client support</span></span><br/>    | <span data-ttu-id="96e76-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96e76-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96e76-133">Producto</span><span class="sxs-lookup"><span data-stu-id="96e76-133">Product</span></span><br/>                  | <span data-ttu-id="96e76-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96e76-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96e76-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96e76-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e76-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e76-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96e76-137">IID</span><span class="sxs-lookup"><span data-stu-id="96e76-137">IID</span></span><br/>                      | <span data-ttu-id="96e76-138">IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="96e76-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="96e76-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="96e76-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e76-140">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="96e76-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

