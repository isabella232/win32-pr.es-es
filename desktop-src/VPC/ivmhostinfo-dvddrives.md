---
title: Propiedad IVMHostInfo DVDDrives (VPCCOMInterfaces. h)
description: Recupera las letras de unidad asociadas a los dispositivos de CD y DVD del host.
ms.assetid: 17f01d00-2c02-48f0-bfe9-0326a40fdf55
keywords:
- Propiedad DVDDrives Virtual PC
- Propiedad DVDDrives Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad DVDDrives
topic_type:
- apiref
api_name:
- IVMHostInfo.DVDDrives
- IVMHostInfo.get_DVDDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb9380773934b63ae637d32ec5acfef5112f2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422300"
---
# <a name="ivmhostinfodvddrives-property"></a><span data-ttu-id="0e057-106">IVMHostInfo::D propiedad VDDrives</span><span class="sxs-lookup"><span data-stu-id="0e057-106">IVMHostInfo::DVDDrives property</span></span>

<span data-ttu-id="0e057-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0e057-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0e057-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0e057-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0e057-109">Recupera las letras de unidad asociadas a los dispositivos de CD y DVD del host.</span><span class="sxs-lookup"><span data-stu-id="0e057-109">Retrieves the drive letters associated with host CD and DVD devices.</span></span>

<span data-ttu-id="0e057-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0e057-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e057-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e057-111">Syntax</span></span>


```C++
HRESULT get_DVDDrives(
  [out, retval] VARIANT *DVDDrives
);
```



## <a name="property-value"></a><span data-ttu-id="0e057-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0e057-112">Property value</span></span>

<span data-ttu-id="0e057-113">Matriz de Letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="0e057-113">An array of drive letters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e057-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0e057-114">Error codes</span></span>



| <span data-ttu-id="0e057-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="0e057-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0e057-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0e057-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0e057-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e057-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0e057-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0e057-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0e057-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0e057-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0e057-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="0e057-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0e057-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0e057-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0e057-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0e057-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0e057-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e057-123">Requirements</span></span>



| <span data-ttu-id="0e057-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e057-124">Requirement</span></span> | <span data-ttu-id="0e057-125">Value</span><span class="sxs-lookup"><span data-stu-id="0e057-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e057-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e057-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e057-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e057-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e057-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e057-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e057-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0e057-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0e057-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0e057-130">End of client support</span></span><br/>    | <span data-ttu-id="0e057-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e057-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0e057-132">Producto</span><span class="sxs-lookup"><span data-stu-id="0e057-132">Product</span></span><br/>                  | <span data-ttu-id="0e057-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0e057-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0e057-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e057-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e057-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e057-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0e057-136">IID</span><span class="sxs-lookup"><span data-stu-id="0e057-136">IID</span></span><br/>                      | <span data-ttu-id="0e057-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="0e057-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0e057-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e057-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e057-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="0e057-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

