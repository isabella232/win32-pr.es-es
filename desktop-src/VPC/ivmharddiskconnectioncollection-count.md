---
title: Propiedad de recuento de IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera el número de conexiones del disco duro de esta colección.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMHardDiskConnectionCollection
- Interfaz IVMHardDiskConnectionCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802467"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="45b8f-106">IVMHardDiskConnectionCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="45b8f-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="45b8f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45b8f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="45b8f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="45b8f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="45b8f-109">Recupera el número de conexiones del disco duro de esta colección.</span><span class="sxs-lookup"><span data-stu-id="45b8f-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="45b8f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="45b8f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b8f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45b8f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="45b8f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="45b8f-112">Property value</span></span>

<span data-ttu-id="45b8f-113">El número de conexiones del disco duro.</span><span class="sxs-lookup"><span data-stu-id="45b8f-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45b8f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="45b8f-114">Error codes</span></span>



| <span data-ttu-id="45b8f-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="45b8f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="45b8f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="45b8f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="45b8f-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="45b8f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="45b8f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="45b8f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="45b8f-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="45b8f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="45b8f-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="45b8f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="45b8f-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="45b8f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="45b8f-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="45b8f-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="45b8f-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="45b8f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="45b8f-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="45b8f-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="45b8f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b8f-125">Requirements</span></span>



| <span data-ttu-id="45b8f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b8f-126">Requirement</span></span> | <span data-ttu-id="45b8f-127">Value</span><span class="sxs-lookup"><span data-stu-id="45b8f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b8f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="45b8f-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="45b8f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="45b8f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="45b8f-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="45b8f-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="45b8f-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="45b8f-132">End of client support</span></span><br/>    | <span data-ttu-id="45b8f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45b8f-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="45b8f-134">Producto</span><span class="sxs-lookup"><span data-stu-id="45b8f-134">Product</span></span><br/>                  | <span data-ttu-id="45b8f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="45b8f-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="45b8f-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45b8f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="45b8f-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b8f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="45b8f-138">IID</span><span class="sxs-lookup"><span data-stu-id="45b8f-138">IID</span></span><br/>                      | <span data-ttu-id="45b8f-139">IID \_ IVMHardDiskconnectionCollection se define como b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="45b8f-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45b8f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="45b8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b8f-141">**IVMHardDiskConnectionCollection**</span><span class="sxs-lookup"><span data-stu-id="45b8f-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

