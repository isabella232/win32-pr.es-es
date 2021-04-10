---
title: Propiedad _NewEnum IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Recupera un enumerador para la colección. | Propiedad _NewEnum IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
ms.assetid: 3ea01a88-72ec-4dc0-901f-e48092cf9251
keywords:
- _NewEnum propiedad de PC virtual
- Propiedad _NewEnum Virtual PC, interfaz IVMVirtualNetworkCollection
- Interfaz IVMVirtualNetworkCollection Virtual PC, propiedad _NewEnum
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection._NewEnum
- IVMVirtualNetworkCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50a279e3f160a79f143a7516e29c0dbc3eccdf4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280196"
---
# <a name="ivmvirtualnetworkcollection_newenum-property"></a><span data-ttu-id="296dc-107">IVMVirtualNetworkCollection:: \_ NewEnum (propiedad)</span><span class="sxs-lookup"><span data-stu-id="296dc-107">IVMVirtualNetworkCollection::\_NewEnum property</span></span>

<span data-ttu-id="296dc-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="296dc-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="296dc-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="296dc-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="296dc-110">Recupera un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="296dc-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="296dc-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="296dc-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="296dc-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="296dc-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="296dc-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="296dc-113">Property value</span></span>

<span data-ttu-id="296dc-114">Enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="296dc-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="296dc-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="296dc-115">Error codes</span></span>



| <span data-ttu-id="296dc-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="296dc-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="296dc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="296dc-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="296dc-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="296dc-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="296dc-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="296dc-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="296dc-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="296dc-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="296dc-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="296dc-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="296dc-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="296dc-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="296dc-123">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="296dc-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="296dc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="296dc-124">Requirements</span></span>



| <span data-ttu-id="296dc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="296dc-125">Requirement</span></span> | <span data-ttu-id="296dc-126">Value</span><span class="sxs-lookup"><span data-stu-id="296dc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="296dc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="296dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="296dc-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="296dc-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="296dc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="296dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="296dc-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="296dc-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="296dc-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="296dc-131">End of client support</span></span><br/>    | <span data-ttu-id="296dc-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="296dc-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="296dc-133">Producto</span><span class="sxs-lookup"><span data-stu-id="296dc-133">Product</span></span><br/>                  | <span data-ttu-id="296dc-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="296dc-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="296dc-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="296dc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="296dc-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="296dc-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="296dc-137">IID</span><span class="sxs-lookup"><span data-stu-id="296dc-137">IID</span></span><br/>                      | <span data-ttu-id="296dc-138">IID \_ IVMVirtualNetworkCollection se define como 8ed680be-4242-4B2A-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="296dc-138">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="296dc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="296dc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="296dc-140">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="296dc-140">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

