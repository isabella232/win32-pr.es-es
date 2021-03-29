---
title: Método IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Anula el registro de una configuración de máquina virtual sin eliminar el archivo de configuración.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Método UnregisterVirtualMachine Virtual PC
- Método UnregisterVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método UnregisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492886"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="f31ee-106">IVMVirtualPC:: UnregisterVirtualMachine (método)</span><span class="sxs-lookup"><span data-stu-id="f31ee-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="f31ee-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f31ee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f31ee-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f31ee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f31ee-109">Anula el registro de una configuración de máquina virtual (VM) sin eliminar el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="f31ee-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31ee-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f31ee-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="f31ee-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f31ee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31ee-112">*virtualMachine* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f31ee-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31ee-113">Un puntero a un objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa la configuración de la máquina virtual cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="f31ee-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f31ee-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f31ee-114">Return value</span></span>

<span data-ttu-id="f31ee-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f31ee-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f31ee-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f31ee-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="f31ee-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f31ee-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f31ee-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f31ee-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f31ee-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f31ee-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f31ee-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f31ee-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f31ee-121">El parámetro *virtualMachine* era **null**.</span><span class="sxs-lookup"><span data-stu-id="f31ee-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f31ee-122"><dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="f31ee-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="f31ee-123">La máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f31ee-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="f31ee-124"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f31ee-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f31ee-125">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="f31ee-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="f31ee-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f31ee-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="f31ee-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f31ee-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="f31ee-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f31ee-128">Remarks</span></span>

<span data-ttu-id="f31ee-129">Solo se puede anular el registro de las máquinas virtuales detenidas.</span><span class="sxs-lookup"><span data-stu-id="f31ee-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="f31ee-130">Los datos del estado guardado o de la unidad de deshacer existentes para esta configuración se conservarán cuando se anule el registro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f31ee-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31ee-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f31ee-131">Requirements</span></span>



| <span data-ttu-id="f31ee-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f31ee-132">Requirement</span></span> | <span data-ttu-id="f31ee-133">Value</span><span class="sxs-lookup"><span data-stu-id="f31ee-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31ee-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f31ee-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f31ee-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f31ee-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f31ee-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f31ee-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f31ee-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f31ee-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f31ee-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f31ee-138">End of client support</span></span><br/>    | <span data-ttu-id="f31ee-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f31ee-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f31ee-140">Producto</span><span class="sxs-lookup"><span data-stu-id="f31ee-140">Product</span></span><br/>                  | <span data-ttu-id="f31ee-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f31ee-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f31ee-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f31ee-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f31ee-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f31ee-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f31ee-144">IID</span><span class="sxs-lookup"><span data-stu-id="f31ee-144">IID</span></span><br/>                      | <span data-ttu-id="f31ee-145">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f31ee-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f31ee-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f31ee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31ee-147">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f31ee-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

