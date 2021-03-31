---
title: Propiedad IVMHardDisk SizeOnHost (VPCCOMInterfaces. h)
description: Tamaño del archivo de disco duro virtual en el equipo host.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Propiedad SizeOnHost Virtual PC
- Propiedad SizeOnHost Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, propiedad SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079583"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="b1cab-106">IVMHardDisk:: SizeOnHost (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b1cab-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="b1cab-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1cab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b1cab-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b1cab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b1cab-109">Recupera el tamaño del archivo de disco duro virtual en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="b1cab-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="b1cab-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b1cab-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cab-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1cab-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="b1cab-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b1cab-112">Property value</span></span>

<span data-ttu-id="b1cab-113">Tamaño, en bytes, del archivo de imagen del disco duro.</span><span class="sxs-lookup"><span data-stu-id="b1cab-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="b1cab-114">Este valor es una **variante** de tipo **VT \_ decimal**.</span><span class="sxs-lookup"><span data-stu-id="b1cab-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1cab-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b1cab-115">Error codes</span></span>



| <span data-ttu-id="b1cab-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b1cab-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="b1cab-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b1cab-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="b1cab-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b1cab-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1cab-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="b1cab-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b1cab-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b1cab-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="b1cab-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b1cab-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b1cab-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="b1cab-124"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b1cab-125">No se encontró el archivo de imagen de disco duro.</span><span class="sxs-lookup"><span data-stu-id="b1cab-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b1cab-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1cab-126">Requirements</span></span>



| <span data-ttu-id="b1cab-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1cab-127">Requirement</span></span> | <span data-ttu-id="b1cab-128">Value</span><span class="sxs-lookup"><span data-stu-id="b1cab-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cab-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1cab-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b1cab-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1cab-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1cab-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1cab-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b1cab-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b1cab-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b1cab-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b1cab-133">End of client support</span></span><br/>    | <span data-ttu-id="b1cab-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1cab-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b1cab-135">Producto</span><span class="sxs-lookup"><span data-stu-id="b1cab-135">Product</span></span><br/>                  | <span data-ttu-id="b1cab-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b1cab-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b1cab-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1cab-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1cab-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1cab-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b1cab-139">IID</span><span class="sxs-lookup"><span data-stu-id="b1cab-139">IID</span></span><br/>                      | <span data-ttu-id="b1cab-140">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="b1cab-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b1cab-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1cab-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1cab-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="b1cab-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

