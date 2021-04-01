---
title: Método IVMVirtualMachine RemoveDVDROMDrive (VPCCOMInterfaces. h)
description: Quita la unidad de CD o DVD especificada de la máquina virtual.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- Método RemoveDVDROMDrive Virtual PC
- Método RemoveDVDROMDrive Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150425"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="b8cec-106">IVMVirtualMachine:: RemoveDVDROMDrive (método)</span><span class="sxs-lookup"><span data-stu-id="b8cec-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="b8cec-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8cec-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8cec-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8cec-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8cec-109">Quita la unidad de CD o DVD especificada de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8cec-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cec-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8cec-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="b8cec-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8cec-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8cec-112">*dvdDrive* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8cec-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8cec-113">Unidad que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="b8cec-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8cec-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8cec-114">Return value</span></span>

<span data-ttu-id="b8cec-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b8cec-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b8cec-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8cec-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="b8cec-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8cec-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8cec-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="b8cec-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8cec-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="b8cec-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="b8cec-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b8cec-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b8cec-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="b8cec-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="b8cec-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="b8cec-124"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="b8cec-125">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="b8cec-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="b8cec-126"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="b8cec-127">La unidad especificada no está conectada a esta ubicación de bus.</span><span class="sxs-lookup"><span data-stu-id="b8cec-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="b8cec-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="b8cec-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b8cec-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="b8cec-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8cec-130">Remarks</span></span>

<span data-ttu-id="b8cec-131">Solo puede quitar una unidad de CD o DVD existente de una máquina virtual detenida.</span><span class="sxs-lookup"><span data-stu-id="b8cec-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cec-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8cec-132">Requirements</span></span>



| <span data-ttu-id="b8cec-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8cec-133">Requirement</span></span> | <span data-ttu-id="b8cec-134">Value</span><span class="sxs-lookup"><span data-stu-id="b8cec-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cec-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8cec-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cec-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8cec-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8cec-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8cec-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cec-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b8cec-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8cec-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b8cec-139">End of client support</span></span><br/>    | <span data-ttu-id="b8cec-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8cec-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8cec-141">Producto</span><span class="sxs-lookup"><span data-stu-id="b8cec-141">Product</span></span><br/>                  | <span data-ttu-id="b8cec-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8cec-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8cec-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8cec-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8cec-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8cec-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b8cec-145">IID</span><span class="sxs-lookup"><span data-stu-id="b8cec-145">IID</span></span><br/>                      | <span data-ttu-id="b8cec-146">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b8cec-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b8cec-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8cec-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cec-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b8cec-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

