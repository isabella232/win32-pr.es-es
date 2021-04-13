---
title: Método IVMVirtualMachine Startup2 (VPCCOMInterfaces. h)
description: Inicia la máquina virtual desde el estado no inicializado o guardado, con opciones avanzadas.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Método Startup2 Virtual PC
- Método Startup2 Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método Startup2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422354"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="89f55-106">IVMVirtualMachine:: Startup2 (método)</span><span class="sxs-lookup"><span data-stu-id="89f55-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="89f55-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89f55-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89f55-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89f55-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89f55-109">Inicia la máquina virtual (VM) desde el estado no inicializado o guardado, con opciones avanzadas.</span><span class="sxs-lookup"><span data-stu-id="89f55-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="89f55-110">Este método proporciona un mecanismo para iniciar una máquina virtual con un disco de diferenciación incluso si se ha cambiado la marca de tiempo del disco principal.</span><span class="sxs-lookup"><span data-stu-id="89f55-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f55-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89f55-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="89f55-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89f55-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f55-113">*startupOption* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89f55-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f55-114">Opción de inicio avanzada.</span><span class="sxs-lookup"><span data-stu-id="89f55-114">The advanced startup option.</span></span> <span data-ttu-id="89f55-115">Los valores posibles proceden de la enumeración [**VMStartupOption**](vmstartupoption.md) .</span><span class="sxs-lookup"><span data-stu-id="89f55-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="89f55-116">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="89f55-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="89f55-117">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de inicio.</span><span class="sxs-lookup"><span data-stu-id="89f55-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f55-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89f55-118">Return value</span></span>

<span data-ttu-id="89f55-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="89f55-119">This method can return one of these values.</span></span>



| <span data-ttu-id="89f55-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89f55-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="89f55-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="89f55-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89f55-122"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="89f55-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="89f55-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="89f55-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="89f55-125">El parámetro *startupOption* no es válido.</span><span class="sxs-lookup"><span data-stu-id="89f55-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="89f55-126"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="89f55-127">El parámetro *startupTask* es **null**.</span><span class="sxs-lookup"><span data-stu-id="89f55-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="89f55-128"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="89f55-129">El autor de la llamada debe tener permisos de acceso de ejecución para iniciar esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="89f55-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="89f55-130"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="89f55-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="89f55-131">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="89f55-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="89f55-132"><dt>**Máquina virtual \_ E \_ fuera \_ del \_ recurso**</dt> <dt>0xA0040203</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="89f55-133">No hay suficientes recursos de host.</span><span class="sxs-lookup"><span data-stu-id="89f55-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="89f55-134"><dt>**Máquina virtual \_ E \_ demasiadas \_ \_ máquinas virtuales**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="89f55-135">Hay demasiadas máquinas virtuales activas.</span><span class="sxs-lookup"><span data-stu-id="89f55-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="89f55-136"><dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="89f55-137">La máquina virtual ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="89f55-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="89f55-138"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="89f55-139">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="89f55-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="89f55-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89f55-140">Remarks</span></span>

<span data-ttu-id="89f55-141">Los valores siguientes se pueden devolver a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto.</span><span class="sxs-lookup"><span data-stu-id="89f55-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="89f55-142">Código de [**error**](ivmtask-error.md) /valor</span><span class="sxs-lookup"><span data-stu-id="89f55-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="89f55-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="89f55-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="89f55-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="89f55-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="89f55-145">El hardware no admite la virtualización.</span><span class="sxs-lookup"><span data-stu-id="89f55-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="89f55-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="89f55-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="89f55-147">La virtualización de hardware está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="89f55-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="89f55-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="89f55-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="89f55-149">Tanto Virtual PC 2007 como Windows Virtual PC están instalados.</span><span class="sxs-lookup"><span data-stu-id="89f55-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="89f55-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="89f55-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="89f55-151">Se instala otro software de virtualización.</span><span class="sxs-lookup"><span data-stu-id="89f55-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="89f55-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="89f55-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="89f55-153">No hay suficientes recursos de host.</span><span class="sxs-lookup"><span data-stu-id="89f55-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="89f55-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f55-154">Requirements</span></span>



| <span data-ttu-id="89f55-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f55-155">Requirement</span></span> | <span data-ttu-id="89f55-156">Value</span><span class="sxs-lookup"><span data-stu-id="89f55-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f55-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89f55-157">Minimum supported client</span></span><br/> | <span data-ttu-id="89f55-158">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="89f55-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89f55-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89f55-159">Minimum supported server</span></span><br/> | <span data-ttu-id="89f55-160">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="89f55-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="89f55-161">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="89f55-161">End of client support</span></span><br/>    | <span data-ttu-id="89f55-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89f55-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="89f55-163">Producto</span><span class="sxs-lookup"><span data-stu-id="89f55-163">Product</span></span><br/>                  | <span data-ttu-id="89f55-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89f55-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="89f55-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89f55-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="89f55-166"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="89f55-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="89f55-167">IID</span><span class="sxs-lookup"><span data-stu-id="89f55-167">IID</span></span><br/>                      | <span data-ttu-id="89f55-168">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="89f55-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="89f55-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="89f55-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f55-170">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="89f55-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

