---
title: Propiedad del elemento IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de dispositivo USB que corresponde al índice especificado.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMUSBDeviceCollection
- Interfaz IVMUSBDeviceCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490937"
---
# <a name="ivmusbdevicecollectionitem-property"></a><span data-ttu-id="39624-106">IVMUSBDeviceCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="39624-106">IVMUSBDeviceCollection::Item property</span></span>

<span data-ttu-id="39624-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39624-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39624-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39624-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39624-109">Recupera el objeto de dispositivo USB que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="39624-109">Retrieves the USB device object that corresponds to the specified index.</span></span>

<span data-ttu-id="39624-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39624-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39624-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39624-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a><span data-ttu-id="39624-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="39624-112">Property value</span></span>

<span data-ttu-id="39624-113">El objeto [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="39624-113">The [**IVMUSBDevice**](ivmusbdevice.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39624-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="39624-114">Error codes</span></span>



| <span data-ttu-id="39624-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="39624-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="39624-116">Significado</span><span class="sxs-lookup"><span data-stu-id="39624-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39624-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39624-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="39624-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="39624-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="39624-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="39624-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="39624-120">El parámetro *usbDevice* es **null**.</span><span class="sxs-lookup"><span data-stu-id="39624-120">The *usbDevice* parameter is **NULL**.</span></span> <br/>                                             |
| <dl> <span data-ttu-id="39624-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="39624-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="39624-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="39624-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="39624-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="39624-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="39624-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="39624-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="39624-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39624-125">Requirements</span></span>



| <span data-ttu-id="39624-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="39624-126">Requirement</span></span> | <span data-ttu-id="39624-127">Value</span><span class="sxs-lookup"><span data-stu-id="39624-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39624-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39624-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39624-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="39624-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39624-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39624-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39624-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="39624-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39624-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="39624-132">End of client support</span></span><br/>    | <span data-ttu-id="39624-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39624-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39624-134">Producto</span><span class="sxs-lookup"><span data-stu-id="39624-134">Product</span></span><br/>                  | <span data-ttu-id="39624-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39624-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39624-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39624-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="39624-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39624-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39624-138">IID</span><span class="sxs-lookup"><span data-stu-id="39624-138">IID</span></span><br/>                      | <span data-ttu-id="39624-139">IID \_ IVMUSBDeviceCollection se define como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="39624-139">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="39624-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="39624-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39624-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="39624-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="39624-142">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="39624-142">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

