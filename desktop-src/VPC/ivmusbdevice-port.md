---
title: Propiedad de Puerto IVMUSBDevice (VPCCOMInterfaces. h)
description: Recupera el identificador del puerto en el que está conectado el dispositivo.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Propiedad de puerto virtual PC
- Propiedad de puerto virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad de Puerto
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803578"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="b2ebc-106">IVMUSBDevice::P propiedad ordenar</span><span class="sxs-lookup"><span data-stu-id="b2ebc-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="b2ebc-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b2ebc-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b2ebc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b2ebc-109">Recupera el identificador del puerto en el que está conectado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="b2ebc-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ebc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2ebc-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="b2ebc-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b2ebc-112">Property value</span></span>

<span data-ttu-id="b2ebc-113">Identificador de puerto.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-113">The port identifier.</span></span> <span data-ttu-id="b2ebc-114">Este valor se asigna mediante el controlador del conector USB.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2ebc-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b2ebc-115">Error codes</span></span>



| <span data-ttu-id="b2ebc-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b2ebc-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="b2ebc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b2ebc-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="b2ebc-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2ebc-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="b2ebc-119">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b2ebc-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b2ebc-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="b2ebc-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b2ebc-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="b2ebc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2ebc-122">Requirements</span></span>



| <span data-ttu-id="b2ebc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ebc-123">Requirement</span></span> | <span data-ttu-id="b2ebc-124">Value</span><span class="sxs-lookup"><span data-stu-id="b2ebc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ebc-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2ebc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ebc-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2ebc-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2ebc-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2ebc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ebc-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2ebc-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b2ebc-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b2ebc-129">End of client support</span></span><br/>    | <span data-ttu-id="b2ebc-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b2ebc-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b2ebc-131">Producto</span><span class="sxs-lookup"><span data-stu-id="b2ebc-131">Product</span></span><br/>                  | <span data-ttu-id="b2ebc-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b2ebc-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b2ebc-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2ebc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2ebc-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ebc-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b2ebc-135">IID</span><span class="sxs-lookup"><span data-stu-id="b2ebc-135">IID</span></span><br/>                      | <span data-ttu-id="b2ebc-136">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="b2ebc-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b2ebc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2ebc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ebc-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="b2ebc-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

