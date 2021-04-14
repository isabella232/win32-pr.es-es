---
title: FMA (Corecrt \_ Math. h)
description: Devuelve la suma de multiplicación con fusibles de doble precisión de a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- HLSL de FMA
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422288"
---
# <a name="fma"></a><span data-ttu-id="0f9ac-104">fma</span><span class="sxs-lookup"><span data-stu-id="0f9ac-104">fma</span></span>

<span data-ttu-id="0f9ac-105">Devuelve la suma de multiplicación con fusibles de doble precisión de \* b + c.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="0f9ac-106">*RET* FMA (doble *a*, *b*, *c*);</span><span class="sxs-lookup"><span data-stu-id="0f9ac-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0f9ac-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f9ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f9ac-108"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="0f9ac-109">\[en \] el primer valor de la suma de multiplicación fusionada.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="0f9ac-110"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="0f9ac-111">\[en \] el segundo valor de la suma de multiplicación fusionada.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="0f9ac-112"><span id="c"></span><span id="C"></span>*unidad*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="0f9ac-113">\[en \] el tercer valor de la suma de multiplicación fusionada.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f9ac-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f9ac-114">Return Value</span></span>

<span data-ttu-id="0f9ac-115">Multiplicación de doble precisión fusionada de los parámetros *a* \* *b*  +  *c*.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="0f9ac-116">El valor devuelto debe ser preciso para 0,5 unidades de menos precisión (ULP).</span><span class="sxs-lookup"><span data-stu-id="0f9ac-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f9ac-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f9ac-117">Remarks</span></span>

<span data-ttu-id="0f9ac-118">El intrínseco de **FMA** debe admitir Nan, INF y desnormativas.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="0f9ac-119">Para usar la función intrínseca de **FMA** en el código del sombreador, llame al método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ las opciones de D3D11 D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para comprobar que el dispositivo Direct3D admite la opción de característica [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="0f9ac-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="0f9ac-120">El intrínseco de **FMA** requiere un controlador de pantalla WDDM 1,2, y todos los controladores de pantalla WDDM 1,2 deben ser compatibles con **FMA**.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="0f9ac-121">Si la aplicación crea un dispositivo de representación con el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 y el destino de compilación es Shader Model 5 o posterior, el código fuente HLSL puede usar la función intrínseca de **FMA** .</span><span class="sxs-lookup"><span data-stu-id="0f9ac-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="0f9ac-122">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="0f9ac-122">Type Description</span></span>



| <span data-ttu-id="0f9ac-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="0f9ac-123">Name</span></span>  | [<span data-ttu-id="0f9ac-124">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0f9ac-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0f9ac-126">Tamaño</span><span class="sxs-lookup"><span data-stu-id="0f9ac-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="0f9ac-127">*un*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-127">*a*</span></span>   | <span data-ttu-id="0f9ac-128">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0f9ac-129">**double**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="0f9ac-130">cualquiera</span><span class="sxs-lookup"><span data-stu-id="0f9ac-130">any</span></span>                          |
| <span data-ttu-id="0f9ac-131">*b*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-131">*b*</span></span>   | <span data-ttu-id="0f9ac-132">igual que *la entrada a*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="0f9ac-133">**double**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="0f9ac-134">las mismas dimensiones que *la entrada a*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="0f9ac-135">*c*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-135">*c*</span></span>   | <span data-ttu-id="0f9ac-136">igual que *la entrada a*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="0f9ac-137">**double**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="0f9ac-138">las mismas dimensiones que *la entrada a*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="0f9ac-139">*direcc*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-139">*ret*</span></span> | <span data-ttu-id="0f9ac-140">igual que *la entrada a*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="0f9ac-141">**double**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="0f9ac-142">las mismas dimensiones que *la entrada a*</span><span class="sxs-lookup"><span data-stu-id="0f9ac-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="0f9ac-143">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0f9ac-143">Minimum Shader Model</span></span>

<span data-ttu-id="0f9ac-144">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f9ac-145">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0f9ac-145">Shader Model</span></span>                                                | <span data-ttu-id="0f9ac-146">Compatible</span><span class="sxs-lookup"><span data-stu-id="0f9ac-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="0f9ac-147">Modelo de sombreador 5 o posterior</span><span class="sxs-lookup"><span data-stu-id="0f9ac-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="0f9ac-148">sí</span><span class="sxs-lookup"><span data-stu-id="0f9ac-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="0f9ac-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f9ac-149">Requirements</span></span>



| <span data-ttu-id="0f9ac-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f9ac-150">Requirement</span></span> | <span data-ttu-id="0f9ac-151">Value</span><span class="sxs-lookup"><span data-stu-id="0f9ac-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9ac-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f9ac-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0f9ac-153">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="0f9ac-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="0f9ac-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f9ac-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0f9ac-155">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0f9ac-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="0f9ac-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f9ac-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f9ac-157"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f9ac-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f9ac-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f9ac-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9ac-159">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="0f9ac-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

