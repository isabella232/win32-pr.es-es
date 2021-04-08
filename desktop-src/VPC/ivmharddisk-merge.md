---
title: Método Merge de IVMHardDisk (VPCCOMInterfaces. h)
description: Combina un disco duro virtual de diferenciación con su imagen de disco principal.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Merge Method Virtual PC
- Merge Method Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996586"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="f55b6-106">IVMHardDisk:: Merge (método)</span><span class="sxs-lookup"><span data-stu-id="f55b6-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="f55b6-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f55b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f55b6-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f55b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f55b6-109">Combina un disco duro virtual de diferenciación con su imagen de disco principal.</span><span class="sxs-lookup"><span data-stu-id="f55b6-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f55b6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f55b6-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="f55b6-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f55b6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55b6-112">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f55b6-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f55b6-113">Objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de combinación.</span><span class="sxs-lookup"><span data-stu-id="f55b6-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55b6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f55b6-114">Return value</span></span>

<span data-ttu-id="f55b6-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f55b6-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f55b6-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f55b6-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="f55b6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f55b6-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f55b6-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="f55b6-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f55b6-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f55b6-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="f55b6-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f55b6-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f55b6-122"><dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="f55b6-123">La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está en uso o el elemento primario de esta imagen de disco duro virtual está en uso.</span><span class="sxs-lookup"><span data-stu-id="f55b6-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="f55b6-124">O bien, estas imágenes de disco duro podrían formar parte de un estado guardado.</span><span class="sxs-lookup"><span data-stu-id="f55b6-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="f55b6-125"><dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="f55b6-126">La imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) debe ser una imagen de disco de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="f55b6-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="f55b6-127"><dt>**Máquina virtual \_ E & 0xA004067A de \_ \_ \_ solo lectura de archivos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="f55b6-128">El elemento primario de la imagen de disco duro virtual al que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) está marcado como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f55b6-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f55b6-129"><dt>**Máquina virtual \_ \_ \_ \_ No \_ se encontró la ruta de acceso principal E**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="f55b6-130">No existe el elemento primario del disco duro virtual al que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) .</span><span class="sxs-lookup"><span data-stu-id="f55b6-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="f55b6-131"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f55b6-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="f55b6-132">No se puede fusionar mediante combinación la imagen de disco duro virtual porque se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="f55b6-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="f55b6-133"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="f55b6-134">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f55b6-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="f55b6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f55b6-135">Requirements</span></span>



| <span data-ttu-id="f55b6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f55b6-136">Requirement</span></span> | <span data-ttu-id="f55b6-137">Value</span><span class="sxs-lookup"><span data-stu-id="f55b6-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f55b6-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f55b6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f55b6-139">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f55b6-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f55b6-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f55b6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f55b6-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f55b6-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f55b6-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f55b6-142">End of client support</span></span><br/>    | <span data-ttu-id="f55b6-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f55b6-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f55b6-144">Producto</span><span class="sxs-lookup"><span data-stu-id="f55b6-144">Product</span></span><br/>                  | <span data-ttu-id="f55b6-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f55b6-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f55b6-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f55b6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55b6-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55b6-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f55b6-148">IID</span><span class="sxs-lookup"><span data-stu-id="f55b6-148">IID</span></span><br/>                      | <span data-ttu-id="f55b6-149">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="f55b6-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f55b6-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f55b6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55b6-151">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="f55b6-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

