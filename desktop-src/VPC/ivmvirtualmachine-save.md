---
title: Método Save de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Guarda el estado de la máquina virtual (VM).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Guardar método virtual PC
- Método Save Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803313"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="419fe-106">IVMVirtualMachine:: Save (método)</span><span class="sxs-lookup"><span data-stu-id="419fe-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="419fe-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="419fe-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="419fe-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="419fe-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="419fe-109">Guarda el estado de la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="419fe-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="419fe-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="419fe-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="419fe-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="419fe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419fe-112">*saveTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="419fe-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="419fe-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento del progreso de finalización de la secuencia de almacenamiento de estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="419fe-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419fe-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="419fe-114">Return value</span></span>

<span data-ttu-id="419fe-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="419fe-115">This method can return one of these values.</span></span>



| <span data-ttu-id="419fe-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="419fe-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="419fe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="419fe-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="419fe-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="419fe-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="419fe-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="419fe-120"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="419fe-121">No se pudo guardar la máquina virtual porque los discos para deshacer se marcaron para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="419fe-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="419fe-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="419fe-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="419fe-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="419fe-124"><dt>**HRESULT \_ DE \_ Win32 (error de \_ acceso \_ denegado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="419fe-125">El autor de la llamada debe tener permisos de acceso de ejecución para guardar el estado de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="419fe-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="419fe-126"><dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="419fe-127">La máquina virtual no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="419fe-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="419fe-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="419fe-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="419fe-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="419fe-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="419fe-130">Remarks</span></span>

<span data-ttu-id="419fe-131">La máquina virtual se apaga cuando la tarea **Guardar** llega a su finalización.</span><span class="sxs-lookup"><span data-stu-id="419fe-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="419fe-132">La propiedad [**IVMVirtualMachine:: State**](ivmvirtualmachine-state.md) contendrá **vmVMState \_** al guardar mientras está en curso, seguido de **vmVMState \_ guardada** cuando se haya completado el proceso de guardado y se haya desactivado la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="419fe-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="419fe-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="419fe-133">Requirements</span></span>



| <span data-ttu-id="419fe-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="419fe-134">Requirement</span></span> | <span data-ttu-id="419fe-135">Value</span><span class="sxs-lookup"><span data-stu-id="419fe-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="419fe-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="419fe-136">Minimum supported client</span></span><br/> | <span data-ttu-id="419fe-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="419fe-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="419fe-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="419fe-138">Minimum supported server</span></span><br/> | <span data-ttu-id="419fe-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="419fe-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="419fe-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="419fe-140">End of client support</span></span><br/>    | <span data-ttu-id="419fe-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="419fe-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="419fe-142">Producto</span><span class="sxs-lookup"><span data-stu-id="419fe-142">Product</span></span><br/>                  | <span data-ttu-id="419fe-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="419fe-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="419fe-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="419fe-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="419fe-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="419fe-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="419fe-146">IID</span><span class="sxs-lookup"><span data-stu-id="419fe-146">IID</span></span><br/>                      | <span data-ttu-id="419fe-147">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="419fe-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="419fe-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="419fe-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419fe-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="419fe-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

