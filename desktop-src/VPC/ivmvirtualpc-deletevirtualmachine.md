---
title: Método IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Elimina una configuración de máquina virtual.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Método DeleteVirtualMachine Virtual PC
- Método DeleteVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695998"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="e6947-106">IVMVirtualPC::D método eleteVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e6947-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="e6947-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6947-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6947-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6947-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6947-109">Elimina una configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6947-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6947-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6947-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="e6947-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6947-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6947-112">*virtualMachine* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6947-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6947-113">Un puntero a un objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa la configuración de la máquina virtual que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="e6947-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6947-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6947-114">Return value</span></span>

<span data-ttu-id="e6947-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e6947-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e6947-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6947-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e6947-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6947-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6947-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e6947-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6947-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e6947-120"><dt>**S \_ FALSO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="e6947-121">No se encontró la configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="e6947-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e6947-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e6947-123">El parámetro *virtualMachine* era **null**.</span><span class="sxs-lookup"><span data-stu-id="e6947-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="e6947-124"><dt>**Máquina virtual \_ \_Máquina virtual \_ que ejecuta**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="e6947-125">La máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e6947-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="e6947-126"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e6947-127">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="e6947-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="e6947-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e6947-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e6947-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e6947-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6947-130">Remarks</span></span>

<span data-ttu-id="e6947-131">Solo se pueden eliminar las máquinas virtuales detenidas.</span><span class="sxs-lookup"><span data-stu-id="e6947-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="e6947-132">Tenga en cuenta que los datos del estado guardado o de la unidad de deshacer existentes para esta configuración se eliminarán además del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="e6947-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6947-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6947-133">Requirements</span></span>



| <span data-ttu-id="e6947-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6947-134">Requirement</span></span> | <span data-ttu-id="e6947-135">Value</span><span class="sxs-lookup"><span data-stu-id="e6947-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6947-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6947-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e6947-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6947-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6947-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6947-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e6947-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e6947-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6947-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e6947-140">End of client support</span></span><br/>    | <span data-ttu-id="e6947-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6947-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6947-142">Producto</span><span class="sxs-lookup"><span data-stu-id="e6947-142">Product</span></span><br/>                  | <span data-ttu-id="e6947-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6947-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6947-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6947-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6947-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6947-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6947-146">IID</span><span class="sxs-lookup"><span data-stu-id="e6947-146">IID</span></span><br/>                      | <span data-ttu-id="e6947-147">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e6947-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e6947-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6947-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6947-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e6947-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

