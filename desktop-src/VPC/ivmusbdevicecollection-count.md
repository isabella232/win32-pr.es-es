---
title: Propiedad de recuento de IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera el número de dispositivos USB de esta colección.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Propiedad Count Virtual PC
- Propiedad Count Virtual PC, interfaz IVMUSBDeviceCollection
- Interfaz IVMUSBDeviceCollection Virtual PC, propiedad Count
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490942"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="79185-106">IVMUSBDeviceCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="79185-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="79185-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79185-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79185-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79185-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79185-109">Recupera el número de dispositivos USB de esta colección.</span><span class="sxs-lookup"><span data-stu-id="79185-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="79185-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="79185-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79185-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79185-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="79185-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="79185-112">Property value</span></span>

<span data-ttu-id="79185-113">El número de dispositivos USB.</span><span class="sxs-lookup"><span data-stu-id="79185-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79185-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="79185-114">Error codes</span></span>



| <span data-ttu-id="79185-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="79185-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="79185-116">Significado</span><span class="sxs-lookup"><span data-stu-id="79185-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="79185-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79185-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="79185-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="79185-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="79185-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="79185-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="79185-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="79185-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="79185-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="79185-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="79185-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="79185-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="79185-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79185-123">Requirements</span></span>



| <span data-ttu-id="79185-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79185-124">Requirement</span></span> | <span data-ttu-id="79185-125">Value</span><span class="sxs-lookup"><span data-stu-id="79185-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79185-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79185-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79185-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="79185-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79185-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79185-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79185-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79185-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79185-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="79185-130">End of client support</span></span><br/>    | <span data-ttu-id="79185-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79185-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79185-132">Producto</span><span class="sxs-lookup"><span data-stu-id="79185-132">Product</span></span><br/>                  | <span data-ttu-id="79185-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79185-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79185-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79185-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="79185-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="79185-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="79185-136">IID</span><span class="sxs-lookup"><span data-stu-id="79185-136">IID</span></span><br/>                      | <span data-ttu-id="79185-137">IID \_ IVMUSBDeviceCollection se define como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="79185-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="79185-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="79185-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79185-139">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="79185-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

