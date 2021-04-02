---
title: Propiedad nombre de IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Nombre único de la instancia de la red virtual.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Propiedad nombre virtual PC
- Propiedad nombre virtual PC, interfaz IVMVirtualNetwork
- Interfaz IVMVirtualNetwork Virtual PC, propiedad Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996943"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="185b3-106">IVMVirtualNetwork:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="185b3-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="185b3-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="185b3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="185b3-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="185b3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="185b3-109">Recupera el nombre único de la instancia de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="185b3-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="185b3-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="185b3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="185b3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="185b3-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="185b3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="185b3-112">Property value</span></span>

<span data-ttu-id="185b3-113">El nombre de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="185b3-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="185b3-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="185b3-114">Error codes</span></span>



| <span data-ttu-id="185b3-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="185b3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="185b3-116">Significado</span><span class="sxs-lookup"><span data-stu-id="185b3-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="185b3-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="185b3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="185b3-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="185b3-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="185b3-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="185b3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="185b3-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="185b3-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="185b3-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="185b3-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="185b3-122">Se ha producido un error inesperado o se desconoce la instancia de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="185b3-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="185b3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="185b3-123">Remarks</span></span>

<span data-ttu-id="185b3-124">Los nombres de red virtual no distinguen mayúsculas de minúsculas, por ejemplo, "subred" y "subred" hacen referencia a la misma red virtual.</span><span class="sxs-lookup"><span data-stu-id="185b3-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="185b3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="185b3-125">Requirements</span></span>



| <span data-ttu-id="185b3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="185b3-126">Requirement</span></span> | <span data-ttu-id="185b3-127">Value</span><span class="sxs-lookup"><span data-stu-id="185b3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="185b3-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="185b3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="185b3-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="185b3-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="185b3-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="185b3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="185b3-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="185b3-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="185b3-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="185b3-132">End of client support</span></span><br/>    | <span data-ttu-id="185b3-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="185b3-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="185b3-134">Producto</span><span class="sxs-lookup"><span data-stu-id="185b3-134">Product</span></span><br/>                  | <span data-ttu-id="185b3-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="185b3-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="185b3-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="185b3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="185b3-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="185b3-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="185b3-138">IID</span><span class="sxs-lookup"><span data-stu-id="185b3-138">IID</span></span><br/>                      | <span data-ttu-id="185b3-139">IID \_ IVMVirtualNetwork se define como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="185b3-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="185b3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="185b3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185b3-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="185b3-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

