---
title: Propiedad IVMHostInfo ProcessorManufacturerString (VPCCOMInterfaces. h)
description: Recupera el fabricante del procesador del host.
ms.assetid: b7f4a03a-184c-4996-8102-994bf7f37e50
keywords:
- Propiedad ProcessorManufacturerString Virtual PC
- Propiedad ProcessorManufacturerString Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad ProcessorManufacturerString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorManufacturerString
- IVMHostInfo.get_ProcessorManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029e64f0a13d84bea118498726893620e058ac83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078816"
---
# <a name="ivmhostinfoprocessormanufacturerstring-property"></a><span data-ttu-id="d8652-106">IVMHostInfo::P propiedad rocessorManufacturerString</span><span class="sxs-lookup"><span data-stu-id="d8652-106">IVMHostInfo::ProcessorManufacturerString property</span></span>

<span data-ttu-id="d8652-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8652-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d8652-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d8652-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d8652-109">Recupera el fabricante del procesador del host.</span><span class="sxs-lookup"><span data-stu-id="d8652-109">Retrieves the manufacturer of the host processor.</span></span>

<span data-ttu-id="d8652-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8652-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8652-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8652-111">Syntax</span></span>


```C++
HRESULT get_ProcessorManufacturerString(
  [out, retval] BSTR *processorManufacturerString
);
```



## <a name="property-value"></a><span data-ttu-id="d8652-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d8652-112">Property value</span></span>

<span data-ttu-id="d8652-113">Fabricante.</span><span class="sxs-lookup"><span data-stu-id="d8652-113">The manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8652-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d8652-114">Error codes</span></span>



| <span data-ttu-id="d8652-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="d8652-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d8652-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d8652-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d8652-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8652-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d8652-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8652-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d8652-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d8652-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d8652-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="d8652-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d8652-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d8652-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d8652-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d8652-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d8652-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8652-123">Requirements</span></span>



| <span data-ttu-id="d8652-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8652-124">Requirement</span></span> | <span data-ttu-id="d8652-125">Value</span><span class="sxs-lookup"><span data-stu-id="d8652-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8652-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8652-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d8652-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8652-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8652-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8652-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d8652-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d8652-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d8652-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d8652-130">End of client support</span></span><br/>    | <span data-ttu-id="d8652-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8652-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d8652-132">Producto</span><span class="sxs-lookup"><span data-stu-id="d8652-132">Product</span></span><br/>                  | <span data-ttu-id="d8652-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d8652-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d8652-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8652-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8652-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8652-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d8652-136">IID</span><span class="sxs-lookup"><span data-stu-id="d8652-136">IID</span></span><br/>                      | <span data-ttu-id="d8652-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="d8652-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d8652-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8652-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8652-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="d8652-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

