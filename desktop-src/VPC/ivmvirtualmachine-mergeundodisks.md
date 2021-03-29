---
title: Método IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Combina los discos para deshacer virtuales.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Método MergeUndoDisks Virtual PC
- Método MergeUndoDisks Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359811"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="ce537-106">IVMVirtualMachine:: MergeUndoDisks (método)</span><span class="sxs-lookup"><span data-stu-id="ce537-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="ce537-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce537-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce537-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ce537-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce537-109">Combina los discos para deshacer virtuales.</span><span class="sxs-lookup"><span data-stu-id="ce537-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce537-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce537-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="ce537-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce537-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce537-112">*undoMergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ce537-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ce537-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la creación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ce537-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce537-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce537-114">Return value</span></span>

<span data-ttu-id="ce537-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ce537-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ce537-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce537-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="ce537-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce537-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce537-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="ce537-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce537-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="ce537-120"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="ce537-121">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ce537-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="ce537-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="ce537-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ce537-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="ce537-124"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="ce537-125">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *convertedDiskImagePath* o uno de los discos primarios no es válido.</span><span class="sxs-lookup"><span data-stu-id="ce537-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ce537-126"><dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="ce537-127">El usuario actual no tiene acceso suficiente al archivo primario.</span><span class="sxs-lookup"><span data-stu-id="ce537-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="ce537-128"><dt>**E \_ ADMINISTRAR**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="ce537-129">Uno de los discos primarios está en uso.</span><span class="sxs-lookup"><span data-stu-id="ce537-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="ce537-130"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ce537-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="ce537-131">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="ce537-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="ce537-132"><dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="ce537-133">La máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ce537-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="ce537-134"><dt>**Máquina virtual \_ E & 0xA004067A de \_ \_ \_ solo lectura de archivos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ce537-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="ce537-135">El elemento primario de los discos para deshacer virtual está marcado como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ce537-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="ce537-136"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="ce537-137">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ce537-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ce537-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce537-138">Remarks</span></span>

<span data-ttu-id="ce537-139">No se puede llamar a **MergeUndoDisks** mientras la máquina virtual sigue en ejecución.</span><span class="sxs-lookup"><span data-stu-id="ce537-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="ce537-140">Use [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md) para guardar el estado de la máquina virtual antes de llamar a **MergeUndoDisks** o [**IVMVirtualMachine::**](ivmvirtualmachine-turnoff.md) desactivador para desactivar la máquina virtual sin guardar su estado actual de antemano.</span><span class="sxs-lookup"><span data-stu-id="ce537-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce537-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce537-141">Requirements</span></span>



| <span data-ttu-id="ce537-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce537-142">Requirement</span></span> | <span data-ttu-id="ce537-143">Value</span><span class="sxs-lookup"><span data-stu-id="ce537-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce537-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce537-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ce537-145">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce537-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce537-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce537-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ce537-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce537-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce537-148">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ce537-148">End of client support</span></span><br/>    | <span data-ttu-id="ce537-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce537-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce537-150">Producto</span><span class="sxs-lookup"><span data-stu-id="ce537-150">Product</span></span><br/>                  | <span data-ttu-id="ce537-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce537-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce537-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce537-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce537-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce537-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ce537-154">IID</span><span class="sxs-lookup"><span data-stu-id="ce537-154">IID</span></span><br/>                      | <span data-ttu-id="ce537-155">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ce537-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ce537-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce537-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce537-157">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ce537-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

