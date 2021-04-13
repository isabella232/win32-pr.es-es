---
title: Propiedad IVMHardDiskConnection BusNumber (VPCCOMInterfaces. h)
description: Recupera el número de bus al que está conectada la imagen de la unidad.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- Propiedad BusNumber Virtual PC
- Propiedad BusNumber Virtual PC, interfaz IVMHardDiskConnection
- Interfaz IVMHardDiskConnection Virtual PC, propiedad BusNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491884"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a><span data-ttu-id="9308c-106">IVMHardDiskConnection:: BusNumber (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9308c-106">IVMHardDiskConnection::BusNumber property</span></span>

<span data-ttu-id="9308c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9308c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9308c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9308c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9308c-109">Recupera el número de bus al que está conectada la imagen de la unidad.</span><span class="sxs-lookup"><span data-stu-id="9308c-109">Retrieves the bus number to which the drive image is attached.</span></span>

<span data-ttu-id="9308c-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9308c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9308c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9308c-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="9308c-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9308c-112">Property value</span></span>

<span data-ttu-id="9308c-113">Número de bus que corresponde a esta conexión.</span><span class="sxs-lookup"><span data-stu-id="9308c-113">The bus number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9308c-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9308c-114">Error codes</span></span>



| <span data-ttu-id="9308c-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="9308c-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="9308c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9308c-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9308c-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9308c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="9308c-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9308c-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="9308c-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9308c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="9308c-120">El parámetro es **null** o no es válido.</span><span class="sxs-lookup"><span data-stu-id="9308c-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9308c-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9308c-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="9308c-122">La configuración de máquina virtual actual no es válida.</span><span class="sxs-lookup"><span data-stu-id="9308c-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="9308c-123"><dt>Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9308c-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="9308c-124">La ubicación del bus para esta conexión no se ha inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9308c-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="9308c-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9308c-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="9308c-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9308c-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="9308c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9308c-127">Requirements</span></span>



| <span data-ttu-id="9308c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9308c-128">Requirement</span></span> | <span data-ttu-id="9308c-129">Value</span><span class="sxs-lookup"><span data-stu-id="9308c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9308c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9308c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9308c-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9308c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9308c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9308c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9308c-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9308c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9308c-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9308c-134">End of client support</span></span><br/>    | <span data-ttu-id="9308c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9308c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9308c-136">Producto</span><span class="sxs-lookup"><span data-stu-id="9308c-136">Product</span></span><br/>                  | <span data-ttu-id="9308c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9308c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9308c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9308c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9308c-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9308c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9308c-140">IID</span><span class="sxs-lookup"><span data-stu-id="9308c-140">IID</span></span><br/>                      | <span data-ttu-id="9308c-141">IID \_ IVMHardDiskconnection se define como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="9308c-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="9308c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9308c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9308c-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="9308c-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

