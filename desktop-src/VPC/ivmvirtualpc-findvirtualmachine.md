---
title: Método IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Recupera un objeto de máquina virtual que coincide con la configuración solicitada.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Método FindVirtualMachine Virtual PC
- Método FindVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150793"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="056bd-106">IVMVirtualPC:: FindVirtualMachine (método)</span><span class="sxs-lookup"><span data-stu-id="056bd-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="056bd-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="056bd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="056bd-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="056bd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="056bd-109">Recupera un objeto de máquina virtual que coincide con la configuración solicitada.</span><span class="sxs-lookup"><span data-stu-id="056bd-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="056bd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="056bd-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="056bd-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="056bd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="056bd-112">*configurationName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="056bd-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="056bd-113">Nombre de la máquina virtual que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="056bd-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="056bd-114">*virtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="056bd-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="056bd-115">Un puntero a un nuevo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="056bd-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="056bd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="056bd-116">Return value</span></span>

<span data-ttu-id="056bd-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="056bd-117">This method can return one of these values.</span></span>



| <span data-ttu-id="056bd-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="056bd-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="056bd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="056bd-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="056bd-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="056bd-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="056bd-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="056bd-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="056bd-122"><dt>**S \_ FALSO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="056bd-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="056bd-123">No se encontró la configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="056bd-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="056bd-124"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="056bd-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="056bd-125">El parámetro *configurationName* no es válido o *virtualMachine* es **null**.</span><span class="sxs-lookup"><span data-stu-id="056bd-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="056bd-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="056bd-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="056bd-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="056bd-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="056bd-128"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="056bd-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="056bd-129">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="056bd-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="056bd-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="056bd-130">Remarks</span></span>

<span data-ttu-id="056bd-131">Los nombres de las máquinas virtuales no distinguen mayúsculas de minúsculas, por ejemplo, "MyVM" y "MyVM" hacen referencia a la misma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="056bd-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="056bd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056bd-132">Requirements</span></span>



| <span data-ttu-id="056bd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="056bd-133">Requirement</span></span> | <span data-ttu-id="056bd-134">Value</span><span class="sxs-lookup"><span data-stu-id="056bd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="056bd-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="056bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="056bd-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="056bd-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="056bd-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="056bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="056bd-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="056bd-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="056bd-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="056bd-139">End of client support</span></span><br/>    | <span data-ttu-id="056bd-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="056bd-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="056bd-141">Producto</span><span class="sxs-lookup"><span data-stu-id="056bd-141">Product</span></span><br/>                  | <span data-ttu-id="056bd-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="056bd-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="056bd-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="056bd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="056bd-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="056bd-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="056bd-145">IID</span><span class="sxs-lookup"><span data-stu-id="056bd-145">IID</span></span><br/>                      | <span data-ttu-id="056bd-146">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="056bd-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="056bd-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="056bd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056bd-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="056bd-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

