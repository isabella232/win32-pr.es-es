---
title: Método IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces. h)
description: Establece la ubicación del bus al que está conectado este disco duro.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Método SetBusLocation Virtual PC
- Método SetBusLocation Virtual PC, interfaz IVMHardDiskConnection
- Interfaz IVMHardDiskConnection Virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359665"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="7804f-106">IVMHardDiskConnection:: SetBusLocation (método)</span><span class="sxs-lookup"><span data-stu-id="7804f-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="7804f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7804f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7804f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7804f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7804f-109">Establece la ubicación del bus al que está conectado este disco duro.</span><span class="sxs-lookup"><span data-stu-id="7804f-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="7804f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7804f-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="7804f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7804f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7804f-112">*vmBusNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7804f-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7804f-113">Número de bus que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7804f-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="7804f-114">*vmDeviceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7804f-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7804f-115">Número de dispositivo que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7804f-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7804f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7804f-116">Return value</span></span>

<span data-ttu-id="7804f-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7804f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="7804f-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7804f-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="7804f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7804f-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7804f-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7804f-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="7804f-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7804f-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="7804f-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="7804f-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="7804f-123">La ubicación de bus especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="7804f-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="7804f-124"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="7804f-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="7804f-125">No se pudo establecer la ubicación del bus porque la máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="7804f-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="7804f-126"><dt>**Máquina virtual \_ E \_ unidad \_ \_ de bus \_ de disco en \_ uso**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="7804f-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="7804f-127">No se pudo establecer la ubicación del bus porque otro dispositivo está conectado actualmente a esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="7804f-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="7804f-128"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7804f-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="7804f-129">La unidad actual no es válida.</span><span class="sxs-lookup"><span data-stu-id="7804f-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="7804f-130"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7804f-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="7804f-131">La máquina virtual actual no es válida.</span><span class="sxs-lookup"><span data-stu-id="7804f-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="7804f-132"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7804f-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="7804f-133">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="7804f-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="7804f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7804f-134">Requirements</span></span>



| <span data-ttu-id="7804f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7804f-135">Requirement</span></span> | <span data-ttu-id="7804f-136">Value</span><span class="sxs-lookup"><span data-stu-id="7804f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7804f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7804f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7804f-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7804f-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7804f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7804f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7804f-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7804f-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7804f-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7804f-141">End of client support</span></span><br/>    | <span data-ttu-id="7804f-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7804f-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7804f-143">Producto</span><span class="sxs-lookup"><span data-stu-id="7804f-143">Product</span></span><br/>                  | <span data-ttu-id="7804f-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7804f-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7804f-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7804f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7804f-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7804f-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7804f-147">IID</span><span class="sxs-lookup"><span data-stu-id="7804f-147">IID</span></span><br/>                      | <span data-ttu-id="7804f-148">IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="7804f-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="7804f-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="7804f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7804f-150">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="7804f-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

