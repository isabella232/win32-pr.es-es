---
title: Propiedad de memoria IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera la cantidad total de memoria física en el equipo host, en megabytes.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Propiedad de memoria virtual PC
- Propiedad de memoria virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad de memoria
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f634bfe3bf81dcb13c9f09d8f19a5a82aa6902
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696018"
---
# <a name="ivmhostinfomemory-property"></a><span data-ttu-id="aef01-106">IVMHostInfo:: Memory (propiedad)</span><span class="sxs-lookup"><span data-stu-id="aef01-106">IVMHostInfo::Memory property</span></span>

<span data-ttu-id="aef01-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aef01-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aef01-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aef01-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aef01-109">Recupera la cantidad total de memoria física en el equipo host, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="aef01-109">Retrieves the total amount of physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="aef01-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aef01-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef01-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aef01-111">Syntax</span></span>


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="aef01-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="aef01-112">Property value</span></span>

<span data-ttu-id="aef01-113">Cantidad total de memoria física, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="aef01-113">The total amount of physical memory, in megabytes.</span></span> <span data-ttu-id="aef01-114">Este valor es una **variante** de tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="aef01-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aef01-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="aef01-115">Error codes</span></span>



| <span data-ttu-id="aef01-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="aef01-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="aef01-117">Significado</span><span class="sxs-lookup"><span data-stu-id="aef01-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="aef01-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aef01-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="aef01-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="aef01-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="aef01-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="aef01-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="aef01-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="aef01-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="aef01-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aef01-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="aef01-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="aef01-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="aef01-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aef01-124">Requirements</span></span>



| <span data-ttu-id="aef01-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef01-125">Requirement</span></span> | <span data-ttu-id="aef01-126">Value</span><span class="sxs-lookup"><span data-stu-id="aef01-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef01-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aef01-127">Minimum supported client</span></span><br/> | <span data-ttu-id="aef01-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="aef01-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aef01-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aef01-129">Minimum supported server</span></span><br/> | <span data-ttu-id="aef01-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aef01-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aef01-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="aef01-131">End of client support</span></span><br/>    | <span data-ttu-id="aef01-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aef01-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aef01-133">Producto</span><span class="sxs-lookup"><span data-stu-id="aef01-133">Product</span></span><br/>                  | <span data-ttu-id="aef01-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aef01-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aef01-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aef01-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="aef01-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="aef01-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aef01-137">IID</span><span class="sxs-lookup"><span data-stu-id="aef01-137">IID</span></span><br/>                      | <span data-ttu-id="aef01-138">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="aef01-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="aef01-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="aef01-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef01-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="aef01-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

