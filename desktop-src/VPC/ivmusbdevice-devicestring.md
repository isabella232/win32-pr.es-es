---
title: Propiedad IVMUSBDevice DeviceString (VPCCOMInterfaces. h)
description: Recupera el nombre del dispositivo USB.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Propiedad DeviceString Virtual PC
- Propiedad DeviceString Virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad DeviceString
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905302"
---
# <a name="ivmusbdevicedevicestring-property"></a><span data-ttu-id="2448a-106">IVMUSBDevice::D propiedad eviceString</span><span class="sxs-lookup"><span data-stu-id="2448a-106">IVMUSBDevice::DeviceString property</span></span>

<span data-ttu-id="2448a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2448a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2448a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2448a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2448a-109">Recupera el nombre del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="2448a-109">Retrieves the name of the USB device.</span></span>

<span data-ttu-id="2448a-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2448a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2448a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2448a-111">Syntax</span></span>


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a><span data-ttu-id="2448a-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2448a-112">Property value</span></span>

<span data-ttu-id="2448a-113">Nombre del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="2448a-113">The name of the USB device.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2448a-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2448a-114">Error codes</span></span>



| <span data-ttu-id="2448a-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="2448a-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="2448a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2448a-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="2448a-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2448a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="2448a-118">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2448a-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2448a-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2448a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="2448a-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2448a-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="2448a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2448a-121">Requirements</span></span>



| <span data-ttu-id="2448a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2448a-122">Requirement</span></span> | <span data-ttu-id="2448a-123">Value</span><span class="sxs-lookup"><span data-stu-id="2448a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2448a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2448a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2448a-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2448a-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2448a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2448a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2448a-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2448a-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2448a-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2448a-128">End of client support</span></span><br/>    | <span data-ttu-id="2448a-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2448a-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2448a-130">Producto</span><span class="sxs-lookup"><span data-stu-id="2448a-130">Product</span></span><br/>                  | <span data-ttu-id="2448a-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2448a-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2448a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2448a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2448a-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2448a-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2448a-134">IID</span><span class="sxs-lookup"><span data-stu-id="2448a-134">IID</span></span><br/>                      | <span data-ttu-id="2448a-135">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="2448a-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2448a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2448a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2448a-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="2448a-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

