---
title: Propiedad IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces. h)
description: Recupera la cantidad de espacio en disco restante disponible en el host para el disco duro virtual.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Propiedad HostFreeDiskSpace Virtual PC
- Propiedad HostFreeDiskSpace Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150996"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="3dbce-106">IVMHardDisk:: HostFreeDiskSpace (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3dbce-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="3dbce-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3dbce-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3dbce-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3dbce-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3dbce-109">Recupera la cantidad de espacio en disco restante disponible en el host para el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="3dbce-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="3dbce-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3dbce-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dbce-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dbce-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="3dbce-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3dbce-112">Property value</span></span>

<span data-ttu-id="3dbce-113">La cantidad de espacio en disco restante disponible en el equipo host para el archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="3dbce-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="3dbce-114">Este valor es una **variante** de tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="3dbce-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3dbce-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3dbce-115">Error codes</span></span>



| <span data-ttu-id="3dbce-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="3dbce-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="3dbce-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3dbce-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3dbce-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3dbce-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="3dbce-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3dbce-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="3dbce-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3dbce-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="3dbce-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="3dbce-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3dbce-122"><dt>HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3dbce-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="3dbce-123">La ruta de acceso al archivo de disco duro virtual actual no es válida.</span><span class="sxs-lookup"><span data-stu-id="3dbce-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="3dbce-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3dbce-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="3dbce-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3dbce-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="3dbce-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbce-126">Requirements</span></span>



| <span data-ttu-id="3dbce-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbce-127">Requirement</span></span> | <span data-ttu-id="3dbce-128">Value</span><span class="sxs-lookup"><span data-stu-id="3dbce-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbce-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dbce-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbce-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3dbce-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3dbce-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dbce-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbce-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3dbce-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3dbce-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3dbce-133">End of client support</span></span><br/>    | <span data-ttu-id="3dbce-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3dbce-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3dbce-135">Producto</span><span class="sxs-lookup"><span data-stu-id="3dbce-135">Product</span></span><br/>                  | <span data-ttu-id="3dbce-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3dbce-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3dbce-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dbce-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbce-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbce-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3dbce-139">IID</span><span class="sxs-lookup"><span data-stu-id="3dbce-139">IID</span></span><br/>                      | <span data-ttu-id="3dbce-140">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="3dbce-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3dbce-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3dbce-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbce-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="3dbce-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

