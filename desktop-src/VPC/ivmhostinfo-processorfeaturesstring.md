---
title: Propiedad IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces. h)
description: Recupera las características de lista que admite el procesador del host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Propiedad ProcessorFeaturesString Virtual PC
- Propiedad ProcessorFeaturesString Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676549"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="ea845-106">IVMHostInfo::P propiedad rocessorFeaturesString</span><span class="sxs-lookup"><span data-stu-id="ea845-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="ea845-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ea845-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ea845-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ea845-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ea845-109">Recupera las características de lista que admite el procesador del host.</span><span class="sxs-lookup"><span data-stu-id="ea845-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="ea845-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ea845-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea845-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea845-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="ea845-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ea845-112">Property value</span></span>

<span data-ttu-id="ea845-113">Una lista delimitada por comas de características.</span><span class="sxs-lookup"><span data-stu-id="ea845-113">A comma-delimited list of features.</span></span> <span data-ttu-id="ea845-114">Un ejemplo sería "MMX, SSE, SSE2, x86-64".</span><span class="sxs-lookup"><span data-stu-id="ea845-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="ea845-115">Value</span><span class="sxs-lookup"><span data-stu-id="ea845-115">Value</span></span>                                                                                 | <span data-ttu-id="ea845-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ea845-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea845-117"><dt>"AMD-V"</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="ea845-118">Es compatible con las extensiones de virtualización de AMD.</span><span class="sxs-lookup"><span data-stu-id="ea845-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="ea845-119"><dt>"Intel VT"</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="ea845-120">Es compatible con las extensiones de tecnología de virtualización de Intel.</span><span class="sxs-lookup"><span data-stu-id="ea845-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="ea845-121"><dt>"HAVD"</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="ea845-122">La virtualización asistida por hardware está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="ea845-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="ea845-123"><dt>Has</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="ea845-124">La virtualización asistida por hardware está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ea845-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="ea845-125"><dt>MMX</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="ea845-126">Es compatible con las extensiones MMX.</span><span class="sxs-lookup"><span data-stu-id="ea845-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="ea845-127"><dt>SSE</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="ea845-128">Admite las extensiones SIMD de streaming.</span><span class="sxs-lookup"><span data-stu-id="ea845-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="ea845-129"><dt>DICHAS</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="ea845-130">Admite las extensiones SIMD de streaming 2.</span><span class="sxs-lookup"><span data-stu-id="ea845-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="ea845-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="ea845-132">Admite las extensiones SIMD de streaming 3.</span><span class="sxs-lookup"><span data-stu-id="ea845-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="ea845-133"><dt>"TXTE"</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="ea845-134">Es compatible con las extensiones de tecnología de ejecución de confianza.</span><span class="sxs-lookup"><span data-stu-id="ea845-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="ea845-135"><dt>"x86-64"</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="ea845-136">Admite extensiones x86-64.</span><span class="sxs-lookup"><span data-stu-id="ea845-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="ea845-137">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ea845-137">Error codes</span></span>



| <span data-ttu-id="ea845-138">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="ea845-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ea845-139">Significado</span><span class="sxs-lookup"><span data-stu-id="ea845-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ea845-140"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ea845-141">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ea845-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ea845-142"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ea845-143">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ea845-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ea845-144"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ea845-145">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ea845-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ea845-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea845-146">Requirements</span></span>



| <span data-ttu-id="ea845-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea845-147">Requirement</span></span> | <span data-ttu-id="ea845-148">Value</span><span class="sxs-lookup"><span data-stu-id="ea845-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea845-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea845-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ea845-150">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea845-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea845-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea845-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ea845-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ea845-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ea845-153">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ea845-153">End of client support</span></span><br/>    | <span data-ttu-id="ea845-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea845-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ea845-155">Producto</span><span class="sxs-lookup"><span data-stu-id="ea845-155">Product</span></span><br/>                  | <span data-ttu-id="ea845-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ea845-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ea845-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea845-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea845-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea845-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ea845-159">IID</span><span class="sxs-lookup"><span data-stu-id="ea845-159">IID</span></span><br/>                      | <span data-ttu-id="ea845-160">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="ea845-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ea845-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea845-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea845-162">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="ea845-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

