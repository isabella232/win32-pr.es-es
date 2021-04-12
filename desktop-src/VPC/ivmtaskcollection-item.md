---
title: Propiedad del elemento IVMTaskCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de tarea que corresponde al índice especificado.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMTaskCollection
- Interfaz IVMTaskCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534773"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="cc3af-106">IVMTaskCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cc3af-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="cc3af-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cc3af-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cc3af-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cc3af-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cc3af-109">Recupera el objeto de tarea que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cc3af-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="cc3af-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc3af-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3af-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc3af-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="cc3af-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cc3af-112">Property value</span></span>

<span data-ttu-id="cc3af-113">El objeto [**IVMTask**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="cc3af-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cc3af-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cc3af-114">Error codes</span></span>



| <span data-ttu-id="cc3af-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="cc3af-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cc3af-116">Significado</span><span class="sxs-lookup"><span data-stu-id="cc3af-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc3af-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cc3af-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cc3af-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc3af-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="cc3af-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cc3af-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cc3af-120">El parámetro de *tarea* es **null**.</span><span class="sxs-lookup"><span data-stu-id="cc3af-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="cc3af-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="cc3af-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="cc3af-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="cc3af-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="cc3af-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cc3af-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cc3af-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="cc3af-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="cc3af-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc3af-125">Requirements</span></span>



| <span data-ttu-id="cc3af-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc3af-126">Requirement</span></span> | <span data-ttu-id="cc3af-127">Value</span><span class="sxs-lookup"><span data-stu-id="cc3af-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3af-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc3af-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3af-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc3af-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc3af-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc3af-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3af-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc3af-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cc3af-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="cc3af-132">End of client support</span></span><br/>    | <span data-ttu-id="cc3af-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc3af-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cc3af-134">Producto</span><span class="sxs-lookup"><span data-stu-id="cc3af-134">Product</span></span><br/>                  | <span data-ttu-id="cc3af-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cc3af-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cc3af-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc3af-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc3af-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc3af-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cc3af-138">IID</span><span class="sxs-lookup"><span data-stu-id="cc3af-138">IID</span></span><br/>                      | <span data-ttu-id="cc3af-139">IID \_ IVMTaskCollection se define como 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="cc3af-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cc3af-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc3af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3af-141">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="cc3af-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="cc3af-142">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="cc3af-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

