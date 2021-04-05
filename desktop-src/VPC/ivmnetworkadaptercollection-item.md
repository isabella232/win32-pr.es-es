---
title: Propiedad del elemento IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Objeto IVMNetworkAdapter que corresponde al índice especificado.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMNetworkAdapterCollection
- Interfaz IVMNetworkAdapterCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997041"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="c46c2-106">IVMNetworkAdapterCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c46c2-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="c46c2-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c46c2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c46c2-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c46c2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c46c2-109">Recupera el objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c46c2-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="c46c2-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c46c2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46c2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c46c2-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="c46c2-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c46c2-112">Property value</span></span>

<span data-ttu-id="c46c2-113">El objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="c46c2-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c46c2-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c46c2-114">Error codes</span></span>



| <span data-ttu-id="c46c2-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="c46c2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c46c2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c46c2-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c46c2-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c46c2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c46c2-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c46c2-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="c46c2-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c46c2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c46c2-120">El parámetro *interfaz Cluster* es **null**.</span><span class="sxs-lookup"><span data-stu-id="c46c2-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="c46c2-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="c46c2-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="c46c2-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="c46c2-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="c46c2-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c46c2-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c46c2-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="c46c2-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="c46c2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c46c2-125">Requirements</span></span>



| <span data-ttu-id="c46c2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c46c2-126">Requirement</span></span> | <span data-ttu-id="c46c2-127">Value</span><span class="sxs-lookup"><span data-stu-id="c46c2-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c46c2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c46c2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c46c2-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c46c2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c46c2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c46c2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c46c2-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c46c2-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c46c2-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c46c2-132">End of client support</span></span><br/>    | <span data-ttu-id="c46c2-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c46c2-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="c46c2-134">Producto</span><span class="sxs-lookup"><span data-stu-id="c46c2-134">Product</span></span><br/>                  | <span data-ttu-id="c46c2-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c46c2-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="c46c2-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c46c2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c46c2-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c46c2-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="c46c2-138">IID</span><span class="sxs-lookup"><span data-stu-id="c46c2-138">IID</span></span><br/>                      | <span data-ttu-id="c46c2-139">IID \_ IVMNetworkAdapterCollection se define como ebaeafe9-eBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="c46c2-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c46c2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c46c2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46c2-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="c46c2-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="c46c2-142">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="c46c2-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

