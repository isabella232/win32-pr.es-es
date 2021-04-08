---
title: Propiedad _NewEnum IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMUSBDeviceCollection (VPCCOMInterfaces. h)
ms.assetid: f14f64a0-e65a-44d6-b053-54bbcb9ea804
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMUSBDeviceCollection
- Interfaz IVMUSBDeviceCollection Virtual PC, propiedad _NewEnum
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection._NewEnum
- IVMUSBDeviceCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e1e2a4d80691be26161ae4835ccb85c0e722d8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003738"
---
# <a name="ivmusbdevicecollection_newenum-property"></a><span data-ttu-id="a373b-107">IVMUSBDeviceCollection:: \_ NewEnum (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a373b-107">IVMUSBDeviceCollection::\_NewEnum property</span></span>

<span data-ttu-id="a373b-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a373b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a373b-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a373b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a373b-110">Recupera un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="a373b-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="a373b-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a373b-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a373b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a373b-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="a373b-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a373b-113">Property value</span></span>

<span data-ttu-id="a373b-114">Enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="a373b-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a373b-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a373b-115">Error codes</span></span>



| <span data-ttu-id="a373b-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="a373b-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a373b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a373b-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a373b-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a373b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a373b-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a373b-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a373b-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a373b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a373b-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="a373b-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a373b-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a373b-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a373b-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a373b-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a373b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a373b-124">Requirements</span></span>



| <span data-ttu-id="a373b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a373b-125">Requirement</span></span> | <span data-ttu-id="a373b-126">Value</span><span class="sxs-lookup"><span data-stu-id="a373b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a373b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a373b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a373b-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a373b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a373b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a373b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a373b-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a373b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a373b-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a373b-131">End of client support</span></span><br/>    | <span data-ttu-id="a373b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a373b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a373b-133">Producto</span><span class="sxs-lookup"><span data-stu-id="a373b-133">Product</span></span><br/>                  | <span data-ttu-id="a373b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a373b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a373b-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a373b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a373b-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a373b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a373b-137">IID</span><span class="sxs-lookup"><span data-stu-id="a373b-137">IID</span></span><br/>                      | <span data-ttu-id="a373b-138">IID \_ IVMUSBDeviceCollection se define como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="a373b-138">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="a373b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a373b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a373b-140">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="a373b-140">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

