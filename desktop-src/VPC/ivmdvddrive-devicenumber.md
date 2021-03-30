---
title: Propiedad IVMDVDDrive DeviceNumber (VPCCOMInterfaces. h)
description: Recupera el número de dispositivo al que está conectada esta unidad.
ms.assetid: 57b09400-e0c8-4ca2-bcd4-e6dd047daf95
keywords:
- Propiedad DeviceNumber Virtual PC
- Propiedad DeviceNumber Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad DeviceNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.DeviceNumber
- IVMDVDDrive.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de189b162ed2c880819f4c8729e996236ace250a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079509"
---
# <a name="ivmdvddrivedevicenumber-property"></a><span data-ttu-id="b0bc3-106">IVMDVDDrive::D propiedad eviceNumber</span><span class="sxs-lookup"><span data-stu-id="b0bc3-106">IVMDVDDrive::DeviceNumber property</span></span>

<span data-ttu-id="b0bc3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b0bc3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b0bc3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b0bc3-109">Recupera el número de dispositivo al que está conectada esta unidad.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-109">Retrieves the device number to which this drive is attached.</span></span>

<span data-ttu-id="b0bc3-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bc3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0bc3-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="b0bc3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b0bc3-112">Property value</span></span>

<span data-ttu-id="b0bc3-113">El número de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-113">The device number.</span></span> <span data-ttu-id="b0bc3-114">Por ejemplo, en un bus IDE, este valor representaría la ubicación principal o secundaria.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0bc3-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b0bc3-115">Error codes</span></span>



| <span data-ttu-id="b0bc3-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b0bc3-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="b0bc3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b0bc3-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0bc3-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0bc3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="b0bc3-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="b0bc3-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b0bc3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="b0bc3-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b0bc3-122"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b0bc3-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="b0bc3-123">La ubicación del bus para esta unidad de DVD no se ha inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="b0bc3-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b0bc3-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="b0bc3-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b0bc3-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="b0bc3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0bc3-126">Requirements</span></span>



| <span data-ttu-id="b0bc3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0bc3-127">Requirement</span></span> | <span data-ttu-id="b0bc3-128">Value</span><span class="sxs-lookup"><span data-stu-id="b0bc3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bc3-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0bc3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b0bc3-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0bc3-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0bc3-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0bc3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b0bc3-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b0bc3-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b0bc3-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b0bc3-133">End of client support</span></span><br/>    | <span data-ttu-id="b0bc3-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0bc3-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b0bc3-135">Producto</span><span class="sxs-lookup"><span data-stu-id="b0bc3-135">Product</span></span><br/>                  | <span data-ttu-id="b0bc3-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b0bc3-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b0bc3-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0bc3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0bc3-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0bc3-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b0bc3-139">IID</span><span class="sxs-lookup"><span data-stu-id="b0bc3-139">IID</span></span><br/>                      | <span data-ttu-id="b0bc3-140">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="b0bc3-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b0bc3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0bc3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bc3-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="b0bc3-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

