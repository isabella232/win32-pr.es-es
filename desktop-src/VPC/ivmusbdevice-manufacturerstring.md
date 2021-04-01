---
title: Propiedad IVMUSBDevice ManufacturerString (VPCCOMInterfaces. h)
description: Recupera el nombre del fabricante del dispositivo USB.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Propiedad ManufacturerString Virtual PC
- Propiedad ManufacturerString Virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad ManufacturerString
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8d74cbe737c59e10daf2cf3ee93e4b1f14983f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150696"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a><span data-ttu-id="26c1b-106">IVMUSBDevice:: ManufacturerString (propiedad)</span><span class="sxs-lookup"><span data-stu-id="26c1b-106">IVMUSBDevice::ManufacturerString property</span></span>

<span data-ttu-id="26c1b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="26c1b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="26c1b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="26c1b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="26c1b-109">Recupera el nombre del fabricante del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="26c1b-109">Retrieves the name of the USB device manufacturer.</span></span>

<span data-ttu-id="26c1b-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26c1b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c1b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26c1b-111">Syntax</span></span>


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a><span data-ttu-id="26c1b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="26c1b-112">Property value</span></span>

<span data-ttu-id="26c1b-113">Nombre del fabricante del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="26c1b-113">The name of the USB device manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26c1b-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="26c1b-114">Error codes</span></span>



| <span data-ttu-id="26c1b-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="26c1b-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="26c1b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="26c1b-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="26c1b-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="26c1b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="26c1b-118">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="26c1b-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="26c1b-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="26c1b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="26c1b-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="26c1b-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="26c1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26c1b-121">Requirements</span></span>



| <span data-ttu-id="26c1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c1b-122">Requirement</span></span> | <span data-ttu-id="26c1b-123">Value</span><span class="sxs-lookup"><span data-stu-id="26c1b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c1b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26c1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26c1b-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="26c1b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26c1b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26c1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26c1b-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="26c1b-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="26c1b-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="26c1b-128">End of client support</span></span><br/>    | <span data-ttu-id="26c1b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26c1b-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="26c1b-130">Producto</span><span class="sxs-lookup"><span data-stu-id="26c1b-130">Product</span></span><br/>                  | <span data-ttu-id="26c1b-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="26c1b-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="26c1b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26c1b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="26c1b-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="26c1b-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="26c1b-134">IID</span><span class="sxs-lookup"><span data-stu-id="26c1b-134">IID</span></span><br/>                      | <span data-ttu-id="26c1b-135">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="26c1b-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="26c1b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="26c1b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c1b-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="26c1b-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

