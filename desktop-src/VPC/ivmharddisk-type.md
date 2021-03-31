---
title: Propiedad de tipo IVMHardDisk (VPCCOMInterfaces. h)
description: Tipo de disco duro virtual.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Propiedad de tipo Virtual PC
- Propiedad Type Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad de tipo
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079330"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="82b01-106">IVMHardDisk:: Type (propiedad)</span><span class="sxs-lookup"><span data-stu-id="82b01-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="82b01-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="82b01-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82b01-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="82b01-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82b01-109">Recupera el tipo del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="82b01-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="82b01-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="82b01-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b01-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82b01-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="82b01-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="82b01-112">Property value</span></span>

<span data-ttu-id="82b01-113">El tipo de la imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="82b01-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="82b01-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="82b01-114">Error codes</span></span>



| <span data-ttu-id="82b01-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="82b01-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="82b01-116">Significado</span><span class="sxs-lookup"><span data-stu-id="82b01-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82b01-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82b01-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="82b01-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="82b01-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="82b01-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="82b01-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="82b01-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="82b01-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="82b01-121"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="82b01-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="82b01-122">No se encontró el archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="82b01-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="82b01-123"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="82b01-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="82b01-124">El tipo de la imagen de disco duro actual no es válido.</span><span class="sxs-lookup"><span data-stu-id="82b01-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="82b01-125"><dt>Máquina virtual \_ E \_ HD \_ Image \_ Open \_ FAIL</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="82b01-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="82b01-126">Se produjo un error al intentar abrir el archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="82b01-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="82b01-127"><dt>Máquina virtual \_ E 0xA0040681 de \_ \_ \_ acceso a imágenes HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="82b01-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="82b01-128">Error al intentar obtener acceso al archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="82b01-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="82b01-129"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="82b01-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="82b01-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="82b01-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="82b01-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82b01-131">Requirements</span></span>



| <span data-ttu-id="82b01-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b01-132">Requirement</span></span> | <span data-ttu-id="82b01-133">Value</span><span class="sxs-lookup"><span data-stu-id="82b01-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b01-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82b01-134">Minimum supported client</span></span><br/> | <span data-ttu-id="82b01-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="82b01-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82b01-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82b01-136">Minimum supported server</span></span><br/> | <span data-ttu-id="82b01-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="82b01-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82b01-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="82b01-138">End of client support</span></span><br/>    | <span data-ttu-id="82b01-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82b01-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82b01-140">Producto</span><span class="sxs-lookup"><span data-stu-id="82b01-140">Product</span></span><br/>                  | <span data-ttu-id="82b01-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82b01-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82b01-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82b01-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b01-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="82b01-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82b01-144">IID</span><span class="sxs-lookup"><span data-stu-id="82b01-144">IID</span></span><br/>                      | <span data-ttu-id="82b01-145">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="82b01-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="82b01-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="82b01-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b01-147">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="82b01-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

