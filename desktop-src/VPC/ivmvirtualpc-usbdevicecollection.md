---
title: Propiedad IVMVirtualPC USBDeviceCollection (VPCCOMInterfaces. h)
description: Colección enumerable de todos los dispositivos USB conectados al host.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Propiedad USBDeviceCollection Virtual PC
- Propiedad USBDeviceCollection Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad USBDeviceCollection
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802678"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a><span data-ttu-id="88368-106">IVMVirtualPC:: USBDeviceCollection (propiedad)</span><span class="sxs-lookup"><span data-stu-id="88368-106">IVMVirtualPC::USBDeviceCollection property</span></span>

<span data-ttu-id="88368-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88368-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88368-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88368-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88368-109">Recupera una colección enumerable de todos los dispositivos USB conectados al host.</span><span class="sxs-lookup"><span data-stu-id="88368-109">Retrieves an enumerable collection of all USB devices connected to the host.</span></span>

<span data-ttu-id="88368-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="88368-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88368-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88368-111">Syntax</span></span>


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="88368-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="88368-112">Property value</span></span>

<span data-ttu-id="88368-113">Referencia a un puntero [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) que representa una colección de objetos [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="88368-113">A reference to an [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) pointer that represents a collection of [**IVMUSBDevice**](ivmusbdevice.md) objects.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88368-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="88368-114">Error codes</span></span>



| <span data-ttu-id="88368-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="88368-115">Name/value</span></span>                                                                                                                                                                                | <span data-ttu-id="88368-116">Significado</span><span class="sxs-lookup"><span data-stu-id="88368-116">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88368-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88368-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="88368-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="88368-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="88368-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="88368-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="88368-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="88368-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="88368-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="88368-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="88368-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="88368-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="88368-123"><dt>Máquina virtual \_ \_Error de \_ enumeración USB \_ \_ más \_ dispositivos</dt> <dt>0xA0040930</dt></span><span class="sxs-lookup"><span data-stu-id="88368-123"><dt>VM\_E\_USB\_ENUMERATION\_FAILED\_MORE\_DEVICES</dt> <dt>0xA0040930</dt></span></span> </dl> | <span data-ttu-id="88368-124">Hay más de 16 dispositivos USB conectados al host.</span><span class="sxs-lookup"><span data-stu-id="88368-124">More than 16 USB devices are connected to the host.</span></span><br/>                                  |
| <dl> <span data-ttu-id="88368-125"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="88368-125"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>      | <span data-ttu-id="88368-126">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="88368-126">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="88368-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88368-127">Requirements</span></span>



| <span data-ttu-id="88368-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="88368-128">Requirement</span></span> | <span data-ttu-id="88368-129">Value</span><span class="sxs-lookup"><span data-stu-id="88368-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="88368-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88368-130">Minimum supported client</span></span><br/> | <span data-ttu-id="88368-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="88368-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88368-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88368-132">Minimum supported server</span></span><br/> | <span data-ttu-id="88368-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88368-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="88368-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="88368-134">End of client support</span></span><br/>    | <span data-ttu-id="88368-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88368-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="88368-136">Producto</span><span class="sxs-lookup"><span data-stu-id="88368-136">Product</span></span><br/>                  | <span data-ttu-id="88368-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88368-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="88368-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88368-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="88368-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="88368-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="88368-140">IID</span><span class="sxs-lookup"><span data-stu-id="88368-140">IID</span></span><br/>                      | <span data-ttu-id="88368-141">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="88368-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="88368-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="88368-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88368-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="88368-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

