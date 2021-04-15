---
title: Método IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Agrega una nueva unidad de CD o DVD a la máquina virtual.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Método AddDVDROMDrive Virtual PC
- Método AddDVDROMDrive Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695954"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="edde0-106">IVMVirtualMachine:: AddDVDROMDrive (método)</span><span class="sxs-lookup"><span data-stu-id="edde0-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="edde0-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="edde0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="edde0-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="edde0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="edde0-109">Agrega una nueva unidad de CD o DVD a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="edde0-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="edde0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edde0-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="edde0-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edde0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edde0-112">*busNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edde0-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edde0-113">El bus al que se conectará la unidad.</span><span class="sxs-lookup"><span data-stu-id="edde0-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="edde0-114">Value</span><span class="sxs-lookup"><span data-stu-id="edde0-114">Value</span></span>                                                                        | <span data-ttu-id="edde0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="edde0-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="edde0-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="edde0-117">La unidad se conectará al primer bus.</span><span class="sxs-lookup"><span data-stu-id="edde0-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="edde0-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="edde0-119">La unidad se conectará al segundo bus.</span><span class="sxs-lookup"><span data-stu-id="edde0-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="edde0-120">*deviceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edde0-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edde0-121">El dispositivo al que se conectará la unidad.</span><span class="sxs-lookup"><span data-stu-id="edde0-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="edde0-122">Value</span><span class="sxs-lookup"><span data-stu-id="edde0-122">Value</span></span>                                                                        | <span data-ttu-id="edde0-123">Significado</span><span class="sxs-lookup"><span data-stu-id="edde0-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="edde0-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="edde0-125">La unidad se conectará al primer dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="edde0-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="edde0-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="edde0-127">La unidad se conectará al segundo dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="edde0-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="edde0-128">*dvdDrive* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="edde0-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="edde0-129">Objeto [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="edde0-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edde0-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edde0-130">Return value</span></span>

<span data-ttu-id="edde0-131">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="edde0-131">This method can return one of these values.</span></span>



| <span data-ttu-id="edde0-132">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edde0-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="edde0-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="edde0-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="edde0-134"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="edde0-135">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="edde0-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="edde0-136"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="edde0-137">El parámetro *dvdDrive* es **null**.</span><span class="sxs-lookup"><span data-stu-id="edde0-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="edde0-138"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="edde0-139">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="edde0-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="edde0-140"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="edde0-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="edde0-141">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="edde0-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="edde0-142"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="edde0-143">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="edde0-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="edde0-144"><dt>**Máquina virtual \_ E \_ unidad \_ \_ de bus \_ de disco en \_ uso**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="edde0-145">La ubicación de bus especificada está en uso.</span><span class="sxs-lookup"><span data-stu-id="edde0-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="edde0-146"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="edde0-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="edde0-147">La unidad especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="edde0-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="edde0-148"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="edde0-149">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="edde0-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="edde0-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edde0-150">Remarks</span></span>

<span data-ttu-id="edde0-151">Solo puede Agregar una nueva unidad de CD o DVD a una máquina virtual detenida.</span><span class="sxs-lookup"><span data-stu-id="edde0-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="edde0-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edde0-152">Requirements</span></span>



| <span data-ttu-id="edde0-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="edde0-153">Requirement</span></span> | <span data-ttu-id="edde0-154">Value</span><span class="sxs-lookup"><span data-stu-id="edde0-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="edde0-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edde0-155">Minimum supported client</span></span><br/> | <span data-ttu-id="edde0-156">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="edde0-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="edde0-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edde0-157">Minimum supported server</span></span><br/> | <span data-ttu-id="edde0-158">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="edde0-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="edde0-159">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="edde0-159">End of client support</span></span><br/>    | <span data-ttu-id="edde0-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="edde0-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="edde0-161">Producto</span><span class="sxs-lookup"><span data-stu-id="edde0-161">Product</span></span><br/>                  | <span data-ttu-id="edde0-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="edde0-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="edde0-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edde0-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="edde0-164"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="edde0-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="edde0-165">IID</span><span class="sxs-lookup"><span data-stu-id="edde0-165">IID</span></span><br/>                      | <span data-ttu-id="edde0-166">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="edde0-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="edde0-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="edde0-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edde0-168">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="edde0-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

