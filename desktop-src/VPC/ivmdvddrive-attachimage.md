---
title: Método IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Adjunta una imagen ISO a la unidad de DVD de la máquina virtual.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Método AttachImage Virtual PC
- Método AttachImage Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422559"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="f829f-106">IVMDVDDrive:: AttachImage (método)</span><span class="sxs-lookup"><span data-stu-id="f829f-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="f829f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f829f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f829f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f829f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f829f-109">Adjunta una imagen ISO a la unidad de DVD de la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="f829f-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f829f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f829f-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="f829f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f829f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f829f-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f829f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f829f-113">Ruta de acceso completa a la imagen ISO que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="f829f-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f829f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f829f-114">Return value</span></span>

<span data-ttu-id="f829f-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f829f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f829f-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f829f-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f829f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f829f-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f829f-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f829f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="f829f-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f829f-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="f829f-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f829f-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="f829f-121">El parámetro *imagePath* es un directorio.</span><span class="sxs-lookup"><span data-stu-id="f829f-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="f829f-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f829f-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="f829f-123">El parámetro *imagePath* es **null**.</span><span class="sxs-lookup"><span data-stu-id="f829f-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f829f-124"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f829f-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="f829f-125">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f829f-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="f829f-126"><dt>**Máquina virtual \_ \_Unidad E \_ en \_ uso**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="f829f-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="f829f-127">Ya hay una unidad de DVD de host o una imagen ISO conectada a esta unidad.</span><span class="sxs-lookup"><span data-stu-id="f829f-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f829f-128"><dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f829f-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="f829f-129">La ubicación del bus para esta unidad no es válida o la unidad no parece ser una unidad de DVD válida.</span><span class="sxs-lookup"><span data-stu-id="f829f-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="f829f-130"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f829f-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="f829f-131">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f829f-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="f829f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f829f-132">Requirements</span></span>



| <span data-ttu-id="f829f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f829f-133">Requirement</span></span> | <span data-ttu-id="f829f-134">Value</span><span class="sxs-lookup"><span data-stu-id="f829f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f829f-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f829f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f829f-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f829f-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f829f-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f829f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f829f-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f829f-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f829f-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f829f-139">End of client support</span></span><br/>    | <span data-ttu-id="f829f-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f829f-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f829f-141">Producto</span><span class="sxs-lookup"><span data-stu-id="f829f-141">Product</span></span><br/>                  | <span data-ttu-id="f829f-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f829f-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f829f-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f829f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f829f-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f829f-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f829f-145">IID</span><span class="sxs-lookup"><span data-stu-id="f829f-145">IID</span></span><br/>                      | <span data-ttu-id="f829f-146">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="f829f-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f829f-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="f829f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f829f-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f829f-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

