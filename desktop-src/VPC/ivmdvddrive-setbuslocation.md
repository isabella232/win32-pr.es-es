---
title: Método IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Conecta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Método SetBusLocation Virtual PC
- Método SetBusLocation Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676767"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="a338d-106">IVMDVDDrive:: SetBusLocation (método)</span><span class="sxs-lookup"><span data-stu-id="a338d-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="a338d-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a338d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a338d-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a338d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a338d-109">Conecta la unidad de DVD a la ubicación de bus especificada en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a338d-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a338d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a338d-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="a338d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a338d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a338d-112">*busNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a338d-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a338d-113">Número de bus al que se va a adjuntar esta unidad.</span><span class="sxs-lookup"><span data-stu-id="a338d-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="a338d-114">Por ejemplo, en un bus IDE, este número representaría si se usara el número de bus principal o secundario.</span><span class="sxs-lookup"><span data-stu-id="a338d-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="a338d-115">*deviceNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a338d-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a338d-116">Número de dispositivo al que se va a adjuntar esta unidad.</span><span class="sxs-lookup"><span data-stu-id="a338d-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="a338d-117">Por ejemplo, en un bus IDE, este número representaría si se usara la ubicación del dispositivo principal o secundario.</span><span class="sxs-lookup"><span data-stu-id="a338d-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a338d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a338d-118">Return value</span></span>

<span data-ttu-id="a338d-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a338d-119">This method can return one of these values.</span></span>



| <span data-ttu-id="a338d-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a338d-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="a338d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a338d-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a338d-122"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="a338d-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a338d-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="a338d-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="a338d-125">La ubicación de bus especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="a338d-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="a338d-126"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="a338d-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a338d-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="a338d-128"><dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="a338d-129">No se puede establecer la ubicación del bus mientras la máquina virtual está en ejecución o en un estado guardado.</span><span class="sxs-lookup"><span data-stu-id="a338d-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a338d-130"><dt>**VM \_ E \_ bus \_ Loc \_ en \_ uso**</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="a338d-131">Otro dispositivo ya está conectado a la ubicación de bus especificada.</span><span class="sxs-lookup"><span data-stu-id="a338d-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="a338d-132"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a338d-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="a338d-133">No se pudo inicializar la unidad actual.</span><span class="sxs-lookup"><span data-stu-id="a338d-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="a338d-134"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a338d-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="a338d-135">No se pudieron escribir los cambios en el archivo de preferencias porque no se pudo determinar la máquina virtual de esta unidad.</span><span class="sxs-lookup"><span data-stu-id="a338d-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="a338d-136"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="a338d-137">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a338d-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="a338d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a338d-138">Requirements</span></span>



| <span data-ttu-id="a338d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a338d-139">Requirement</span></span> | <span data-ttu-id="a338d-140">Value</span><span class="sxs-lookup"><span data-stu-id="a338d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a338d-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a338d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a338d-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a338d-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a338d-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a338d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a338d-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a338d-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a338d-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a338d-145">End of client support</span></span><br/>    | <span data-ttu-id="a338d-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a338d-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a338d-147">Producto</span><span class="sxs-lookup"><span data-stu-id="a338d-147">Product</span></span><br/>                  | <span data-ttu-id="a338d-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a338d-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a338d-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a338d-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a338d-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a338d-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a338d-151">IID</span><span class="sxs-lookup"><span data-stu-id="a338d-151">IID</span></span><br/>                      | <span data-ttu-id="a338d-152">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="a338d-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a338d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="a338d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a338d-154">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="a338d-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

