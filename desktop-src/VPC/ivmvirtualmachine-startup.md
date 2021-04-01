---
title: Método de inicio IVMVirtualMachine (VPCCOMInterfaces. h)
description: Inicia la máquina virtual desde el estado no inicializado o guardado.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Método de inicio Virtual PC
- Método de inicio Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método de inicio
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996879"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="0e91c-106">IVMVirtualMachine:: Startup (método)</span><span class="sxs-lookup"><span data-stu-id="0e91c-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="0e91c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0e91c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0e91c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0e91c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0e91c-109">Inicia la máquina virtual desde el estado no inicializado o guardado.</span><span class="sxs-lookup"><span data-stu-id="0e91c-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e91c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e91c-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="0e91c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e91c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e91c-112">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0e91c-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0e91c-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de la ejecución de la secuencia de inicio de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e91c-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e91c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e91c-114">Return value</span></span>

<span data-ttu-id="0e91c-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0e91c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="0e91c-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e91c-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="0e91c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e91c-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e91c-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="0e91c-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0e91c-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0e91c-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="0e91c-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="0e91c-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="0e91c-122"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="0e91c-123">El autor de la llamada debe tener permisos de acceso de ejecución para iniciar esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e91c-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="0e91c-124"><dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="0e91c-125">La operación no se completó de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="0e91c-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="0e91c-126"><dt>**Máquina virtual \_ E \_ fuera \_ del \_ recurso**</dt> <dt>0xA0040203</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="0e91c-127">No hay suficientes recursos de host.</span><span class="sxs-lookup"><span data-stu-id="0e91c-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="0e91c-128"><dt>**Máquina virtual \_ E \_ demasiadas \_ \_ máquinas virtuales**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="0e91c-129">Hay demasiadas máquinas virtuales activas.</span><span class="sxs-lookup"><span data-stu-id="0e91c-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0e91c-130"><dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="0e91c-131">La máquina virtual ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0e91c-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="0e91c-132"><dt>**Máquina virtual \_ E \_ primario \_ modificado**</dt> <dt>0xA00400687</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="0e91c-133">No se puede iniciar la máquina virtual porque se ha modificado el VHD primario.</span><span class="sxs-lookup"><span data-stu-id="0e91c-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="0e91c-134"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="0e91c-135">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0e91c-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="0e91c-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e91c-136">Remarks</span></span>

<span data-ttu-id="0e91c-137">Si la máquina virtual está guardada, se restaurará desde el estado guardado.</span><span class="sxs-lookup"><span data-stu-id="0e91c-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="0e91c-138">Los valores siguientes se pueden devolver a través de la propiedad [**error**](ivmtask-error.md) del objeto [**IVMTask**](ivmtask.md) devuelto.</span><span class="sxs-lookup"><span data-stu-id="0e91c-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="0e91c-139">Código de [**error**](ivmtask-error.md) /valor</span><span class="sxs-lookup"><span data-stu-id="0e91c-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="0e91c-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e91c-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0e91c-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="0e91c-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="0e91c-142">El hardware no admite la virtualización.</span><span class="sxs-lookup"><span data-stu-id="0e91c-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="0e91c-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="0e91c-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="0e91c-144">La virtualización de hardware está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="0e91c-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="0e91c-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="0e91c-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="0e91c-146">Tanto Virtual PC 2007 como Windows Virtual PC están instalados.</span><span class="sxs-lookup"><span data-stu-id="0e91c-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="0e91c-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="0e91c-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="0e91c-148">Se instala otro software de virtualización.</span><span class="sxs-lookup"><span data-stu-id="0e91c-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="0e91c-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="0e91c-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="0e91c-150">No hay suficientes recursos de host.</span><span class="sxs-lookup"><span data-stu-id="0e91c-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="0e91c-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e91c-151">Requirements</span></span>



| <span data-ttu-id="0e91c-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e91c-152">Requirement</span></span> | <span data-ttu-id="0e91c-153">Value</span><span class="sxs-lookup"><span data-stu-id="0e91c-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e91c-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e91c-154">Minimum supported client</span></span><br/> | <span data-ttu-id="0e91c-155">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e91c-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e91c-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e91c-156">Minimum supported server</span></span><br/> | <span data-ttu-id="0e91c-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0e91c-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0e91c-158">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0e91c-158">End of client support</span></span><br/>    | <span data-ttu-id="0e91c-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e91c-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0e91c-160">Producto</span><span class="sxs-lookup"><span data-stu-id="0e91c-160">Product</span></span><br/>                  | <span data-ttu-id="0e91c-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0e91c-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0e91c-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e91c-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e91c-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e91c-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0e91c-164">IID</span><span class="sxs-lookup"><span data-stu-id="0e91c-164">IID</span></span><br/>                      | <span data-ttu-id="0e91c-165">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0e91c-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0e91c-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e91c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e91c-167">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="0e91c-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

