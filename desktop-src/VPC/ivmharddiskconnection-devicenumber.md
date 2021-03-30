---
title: Propiedad IVMHardDiskConnection DeviceNumber (VPCCOMInterfaces. h)
description: Recupera el número de dispositivo al que está conectada la imagen de la unidad.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- Propiedad DeviceNumber Virtual PC
- Propiedad DeviceNumber Virtual PC, interfaz IVMHardDiskConnection
- Interfaz IVMHardDiskConnection Virtual PC, propiedad DeviceNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150995"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a><span data-ttu-id="bd780-106">IVMHardDiskConnection::D propiedad eviceNumber</span><span class="sxs-lookup"><span data-stu-id="bd780-106">IVMHardDiskConnection::DeviceNumber property</span></span>

<span data-ttu-id="bd780-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bd780-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bd780-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bd780-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bd780-109">Recupera el número de dispositivo al que está conectada la imagen de la unidad.</span><span class="sxs-lookup"><span data-stu-id="bd780-109">Retrieves the device number to which the drive image is attached.</span></span>

<span data-ttu-id="bd780-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bd780-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd780-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd780-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="bd780-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bd780-112">Property value</span></span>

<span data-ttu-id="bd780-113">El número de dispositivo que corresponde a esta conexión.</span><span class="sxs-lookup"><span data-stu-id="bd780-113">The device number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd780-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bd780-114">Error codes</span></span>



| <span data-ttu-id="bd780-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="bd780-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="bd780-116">Significado</span><span class="sxs-lookup"><span data-stu-id="bd780-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd780-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd780-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="bd780-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd780-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="bd780-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bd780-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="bd780-120">El parámetro es **null** o no es válido.</span><span class="sxs-lookup"><span data-stu-id="bd780-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="bd780-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bd780-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="bd780-122">La configuración de máquina virtual actual no es válida.</span><span class="sxs-lookup"><span data-stu-id="bd780-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="bd780-123"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bd780-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="bd780-124">La ubicación del bus para esta conexión no se ha inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd780-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="bd780-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bd780-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="bd780-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="bd780-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="bd780-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd780-127">Requirements</span></span>



| <span data-ttu-id="bd780-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd780-128">Requirement</span></span> | <span data-ttu-id="bd780-129">Value</span><span class="sxs-lookup"><span data-stu-id="bd780-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd780-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd780-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bd780-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd780-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd780-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd780-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bd780-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bd780-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bd780-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bd780-134">End of client support</span></span><br/>    | <span data-ttu-id="bd780-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd780-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bd780-136">Producto</span><span class="sxs-lookup"><span data-stu-id="bd780-136">Product</span></span><br/>                  | <span data-ttu-id="bd780-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bd780-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bd780-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd780-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd780-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd780-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bd780-140">IID</span><span class="sxs-lookup"><span data-stu-id="bd780-140">IID</span></span><br/>                      | <span data-ttu-id="bd780-141">IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="bd780-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="bd780-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd780-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd780-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="bd780-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

