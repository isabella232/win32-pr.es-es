---
title: Propiedad IVMHostInfo ParallelPort (VPCCOMInterfaces. h)
description: Recupera el puerto paralelo del host que se puede adjuntar al invitado.
ms.assetid: 4c9486b8-ab66-4874-b467-a7a0ab7934f1
keywords:
- Propiedad ParallelPort Virtual PC
- Propiedad ParallelPort Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad ParallelPort
topic_type:
- apiref
api_name:
- IVMHostInfo.ParallelPort
- IVMHostInfo.get_ParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0a2050ff505f5ed7a54cf3857ea28661d4d3d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533735"
---
# <a name="ivmhostinfoparallelport-property"></a><span data-ttu-id="889f9-106">IVMHostInfo::P propiedad arallelPort</span><span class="sxs-lookup"><span data-stu-id="889f9-106">IVMHostInfo::ParallelPort property</span></span>

<span data-ttu-id="889f9-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="889f9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="889f9-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="889f9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="889f9-109">Recupera el puerto paralelo del host que se puede adjuntar al invitado.</span><span class="sxs-lookup"><span data-stu-id="889f9-109">Retrieves the host parallel port that can be attached to the guest.</span></span>

<span data-ttu-id="889f9-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="889f9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="889f9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="889f9-111">Syntax</span></span>


```C++
HRESULT get_ParallelPort(
  [out, retval] BSTR *vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="889f9-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="889f9-112">Property value</span></span>

<span data-ttu-id="889f9-113">Nombre del puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="889f9-113">The name of the parallel port.</span></span>

## <a name="error-codes"></a><span data-ttu-id="889f9-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="889f9-114">Error codes</span></span>



| <span data-ttu-id="889f9-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="889f9-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="889f9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="889f9-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="889f9-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="889f9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="889f9-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="889f9-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="889f9-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="889f9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="889f9-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="889f9-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="889f9-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="889f9-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="889f9-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="889f9-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="889f9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="889f9-123">Requirements</span></span>



| <span data-ttu-id="889f9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="889f9-124">Requirement</span></span> | <span data-ttu-id="889f9-125">Value</span><span class="sxs-lookup"><span data-stu-id="889f9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="889f9-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="889f9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="889f9-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="889f9-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="889f9-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="889f9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="889f9-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="889f9-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="889f9-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="889f9-130">End of client support</span></span><br/>    | <span data-ttu-id="889f9-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="889f9-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="889f9-132">Producto</span><span class="sxs-lookup"><span data-stu-id="889f9-132">Product</span></span><br/>                  | <span data-ttu-id="889f9-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="889f9-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="889f9-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="889f9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="889f9-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="889f9-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="889f9-136">IID</span><span class="sxs-lookup"><span data-stu-id="889f9-136">IID</span></span><br/>                      | <span data-ttu-id="889f9-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="889f9-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="889f9-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="889f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889f9-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="889f9-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

