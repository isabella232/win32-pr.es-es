---
title: Propiedad de archivo IVMHardDisk (VPCCOMInterfaces. h)
description: Recupera el nombre de la ruta de acceso completa del archivo de disco duro virtual.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Propiedad de archivo equipo virtual PC
- Propiedad de archivo Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad de archivo
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696019"
---
# <a name="ivmharddiskfile-property"></a><span data-ttu-id="a2467-106">IVMHardDisk:: file (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a2467-106">IVMHardDisk::File property</span></span>

<span data-ttu-id="a2467-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2467-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2467-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2467-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2467-109">Recupera el nombre de la ruta de acceso completa del archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="a2467-109">Retrieves the full path name of the virtual hard disk file.</span></span>

<span data-ttu-id="a2467-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2467-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2467-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2467-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a><span data-ttu-id="a2467-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a2467-112">Property value</span></span>

<span data-ttu-id="a2467-113">Nombre de la ruta de acceso completa del archivo de imagen de disco duro actual.</span><span class="sxs-lookup"><span data-stu-id="a2467-113">The full path name of the current hard disk image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a2467-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a2467-114">Error codes</span></span>



| <span data-ttu-id="a2467-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="a2467-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a2467-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a2467-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a2467-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a2467-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a2467-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a2467-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a2467-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a2467-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a2467-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="a2467-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a2467-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a2467-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a2467-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a2467-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a2467-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2467-123">Requirements</span></span>



| <span data-ttu-id="a2467-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2467-124">Requirement</span></span> | <span data-ttu-id="a2467-125">Value</span><span class="sxs-lookup"><span data-stu-id="a2467-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2467-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2467-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a2467-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2467-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2467-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2467-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a2467-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a2467-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2467-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a2467-130">End of client support</span></span><br/>    | <span data-ttu-id="a2467-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2467-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2467-132">Producto</span><span class="sxs-lookup"><span data-stu-id="a2467-132">Product</span></span><br/>                  | <span data-ttu-id="a2467-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2467-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2467-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2467-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2467-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2467-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2467-136">IID</span><span class="sxs-lookup"><span data-stu-id="a2467-136">IID</span></span><br/>                      | <span data-ttu-id="a2467-137">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="a2467-137">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a2467-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2467-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2467-139">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a2467-139">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

