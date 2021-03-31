---
title: Propiedad IVMUSBDevice HubID (VPCCOMInterfaces. h)
description: Recupera el identificador del concentrador en el que está conectado el dispositivo.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- Propiedad HubID Virtual PC
- Propiedad HubID Virtual PC, interfaz IVMUSBDevice
- Interfaz IVMUSBDevice Virtual PC, propiedad HubID
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53faa79ee999022f993070767846ee4e4723c3a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079580"
---
# <a name="ivmusbdevicehubid-property"></a><span data-ttu-id="66f07-106">IVMUSBDevice:: HubID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="66f07-106">IVMUSBDevice::HubID property</span></span>

<span data-ttu-id="66f07-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="66f07-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66f07-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66f07-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66f07-109">Recupera el identificador del concentrador en el que está conectado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66f07-109">Retrieves the identifier of the hub on which the device is connected.</span></span>

<span data-ttu-id="66f07-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="66f07-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f07-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66f07-111">Syntax</span></span>


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a><span data-ttu-id="66f07-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="66f07-112">Property value</span></span>

<span data-ttu-id="66f07-113">Identificador del centro.</span><span class="sxs-lookup"><span data-stu-id="66f07-113">The hub identifier.</span></span> <span data-ttu-id="66f07-114">Este valor se asigna mediante el controlador del conector USB.</span><span class="sxs-lookup"><span data-stu-id="66f07-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66f07-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="66f07-115">Error codes</span></span>



| <span data-ttu-id="66f07-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="66f07-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="66f07-117">Significado</span><span class="sxs-lookup"><span data-stu-id="66f07-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="66f07-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66f07-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="66f07-119">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="66f07-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="66f07-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66f07-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="66f07-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="66f07-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="66f07-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f07-122">Requirements</span></span>



| <span data-ttu-id="66f07-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f07-123">Requirement</span></span> | <span data-ttu-id="66f07-124">Value</span><span class="sxs-lookup"><span data-stu-id="66f07-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f07-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66f07-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66f07-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="66f07-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66f07-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66f07-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66f07-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="66f07-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66f07-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="66f07-129">End of client support</span></span><br/>    | <span data-ttu-id="66f07-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66f07-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66f07-131">Producto</span><span class="sxs-lookup"><span data-stu-id="66f07-131">Product</span></span><br/>                  | <span data-ttu-id="66f07-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66f07-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66f07-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66f07-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="66f07-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f07-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66f07-135">IID</span><span class="sxs-lookup"><span data-stu-id="66f07-135">IID</span></span><br/>                      | <span data-ttu-id="66f07-136">IID \_ IVMUSBDevice se define como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="66f07-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="66f07-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="66f07-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f07-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="66f07-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

