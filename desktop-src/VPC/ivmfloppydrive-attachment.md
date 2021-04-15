---
title: Propiedad de datos adjuntos IVMFloppyDrive (VPCCOMInterfaces. h)
description: Recupera el tipo de medio conectado a la unidad de disquete en la máquina virtual.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Propiedad de datos adjuntos Virtual PC
- Propiedad Attachment Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, propiedad Attachment
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695952"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="f0950-106">IVMFloppyDrive:: Attachment (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f0950-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="f0950-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0950-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0950-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0950-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0950-109">Recupera el tipo de medio conectado a la unidad de disquete en la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="f0950-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="f0950-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f0950-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0950-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0950-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="f0950-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f0950-112">Property value</span></span>

<span data-ttu-id="f0950-113">Tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="f0950-113">The type of media.</span></span> <span data-ttu-id="f0950-114">Para obtener una lista de valores, vea [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="f0950-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0950-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f0950-115">Error codes</span></span>



| <span data-ttu-id="f0950-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="f0950-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f0950-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f0950-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0950-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0950-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f0950-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0950-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f0950-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f0950-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f0950-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f0950-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f0950-122"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f0950-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f0950-123">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="f0950-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="f0950-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0950-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f0950-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f0950-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="f0950-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0950-126">Requirements</span></span>



| <span data-ttu-id="f0950-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0950-127">Requirement</span></span> | <span data-ttu-id="f0950-128">Value</span><span class="sxs-lookup"><span data-stu-id="f0950-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0950-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0950-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0950-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0950-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0950-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0950-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0950-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0950-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0950-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f0950-133">End of client support</span></span><br/>    | <span data-ttu-id="f0950-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0950-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0950-135">Producto</span><span class="sxs-lookup"><span data-stu-id="f0950-135">Product</span></span><br/>                  | <span data-ttu-id="f0950-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0950-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0950-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0950-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0950-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0950-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0950-139">IID</span><span class="sxs-lookup"><span data-stu-id="f0950-139">IID</span></span><br/>                      | <span data-ttu-id="f0950-140">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="f0950-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f0950-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0950-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0950-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="f0950-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

