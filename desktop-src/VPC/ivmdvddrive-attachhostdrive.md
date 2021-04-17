---
title: Método IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Conecta una unidad host a la unidad de DVD de la máquina virtual.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Método AttachHostDrive Virtual PC
- Método AttachHostDrive Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012afcdc0b88aa5b77f1d85cc5becff1e70853f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651414"
---
# <a name="ivmdvddriveattachhostdrive-method"></a><span data-ttu-id="5bec2-106">IVMDVDDrive:: AttachHostDrive (método)</span><span class="sxs-lookup"><span data-stu-id="5bec2-106">IVMDVDDrive::AttachHostDrive method</span></span>

<span data-ttu-id="5bec2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5bec2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5bec2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5bec2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5bec2-109">Conecta una unidad host a la unidad de DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bec2-109">Attaches a host drive to the DVD drive within the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bec2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bec2-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="5bec2-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bec2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bec2-112">*letraDeUnidad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bec2-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bec2-113">La letra de la unidad de host que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="5bec2-113">The letter of the host drive that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bec2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bec2-114">Return value</span></span>

<span data-ttu-id="5bec2-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="5bec2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5bec2-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bec2-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="5bec2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bec2-117">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bec2-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="5bec2-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5bec2-119">The operation was successful.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="5bec2-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="5bec2-121">No se especificó ninguna letra de unidad o la letra de unidad especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="5bec2-121">No drive letter was specified, or the specified drive letter is invalid.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="5bec2-122"><dt>**E \_ ERROR**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-122"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="5bec2-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="5bec2-123">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="5bec2-124"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="5bec2-125">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bec2-125">The virtual machine could not be found.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="5bec2-126"><dt>**Máquina virtual \_ \_Unidad E \_ en \_ uso**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="5bec2-127">Ya hay una unidad de DVD de host o una imagen ISO conectada a esta unidad en la máquina virtual, o bien la unidad de host especificada ya está en uso en otra máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bec2-127">A host DVD drive or ISO image is already attached to this drive within the virtual machine, or the specified host drive is already in use within another virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="5bec2-128"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="5bec2-129">La ubicación del bus para esta unidad no es válida o la unidad no parece ser una unidad de DVD válida.</span><span class="sxs-lookup"><span data-stu-id="5bec2-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="5bec2-130"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="5bec2-131">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="5bec2-131">An unexpected error has occurred.</span></span><br/>                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="5bec2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bec2-132">Requirements</span></span>



| <span data-ttu-id="5bec2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bec2-133">Requirement</span></span> | <span data-ttu-id="5bec2-134">Value</span><span class="sxs-lookup"><span data-stu-id="5bec2-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bec2-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bec2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5bec2-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5bec2-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5bec2-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bec2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5bec2-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5bec2-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5bec2-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5bec2-139">End of client support</span></span><br/>    | <span data-ttu-id="5bec2-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5bec2-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5bec2-141">Producto</span><span class="sxs-lookup"><span data-stu-id="5bec2-141">Product</span></span><br/>                  | <span data-ttu-id="5bec2-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5bec2-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5bec2-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bec2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bec2-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bec2-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5bec2-145">IID</span><span class="sxs-lookup"><span data-stu-id="5bec2-145">IID</span></span><br/>                      | <span data-ttu-id="5bec2-146">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="5bec2-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="5bec2-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bec2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bec2-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="5bec2-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

