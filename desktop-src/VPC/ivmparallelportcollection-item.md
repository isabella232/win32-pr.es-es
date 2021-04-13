---
title: Propiedad del elemento IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de puerto paralelo que corresponde al índice especificado.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMParallelPortCollection
- Interfaz IVMParallelPortCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492586"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="1972f-106">IVMParallelPortCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1972f-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="1972f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1972f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1972f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1972f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1972f-109">Recupera el objeto de puerto paralelo que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1972f-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="1972f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1972f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1972f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1972f-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="1972f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1972f-112">Property value</span></span>

<span data-ttu-id="1972f-113">El objeto [**IVMParallelPort**](ivmparallelport.md) .</span><span class="sxs-lookup"><span data-stu-id="1972f-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1972f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1972f-114">Error codes</span></span>



| <span data-ttu-id="1972f-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="1972f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1972f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1972f-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1972f-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1972f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1972f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1972f-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="1972f-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1972f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1972f-120">El parámetro *vmParallelPort* es **null**.</span><span class="sxs-lookup"><span data-stu-id="1972f-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="1972f-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="1972f-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="1972f-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="1972f-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="1972f-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1972f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="1972f-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="1972f-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="1972f-125"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1972f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1972f-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1972f-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="1972f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1972f-127">Requirements</span></span>



| <span data-ttu-id="1972f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1972f-128">Requirement</span></span> | <span data-ttu-id="1972f-129">Value</span><span class="sxs-lookup"><span data-stu-id="1972f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1972f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1972f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1972f-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1972f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1972f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1972f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1972f-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1972f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1972f-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1972f-134">End of client support</span></span><br/>    | <span data-ttu-id="1972f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1972f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1972f-136">Producto</span><span class="sxs-lookup"><span data-stu-id="1972f-136">Product</span></span><br/>                  | <span data-ttu-id="1972f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1972f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1972f-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1972f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1972f-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1972f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1972f-140">IID</span><span class="sxs-lookup"><span data-stu-id="1972f-140">IID</span></span><br/>                      | <span data-ttu-id="1972f-141">IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="1972f-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1972f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1972f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1972f-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="1972f-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="1972f-144">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="1972f-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

