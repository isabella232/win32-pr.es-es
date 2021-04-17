---
title: Propiedad de memoria IVMVirtualMachine (VPCCOMInterfaces. h)
description: Cantidad de memoria física en la máquina virtual, en megabytes.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propiedad de memoria virtual PC
- Propiedad de memoria virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad de memoria
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651382"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="fa87c-106">IVMVirtualMachine:: Memory (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fa87c-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="fa87c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fa87c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fa87c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fa87c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fa87c-109">Recupera y establece la cantidad de memoria física en la máquina virtual, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="fa87c-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="fa87c-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fa87c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa87c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa87c-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="fa87c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fa87c-112">Property value</span></span>

<span data-ttu-id="fa87c-113">Especifica la cantidad de memoria física, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="fa87c-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa87c-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fa87c-114">Error codes</span></span>



| <span data-ttu-id="fa87c-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="fa87c-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="fa87c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="fa87c-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="fa87c-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="fa87c-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa87c-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="fa87c-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="fa87c-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="fa87c-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="fa87c-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="fa87c-122">El parámetro no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="fa87c-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="fa87c-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="fa87c-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="fa87c-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="fa87c-125"><dt>Máquina virtual \_ E \_ Pref \_ not \_ found</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="fa87c-126">No se encontró la preferencia.</span><span class="sxs-lookup"><span data-stu-id="fa87c-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="fa87c-127"><dt>Máquina virtual \_ E \_ preft \_ VM \_ Active</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="fa87c-128">La máquina virtual está en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="fa87c-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="fa87c-129"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="fa87c-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="fa87c-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="fa87c-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa87c-131">Remarks</span></span>

<span data-ttu-id="fa87c-132">La cantidad de memoria física en una máquina virtual debe ser de al menos 4 MB.</span><span class="sxs-lookup"><span data-stu-id="fa87c-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="fa87c-133">El límite superior de la memoria depende de la configuración del host, pero puede tener como máximo 3.712 MB.</span><span class="sxs-lookup"><span data-stu-id="fa87c-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa87c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa87c-134">Requirements</span></span>



| <span data-ttu-id="fa87c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa87c-135">Requirement</span></span> | <span data-ttu-id="fa87c-136">Value</span><span class="sxs-lookup"><span data-stu-id="fa87c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa87c-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa87c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fa87c-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa87c-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa87c-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa87c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fa87c-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fa87c-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fa87c-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fa87c-141">End of client support</span></span><br/>    | <span data-ttu-id="fa87c-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa87c-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fa87c-143">Producto</span><span class="sxs-lookup"><span data-stu-id="fa87c-143">Product</span></span><br/>                  | <span data-ttu-id="fa87c-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fa87c-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fa87c-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa87c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa87c-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa87c-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fa87c-147">IID</span><span class="sxs-lookup"><span data-stu-id="fa87c-147">IID</span></span><br/>                      | <span data-ttu-id="fa87c-148">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fa87c-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fa87c-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa87c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa87c-150">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fa87c-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

