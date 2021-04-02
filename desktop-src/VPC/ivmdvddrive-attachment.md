---
title: Propiedad de datos adjuntos IVMDVDDrive (VPCCOMInterfaces. h)
description: Recupera el tipo de medio conectado a la unidad de DVD de la máquina virtual.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Propiedad de datos adjuntos Virtual PC
- Propiedad Attachment Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad Attachment
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905434"
---
# <a name="ivmdvddriveattachment-property"></a><span data-ttu-id="56e48-106">IVMDVDDrive:: Attachment (propiedad)</span><span class="sxs-lookup"><span data-stu-id="56e48-106">IVMDVDDrive::Attachment property</span></span>

<span data-ttu-id="56e48-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="56e48-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56e48-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56e48-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56e48-109">Recupera el tipo de medio conectado a la unidad de DVD de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="56e48-109">Retrieves the type of media attached to the DVD drive within the virtual machine.</span></span>

<span data-ttu-id="56e48-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="56e48-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e48-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56e48-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="56e48-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56e48-112">Property value</span></span>

<span data-ttu-id="56e48-113">El tipo de medio asociado.</span><span class="sxs-lookup"><span data-stu-id="56e48-113">The attached media type.</span></span> <span data-ttu-id="56e48-114">Para obtener una lista de valores, vea [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="56e48-114">For a list of values, see [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="56e48-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="56e48-115">Error codes</span></span>



| <span data-ttu-id="56e48-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="56e48-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="56e48-117">Significado</span><span class="sxs-lookup"><span data-stu-id="56e48-117">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="56e48-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56e48-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="56e48-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="56e48-119">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="56e48-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="56e48-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="56e48-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="56e48-121">The parameter is **NULL**.</span></span><br/>                  |
| <dl> <span data-ttu-id="56e48-122"><dt>E \_ ERROR</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="56e48-122"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="56e48-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="56e48-123">An unexpected error has occurred.</span></span><br/>           |
| <dl> <span data-ttu-id="56e48-124"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="56e48-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="56e48-125">No se encontró la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="56e48-125">The virtual machine could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="56e48-126"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="56e48-126"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="56e48-127">La ubicación del bus para esta unidad no es válida.</span><span class="sxs-lookup"><span data-stu-id="56e48-127">The bus location for this drive is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="56e48-128"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="56e48-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="56e48-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="56e48-129">An unexpected error has occurred.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="56e48-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56e48-130">Requirements</span></span>



| <span data-ttu-id="56e48-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="56e48-131">Requirement</span></span> | <span data-ttu-id="56e48-132">Value</span><span class="sxs-lookup"><span data-stu-id="56e48-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e48-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56e48-133">Minimum supported client</span></span><br/> | <span data-ttu-id="56e48-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="56e48-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56e48-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56e48-135">Minimum supported server</span></span><br/> | <span data-ttu-id="56e48-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="56e48-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56e48-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="56e48-137">End of client support</span></span><br/>    | <span data-ttu-id="56e48-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56e48-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56e48-139">Producto</span><span class="sxs-lookup"><span data-stu-id="56e48-139">Product</span></span><br/>                  | <span data-ttu-id="56e48-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56e48-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56e48-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56e48-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="56e48-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e48-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56e48-143">IID</span><span class="sxs-lookup"><span data-stu-id="56e48-143">IID</span></span><br/>                      | <span data-ttu-id="56e48-144">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="56e48-144">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="56e48-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="56e48-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e48-146">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="56e48-146">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

