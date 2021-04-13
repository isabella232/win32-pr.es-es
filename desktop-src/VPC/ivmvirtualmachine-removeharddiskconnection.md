---
title: Método IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
description: Quita la conexión de disco duro especificada de la máquina virtual.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Método RemoveHardDiskConnection Virtual PC
- Método RemoveHardDiskConnection Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422355"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a><span data-ttu-id="fba79-106">IVMVirtualMachine:: RemoveHardDiskConnection (método)</span><span class="sxs-lookup"><span data-stu-id="fba79-106">IVMVirtualMachine::RemoveHardDiskConnection method</span></span>

<span data-ttu-id="fba79-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fba79-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fba79-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fba79-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fba79-109">Quita la conexión de disco duro especificada de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fba79-109">Removes the specified hard disk connection from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba79-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fba79-110">Syntax</span></span>


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="fba79-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fba79-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba79-112">*hardDiskConnection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba79-112">*hardDiskConnection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba79-113">Un objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) que representa la conexión del disco duro que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="fba79-113">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object that represents the hard disk connection to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba79-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba79-114">Return value</span></span>

<span data-ttu-id="fba79-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fba79-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fba79-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba79-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="fba79-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fba79-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="fba79-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fba79-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="fba79-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fba79-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="fba79-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fba79-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="fba79-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="fba79-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fba79-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fba79-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="fba79-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="fba79-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="fba79-124"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="fba79-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="fba79-125">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="fba79-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="fba79-126"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fba79-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="fba79-127">La unidad especificada no está conectada a esta ubicación de bus.</span><span class="sxs-lookup"><span data-stu-id="fba79-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="fba79-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fba79-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="fba79-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="fba79-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="fba79-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fba79-130">Remarks</span></span>

<span data-ttu-id="fba79-131">Solo puede quitar una conexión de disco duro existente de una máquina virtual detenida.</span><span class="sxs-lookup"><span data-stu-id="fba79-131">You can only remove an existing hard disk connection from a stopped virtual machine.</span></span> <span data-ttu-id="fba79-132">Se obtiene una lista de las conexiones actualmente asociadas a la máquina virtual mediante la enumeración de la propiedad [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="fba79-132">A list of connections currently attached to the virtual machine is obtained by enumerating the [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba79-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba79-133">Requirements</span></span>



| <span data-ttu-id="fba79-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba79-134">Requirement</span></span> | <span data-ttu-id="fba79-135">Value</span><span class="sxs-lookup"><span data-stu-id="fba79-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba79-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba79-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fba79-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fba79-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fba79-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba79-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fba79-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fba79-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fba79-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fba79-140">End of client support</span></span><br/>    | <span data-ttu-id="fba79-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fba79-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fba79-142">Producto</span><span class="sxs-lookup"><span data-stu-id="fba79-142">Product</span></span><br/>                  | <span data-ttu-id="fba79-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fba79-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fba79-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fba79-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fba79-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba79-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fba79-146">IID</span><span class="sxs-lookup"><span data-stu-id="fba79-146">IID</span></span><br/>                      | <span data-ttu-id="fba79-147">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fba79-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fba79-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="fba79-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba79-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fba79-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

