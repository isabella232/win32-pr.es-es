---
title: Propiedad IVMDVDDrive BusNumber (VPCCOMInterfaces. h)
description: Recupera el número de bus al que está conectado este dispositivo.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Propiedad BusNumber Virtual PC
- Propiedad BusNumber Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, propiedad BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676867"
---
# <a name="ivmdvddrivebusnumber-property"></a><span data-ttu-id="b2749-106">IVMDVDDrive:: BusNumber (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b2749-106">IVMDVDDrive::BusNumber property</span></span>

<span data-ttu-id="b2749-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b2749-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b2749-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b2749-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b2749-109">Recupera el número de bus al que está conectado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2749-109">Retrieves the bus number to which this device is attached.</span></span>

<span data-ttu-id="b2749-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2749-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2749-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2749-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="b2749-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b2749-112">Property value</span></span>

<span data-ttu-id="b2749-113">El número de bus.</span><span class="sxs-lookup"><span data-stu-id="b2749-113">The bus number.</span></span> <span data-ttu-id="b2749-114">Por ejemplo, en un bus IDE, este valor representaría la ubicación principal o secundaria.</span><span class="sxs-lookup"><span data-stu-id="b2749-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2749-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b2749-115">Error codes</span></span>



| <span data-ttu-id="b2749-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b2749-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="b2749-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b2749-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2749-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2749-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="b2749-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2749-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="b2749-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b2749-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="b2749-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b2749-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b2749-122"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2749-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="b2749-123">La ubicación del bus para esta unidad de DVD no se ha inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2749-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="b2749-124"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b2749-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="b2749-125">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b2749-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="b2749-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2749-126">Requirements</span></span>



| <span data-ttu-id="b2749-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2749-127">Requirement</span></span> | <span data-ttu-id="b2749-128">Value</span><span class="sxs-lookup"><span data-stu-id="b2749-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2749-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2749-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2749-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2749-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2749-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2749-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2749-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2749-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b2749-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b2749-133">End of client support</span></span><br/>    | <span data-ttu-id="b2749-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b2749-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b2749-135">Producto</span><span class="sxs-lookup"><span data-stu-id="b2749-135">Product</span></span><br/>                  | <span data-ttu-id="b2749-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b2749-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b2749-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2749-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2749-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2749-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b2749-139">IID</span><span class="sxs-lookup"><span data-stu-id="b2749-139">IID</span></span><br/>                      | <span data-ttu-id="b2749-140">IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="b2749-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b2749-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2749-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2749-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="b2749-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

