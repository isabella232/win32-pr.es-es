---
title: Propiedad IVMHostInfo MemoryAvail (VPCCOMInterfaces. h)
description: Recupera la cantidad de memoria física disponible en el equipo host, en megabytes.
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- Propiedad MemoryAvail Virtual PC
- Propiedad MemoryAvail Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad MemoryAvail
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df6be8bf62595720d01372ee891184952a0dd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676905"
---
# <a name="ivmhostinfomemoryavail-property"></a><span data-ttu-id="820d9-106">IVMHostInfo:: MemoryAvail (propiedad)</span><span class="sxs-lookup"><span data-stu-id="820d9-106">IVMHostInfo::MemoryAvail property</span></span>

<span data-ttu-id="820d9-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="820d9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="820d9-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="820d9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="820d9-109">Recupera la cantidad de memoria física disponible en el equipo host, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="820d9-109">Retrieves the amount of available physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="820d9-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="820d9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="820d9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="820d9-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="820d9-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="820d9-112">Property value</span></span>

<span data-ttu-id="820d9-113">La memoria física disponible, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="820d9-113">The available physical memory, in megabytes.</span></span> <span data-ttu-id="820d9-114">Este valor es una **variante** de tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="820d9-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="820d9-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="820d9-115">Error codes</span></span>



| <span data-ttu-id="820d9-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="820d9-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="820d9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="820d9-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="820d9-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="820d9-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="820d9-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="820d9-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="820d9-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="820d9-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="820d9-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="820d9-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="820d9-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="820d9-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="820d9-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="820d9-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="820d9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="820d9-124">Requirements</span></span>



| <span data-ttu-id="820d9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="820d9-125">Requirement</span></span> | <span data-ttu-id="820d9-126">Value</span><span class="sxs-lookup"><span data-stu-id="820d9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="820d9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="820d9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="820d9-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="820d9-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="820d9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="820d9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="820d9-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="820d9-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="820d9-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="820d9-131">End of client support</span></span><br/>    | <span data-ttu-id="820d9-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="820d9-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="820d9-133">Producto</span><span class="sxs-lookup"><span data-stu-id="820d9-133">Product</span></span><br/>                  | <span data-ttu-id="820d9-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="820d9-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="820d9-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="820d9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="820d9-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="820d9-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="820d9-137">IID</span><span class="sxs-lookup"><span data-stu-id="820d9-137">IID</span></span><br/>                      | <span data-ttu-id="820d9-138">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="820d9-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="820d9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="820d9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820d9-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="820d9-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

