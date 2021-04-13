---
title: Propiedad IVMHostInfo MemoryTotalString (VPCCOMInterfaces. h)
description: Recupera la cantidad total de memoria física en el equipo host, en megabytes, como una cadena.
ms.assetid: 732c62e5-2776-4551-909f-7ddab74e067d
keywords:
- Propiedad MemoryTotalString Virtual PC
- Propiedad MemoryTotalString Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad MemoryTotalString
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryTotalString
- IVMHostInfo.get_MemoryTotalString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e6c16a4215aba141ff1803d340c63dc9faa868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422387"
---
# <a name="ivmhostinfomemorytotalstring-property"></a><span data-ttu-id="1c65e-106">IVMHostInfo:: MemoryTotalString (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1c65e-106">IVMHostInfo::MemoryTotalString property</span></span>

<span data-ttu-id="1c65e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1c65e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1c65e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1c65e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1c65e-109">Recupera la cantidad total de memoria física en el equipo host, en megabytes, como una cadena.</span><span class="sxs-lookup"><span data-stu-id="1c65e-109">Retrieves the total amount of physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="1c65e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1c65e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c65e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c65e-111">Syntax</span></span>


```C++
HRESULT get_MemoryTotalString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="1c65e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1c65e-112">Property value</span></span>

<span data-ttu-id="1c65e-113">Cantidad total de memoria física, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="1c65e-113">The total amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1c65e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1c65e-114">Error codes</span></span>



| <span data-ttu-id="1c65e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="1c65e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1c65e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1c65e-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1c65e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1c65e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1c65e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c65e-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="1c65e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1c65e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1c65e-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="1c65e-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="1c65e-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1c65e-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1c65e-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1c65e-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1c65e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c65e-123">Requirements</span></span>



| <span data-ttu-id="1c65e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c65e-124">Requirement</span></span> | <span data-ttu-id="1c65e-125">Value</span><span class="sxs-lookup"><span data-stu-id="1c65e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c65e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c65e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c65e-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c65e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c65e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c65e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c65e-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1c65e-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1c65e-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1c65e-130">End of client support</span></span><br/>    | <span data-ttu-id="1c65e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c65e-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1c65e-132">Producto</span><span class="sxs-lookup"><span data-stu-id="1c65e-132">Product</span></span><br/>                  | <span data-ttu-id="1c65e-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1c65e-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1c65e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c65e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c65e-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c65e-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1c65e-136">IID</span><span class="sxs-lookup"><span data-stu-id="1c65e-136">IID</span></span><br/>                      | <span data-ttu-id="1c65e-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="1c65e-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1c65e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c65e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c65e-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="1c65e-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

