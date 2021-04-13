---
title: Propiedad IVMUSBDevice DeviceClass (VPCCOMInterfaces. h)
description: Recupera la clase de dispositivo del dispositivo USB.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- Propiedad DeviceClass Virtual PC
- Propiedad DeviceClass Virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad DeviceClass
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422504"
---
# <a name="ivmusbdevicedeviceclass-property"></a><span data-ttu-id="d191b-106">IVMUSBDevice::D propiedad eviceClass</span><span class="sxs-lookup"><span data-stu-id="d191b-106">IVMUSBDevice::DeviceClass property</span></span>

<span data-ttu-id="d191b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d191b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d191b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d191b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d191b-109">Recupera la clase de dispositivo del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="d191b-109">Retrieves the device class of the USB device.</span></span>

<span data-ttu-id="d191b-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d191b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d191b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d191b-111">Syntax</span></span>


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a><span data-ttu-id="d191b-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d191b-112">Property value</span></span>

<span data-ttu-id="d191b-113">Clase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d191b-113">The device class.</span></span> <span data-ttu-id="d191b-114">Para obtener una lista de valores, vea [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span><span class="sxs-lookup"><span data-stu-id="d191b-114">For a list of values, see [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d191b-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d191b-115">Error codes</span></span>



| <span data-ttu-id="d191b-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d191b-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="d191b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="d191b-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="d191b-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d191b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="d191b-119">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d191b-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d191b-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d191b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="d191b-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d191b-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="d191b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d191b-122">Requirements</span></span>



| <span data-ttu-id="d191b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d191b-123">Requirement</span></span> | <span data-ttu-id="d191b-124">Value</span><span class="sxs-lookup"><span data-stu-id="d191b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d191b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d191b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d191b-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d191b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d191b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d191b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d191b-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d191b-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d191b-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d191b-129">End of client support</span></span><br/>    | <span data-ttu-id="d191b-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d191b-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d191b-131">Producto</span><span class="sxs-lookup"><span data-stu-id="d191b-131">Product</span></span><br/>                  | <span data-ttu-id="d191b-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d191b-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d191b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d191b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d191b-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d191b-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d191b-135">IID</span><span class="sxs-lookup"><span data-stu-id="d191b-135">IID</span></span><br/>                      | <span data-ttu-id="d191b-136">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="d191b-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d191b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d191b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d191b-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="d191b-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

