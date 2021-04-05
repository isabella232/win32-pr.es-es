---
title: Propiedad IVMHostInfo Velocidaddeprocesador (VPCCOMInterfaces. h)
description: Velocidad del procesador del host, en megahercios (MHz) o gigahercios (GHz).
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- Propiedad Velocidaddeprocesador Virtual PC
- Propiedad Velocidaddeprocesador Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad Velocidaddeprocesador
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc890392db5f61a7819fa1d4b4a11d2b3de312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078817"
---
# <a name="ivmhostinfoprocessorspeed-property"></a><span data-ttu-id="f4861-106">IVMHostInfo::P propiedad rocessorSpeed</span><span class="sxs-lookup"><span data-stu-id="f4861-106">IVMHostInfo::ProcessorSpeed property</span></span>

<span data-ttu-id="f4861-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4861-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f4861-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f4861-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f4861-109">Recupera la velocidad del procesador del host, en megahercios (MHz) o gigahercios (GHz).</span><span class="sxs-lookup"><span data-stu-id="f4861-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="f4861-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4861-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4861-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4861-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="f4861-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f4861-112">Property value</span></span>

<span data-ttu-id="f4861-113">La velocidad del procesador, en megahercios o gigahercio.</span><span class="sxs-lookup"><span data-stu-id="f4861-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4861-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f4861-114">Error codes</span></span>



| <span data-ttu-id="f4861-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="f4861-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f4861-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f4861-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f4861-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4861-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f4861-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4861-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f4861-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f4861-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f4861-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f4861-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f4861-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f4861-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f4861-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f4861-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f4861-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4861-123">Requirements</span></span>



| <span data-ttu-id="f4861-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4861-124">Requirement</span></span> | <span data-ttu-id="f4861-125">Value</span><span class="sxs-lookup"><span data-stu-id="f4861-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4861-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4861-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f4861-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4861-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4861-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4861-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f4861-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f4861-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f4861-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f4861-130">End of client support</span></span><br/>    | <span data-ttu-id="f4861-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4861-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f4861-132">Producto</span><span class="sxs-lookup"><span data-stu-id="f4861-132">Product</span></span><br/>                  | <span data-ttu-id="f4861-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f4861-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f4861-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4861-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4861-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4861-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f4861-136">IID</span><span class="sxs-lookup"><span data-stu-id="f4861-136">IID</span></span><br/>                      | <span data-ttu-id="f4861-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="f4861-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f4861-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4861-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4861-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="f4861-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

