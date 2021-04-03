---
title: Propiedad de recuento de IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Número de unidades de disquete en esta colección.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMFloppyDriveCollection
- Interfaz IVMFloppyDriveCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b00c13795a633c664cea2c4476d58b346f9108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079733"
---
# <a name="ivmfloppydrivecollectioncount-property"></a><span data-ttu-id="d6195-106">IVMFloppyDriveCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d6195-106">IVMFloppyDriveCollection::Count property</span></span>

<span data-ttu-id="d6195-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6195-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d6195-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d6195-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d6195-109">Recupera el número de unidades de disquete de esta colección.</span><span class="sxs-lookup"><span data-stu-id="d6195-109">Retrieves the number of floppy drives in this collection.</span></span>

<span data-ttu-id="d6195-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d6195-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6195-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6195-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="d6195-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d6195-112">Property value</span></span>

<span data-ttu-id="d6195-113">El número de unidades de disquete.</span><span class="sxs-lookup"><span data-stu-id="d6195-113">The number of floppy media drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6195-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d6195-114">Error codes</span></span>



| <span data-ttu-id="d6195-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d6195-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d6195-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d6195-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d6195-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d6195-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d6195-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6195-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d6195-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d6195-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d6195-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d6195-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d6195-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d6195-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d6195-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="d6195-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="d6195-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d6195-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d6195-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d6195-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d6195-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6195-125">Requirements</span></span>



| <span data-ttu-id="d6195-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6195-126">Requirement</span></span> | <span data-ttu-id="d6195-127">Value</span><span class="sxs-lookup"><span data-stu-id="d6195-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6195-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6195-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d6195-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6195-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6195-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6195-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d6195-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d6195-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d6195-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d6195-132">End of client support</span></span><br/>    | <span data-ttu-id="d6195-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6195-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d6195-134">Producto</span><span class="sxs-lookup"><span data-stu-id="d6195-134">Product</span></span><br/>                  | <span data-ttu-id="d6195-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d6195-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d6195-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6195-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6195-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6195-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d6195-138">IID</span><span class="sxs-lookup"><span data-stu-id="d6195-138">IID</span></span><br/>                      | <span data-ttu-id="d6195-139">IID \_ IVMFloppyDriveCollection se define como 8ba70a25-F698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="d6195-139">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d6195-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6195-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6195-141">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="d6195-141">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

