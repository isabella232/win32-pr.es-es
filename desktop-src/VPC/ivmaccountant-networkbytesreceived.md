---
title: Propiedad IVMAccountant NetworkBytesReceived (VPCCOMInterfaces. h)
description: Número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- Propiedad NetworkBytesReceived Virtual PC
- Propiedad NetworkBytesReceived Virtual PC, interfaz IVMAccountant
- Interfaz IVMAccountant Virtual PC, propiedad NetworkBytesReceived
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e14d7454516ff4e83771744c74f31ee594aa67f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492905"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a><span data-ttu-id="4c8ae-106">IVMAccountant:: NetworkBytesReceived (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4c8ae-106">IVMAccountant::NetworkBytesReceived property</span></span>

<span data-ttu-id="4c8ae-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c8ae-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c8ae-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c8ae-109">Recupera el número total de bytes recibidos por todos los adaptadores de red virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-109">Retrieves the total number of bytes received by all virtual network adapters for this virtual machine.</span></span>

<span data-ttu-id="4c8ae-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8ae-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c8ae-111">Syntax</span></span>


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a><span data-ttu-id="4c8ae-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4c8ae-112">Property value</span></span>

<span data-ttu-id="4c8ae-113">Número total de bytes recibidos.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-113">The total number of bytes received.</span></span> <span data-ttu-id="4c8ae-114">Estos datos se devuelven como una **variante** de tipo **VT \_ decimal**.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c8ae-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4c8ae-115">Error codes</span></span>



| <span data-ttu-id="4c8ae-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="4c8ae-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4c8ae-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4c8ae-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4c8ae-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ae-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4c8ae-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="4c8ae-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ae-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4c8ae-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="4c8ae-122"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ae-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="4c8ae-123">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="4c8ae-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ae-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4c8ae-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="4c8ae-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c8ae-126">Remarks</span></span>

<span data-ttu-id="4c8ae-127">Tenga en cuenta que las estadísticas de e/s de red se restablecen a cero cuando una máquina virtual se enciende, se restablece o se restaura desde el estado guardado.</span><span class="sxs-lookup"><span data-stu-id="4c8ae-127">Note that network I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8ae-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c8ae-128">Requirements</span></span>



| <span data-ttu-id="4c8ae-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8ae-129">Requirement</span></span> | <span data-ttu-id="4c8ae-130">Value</span><span class="sxs-lookup"><span data-stu-id="4c8ae-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8ae-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c8ae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c8ae-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c8ae-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c8ae-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c8ae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c8ae-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4c8ae-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c8ae-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4c8ae-135">End of client support</span></span><br/>    | <span data-ttu-id="4c8ae-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c8ae-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c8ae-137">Producto</span><span class="sxs-lookup"><span data-stu-id="4c8ae-137">Product</span></span><br/>                  | <span data-ttu-id="4c8ae-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c8ae-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c8ae-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c8ae-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c8ae-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ae-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c8ae-141">IID</span><span class="sxs-lookup"><span data-stu-id="4c8ae-141">IID</span></span><br/>                      | <span data-ttu-id="4c8ae-142">IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="4c8ae-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4c8ae-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c8ae-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8ae-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="4c8ae-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

