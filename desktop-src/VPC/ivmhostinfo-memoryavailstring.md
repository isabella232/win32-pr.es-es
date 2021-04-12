---
title: Propiedad IVMHostInfo MemoryAvailString (VPCCOMInterfaces. h)
description: Recupera la cantidad de memoria física disponible en el equipo host, en megabytes, como una cadena.
ms.assetid: a0f17dda-2042-4aec-9968-6662d32684cf
keywords:
- Propiedad MemoryAvailString Virtual PC
- Propiedad MemoryAvailString Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad MemoryAvailString
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvailString
- IVMHostInfo.get_MemoryAvailString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea003b94d0d4604dfba3daf545a51b9d69b6708c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491308"
---
# <a name="ivmhostinfomemoryavailstring-property"></a><span data-ttu-id="95b84-106">IVMHostInfo:: MemoryAvailString (propiedad)</span><span class="sxs-lookup"><span data-stu-id="95b84-106">IVMHostInfo::MemoryAvailString property</span></span>

<span data-ttu-id="95b84-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="95b84-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="95b84-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="95b84-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="95b84-109">Recupera la cantidad de memoria física disponible en el equipo host, en megabytes, como una cadena.</span><span class="sxs-lookup"><span data-stu-id="95b84-109">Retrieves the amount of available physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="95b84-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="95b84-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b84-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95b84-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvailString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="95b84-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="95b84-112">Property value</span></span>

<span data-ttu-id="95b84-113">La memoria física disponible, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="95b84-113">The available physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="95b84-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="95b84-114">Error codes</span></span>



| <span data-ttu-id="95b84-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="95b84-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="95b84-116">Significado</span><span class="sxs-lookup"><span data-stu-id="95b84-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="95b84-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="95b84-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="95b84-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="95b84-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="95b84-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="95b84-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="95b84-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="95b84-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="95b84-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="95b84-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="95b84-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="95b84-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="95b84-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95b84-123">Requirements</span></span>



| <span data-ttu-id="95b84-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b84-124">Requirement</span></span> | <span data-ttu-id="95b84-125">Value</span><span class="sxs-lookup"><span data-stu-id="95b84-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b84-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95b84-126">Minimum supported client</span></span><br/> | <span data-ttu-id="95b84-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="95b84-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95b84-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95b84-128">Minimum supported server</span></span><br/> | <span data-ttu-id="95b84-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="95b84-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="95b84-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="95b84-130">End of client support</span></span><br/>    | <span data-ttu-id="95b84-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95b84-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="95b84-132">Producto</span><span class="sxs-lookup"><span data-stu-id="95b84-132">Product</span></span><br/>                  | <span data-ttu-id="95b84-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="95b84-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="95b84-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95b84-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b84-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b84-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="95b84-136">IID</span><span class="sxs-lookup"><span data-stu-id="95b84-136">IID</span></span><br/>                      | <span data-ttu-id="95b84-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="95b84-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="95b84-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="95b84-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b84-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="95b84-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

