---
title: Método compacto IVMHardDisk (VPCCOMInterfaces. h)
description: Compacta una imagen de disco duro virtual de expansión dinámica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Método compacto Virtual PC
- Método compacto Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método compacto
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803584"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="99123-106">IVMHardDisk:: Compact (método)</span><span class="sxs-lookup"><span data-stu-id="99123-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="99123-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="99123-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="99123-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="99123-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="99123-109">Compacta una imagen de disco duro virtual de expansión dinámica.</span><span class="sxs-lookup"><span data-stu-id="99123-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="99123-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99123-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="99123-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99123-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99123-112">*compactTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="99123-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="99123-113">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de compactación.</span><span class="sxs-lookup"><span data-stu-id="99123-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99123-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99123-114">Return value</span></span>

<span data-ttu-id="99123-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="99123-115">This method can return one of these values.</span></span>



| <span data-ttu-id="99123-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99123-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="99123-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="99123-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99123-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="99123-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="99123-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99123-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="99123-120"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="99123-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="99123-121">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="99123-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="99123-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="99123-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="99123-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="99123-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="99123-124"><dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="99123-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="99123-125">La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está en uso.</span><span class="sxs-lookup"><span data-stu-id="99123-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="99123-126"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="99123-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="99123-127">El volumen del host no tiene espacio suficiente para crear un archivo temporal necesario para la compactación de esta imagen de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="99123-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="99123-128"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="99123-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="99123-129">La imagen del disco duro virtual no se puede compactar porque la aplicación se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="99123-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="99123-130"><dt>**Máquina virtual \_ E & 0xA004067A de \_ \_ \_ solo lectura de archivos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="99123-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="99123-131">La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) se marca como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="99123-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="99123-132"><dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="99123-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="99123-133">La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) debe ser un tipo de imagen **vmDiskTypeDynamic** .</span><span class="sxs-lookup"><span data-stu-id="99123-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="99123-134"><dt>**Máquina virtual \_ E 0xA0040682 de \_ \_ \_ archivo HD no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="99123-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="99123-135">Parece que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen válida.</span><span class="sxs-lookup"><span data-stu-id="99123-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="99123-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99123-136">Remarks</span></span>

<span data-ttu-id="99123-137">Para compactar una imagen de disco duro de expansión dinámica, el espacio libre en la imagen de disco debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="99123-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="99123-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99123-138">Requirements</span></span>



| <span data-ttu-id="99123-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="99123-139">Requirement</span></span> | <span data-ttu-id="99123-140">Value</span><span class="sxs-lookup"><span data-stu-id="99123-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99123-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99123-141">Minimum supported client</span></span><br/> | <span data-ttu-id="99123-142">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="99123-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99123-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99123-143">Minimum supported server</span></span><br/> | <span data-ttu-id="99123-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="99123-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="99123-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="99123-145">End of client support</span></span><br/>    | <span data-ttu-id="99123-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99123-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="99123-147">Producto</span><span class="sxs-lookup"><span data-stu-id="99123-147">Product</span></span><br/>                  | <span data-ttu-id="99123-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="99123-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="99123-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99123-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="99123-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="99123-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="99123-151">IID</span><span class="sxs-lookup"><span data-stu-id="99123-151">IID</span></span><br/>                      | <span data-ttu-id="99123-152">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="99123-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="99123-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="99123-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99123-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="99123-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

