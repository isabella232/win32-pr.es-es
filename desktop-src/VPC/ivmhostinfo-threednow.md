---
title: Propiedad IVMHostInfo ThreeDNow (VPCCOMInterfaces. h)
description: Determina si el procesador admite el conjunto de instrucciones 3DNow. | Propiedad IVMHostInfo ThreeDNow (VPCCOMInterfaces. h)
ms.assetid: 4987e326-d8fa-4dfa-b592-9dd90cedb0ef
keywords:
- Propiedad ThreeDNow Virtual PC
- Propiedad ThreeDNow Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad ThreeDNow
topic_type:
- apiref
api_name:
- IVMHostInfo.ThreeDNow
- IVMHostInfo.get_ThreeDNow
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76737b9512e42aef5549985e3ec38953ef02d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698152"
---
# <a name="ivmhostinfothreednow-property"></a><span data-ttu-id="b67c0-107">IVMHostInfo:: ThreeDNow (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b67c0-107">IVMHostInfo::ThreeDNow property</span></span>

<span data-ttu-id="b67c0-108">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b67c0-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b67c0-109">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b67c0-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b67c0-110">Determina si el procesador admite el conjunto de instrucciones 3DNow.</span><span class="sxs-lookup"><span data-stu-id="b67c0-110">Determines whether the processor supports the 3DNow instruction set.</span></span>

<span data-ttu-id="b67c0-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b67c0-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b67c0-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b67c0-112">Syntax</span></span>


```C++
HRESULT get_ThreeDNow(
  [out, retval] VARIANT_BOOL *threeDNowEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="b67c0-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b67c0-113">Property value</span></span>

<span data-ttu-id="b67c0-114">**True** si el procesador del host admite instrucciones 3DNow; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="b67c0-114">**TRUE** if 3DNow instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b67c0-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b67c0-115">Error codes</span></span>



| <span data-ttu-id="b67c0-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="b67c0-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b67c0-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b67c0-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b67c0-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b67c0-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b67c0-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b67c0-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b67c0-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b67c0-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b67c0-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="b67c0-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b67c0-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b67c0-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b67c0-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b67c0-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b67c0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b67c0-124">Requirements</span></span>



| <span data-ttu-id="b67c0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b67c0-125">Requirement</span></span> | <span data-ttu-id="b67c0-126">Value</span><span class="sxs-lookup"><span data-stu-id="b67c0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b67c0-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b67c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b67c0-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b67c0-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b67c0-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b67c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b67c0-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b67c0-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b67c0-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b67c0-131">End of client support</span></span><br/>    | <span data-ttu-id="b67c0-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b67c0-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b67c0-133">Producto</span><span class="sxs-lookup"><span data-stu-id="b67c0-133">Product</span></span><br/>                  | <span data-ttu-id="b67c0-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b67c0-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b67c0-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b67c0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b67c0-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b67c0-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b67c0-137">IID</span><span class="sxs-lookup"><span data-stu-id="b67c0-137">IID</span></span><br/>                      | <span data-ttu-id="b67c0-138">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="b67c0-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b67c0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b67c0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67c0-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="b67c0-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

