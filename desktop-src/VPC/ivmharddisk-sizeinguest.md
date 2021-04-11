---
title: Propiedad IVMHardDisk SizeInGuest (VPCCOMInterfaces. h)
description: Recupera el tamaño del disco duro virtual en el sistema operativo invitado.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Propiedad SizeInGuest Virtual PC
- Propiedad SizeInGuest Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150698"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="b3b0c-106">IVMHardDisk:: SizeInGuest (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b3b0c-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="b3b0c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b3b0c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b3b0c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b3b0c-109">Recupera el tamaño del disco duro virtual en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="b3b0c-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b0c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3b0c-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="b3b0c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b3b0c-112">Property value</span></span>

<span data-ttu-id="b3b0c-113">Tamaño, en bytes, de la imagen del disco duro.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="b3b0c-114">Este valor es una **variante** de tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3b0c-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b3b0c-115">Error codes</span></span>



| <span data-ttu-id="b3b0c-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b3b0c-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="b3b0c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b3b0c-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3b0c-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b3b0c-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="b3b0c-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b3b0c-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="b3b0c-122"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b3b0c-123">No se encontró el archivo del disco duro virtual actual.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="b3b0c-124"><dt>Máquina virtual \_ E \_ HD \_ Image \_ Open \_ FAIL</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="b3b0c-125">Se produjo un error al intentar abrir el archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="b3b0c-126"><dt>Máquina virtual \_ E 0xA0040681 de \_ \_ \_ acceso a imágenes HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="b3b0c-127">Error al intentar obtener acceso al archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="b3b0c-128"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b3b0c-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b3b0c-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="b3b0c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b0c-130">Requirements</span></span>



| <span data-ttu-id="b3b0c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b0c-131">Requirement</span></span> | <span data-ttu-id="b3b0c-132">Value</span><span class="sxs-lookup"><span data-stu-id="b3b0c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b0c-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3b0c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b0c-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3b0c-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3b0c-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3b0c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b0c-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b3b0c-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b3b0c-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b3b0c-137">End of client support</span></span><br/>    | <span data-ttu-id="b3b0c-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3b0c-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b3b0c-139">Producto</span><span class="sxs-lookup"><span data-stu-id="b3b0c-139">Product</span></span><br/>                  | <span data-ttu-id="b3b0c-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b3b0c-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b3b0c-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3b0c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b0c-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b0c-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b3b0c-143">IID</span><span class="sxs-lookup"><span data-stu-id="b3b0c-143">IID</span></span><br/>                      | <span data-ttu-id="b3b0c-144">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="b3b0c-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b3b0c-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3b0c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b0c-146">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="b3b0c-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

