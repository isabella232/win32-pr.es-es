---
title: msad4
description: Compara un valor de referencia de 4 bytes y un valor de origen de 8 bytes y acumula un vector de 4 sumas. Cada suma corresponde a la suma enmascarada de diferencias absolutas de una alineación de bytes diferente entre el valor de referencia y el valor de origen.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- HLSL de msad4
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984143"
---
# <a name="msad4"></a><span data-ttu-id="eb23d-105">msad4</span><span class="sxs-lookup"><span data-stu-id="eb23d-105">msad4</span></span>

<span data-ttu-id="eb23d-106">Compara un valor de referencia de 4 bytes y un valor de origen de 8 bytes y acumula un vector de 4 sumas.</span><span class="sxs-lookup"><span data-stu-id="eb23d-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="eb23d-107">Cada suma corresponde a la suma enmascarada de diferencias absolutas de una alineación de bytes diferente entre el valor de referencia y el valor de origen.</span><span class="sxs-lookup"><span data-stu-id="eb23d-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="eb23d-108">resultado de uint4 = msad4 (referencia uint, origen uint2, acumulación de uint4);</span><span class="sxs-lookup"><span data-stu-id="eb23d-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="eb23d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb23d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb23d-110"><span id="reference"></span><span id="REFERENCE"></span>*referencia*</span><span class="sxs-lookup"><span data-stu-id="eb23d-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="eb23d-111">\[en \] la matriz de referencia de 4 bytes en un valor **uint** .</span><span class="sxs-lookup"><span data-stu-id="eb23d-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="eb23d-112"><span id="source"></span><span id="SOURCE"></span>*fuentes*</span><span class="sxs-lookup"><span data-stu-id="eb23d-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="eb23d-113">\[en \] la matriz de origen de 8 bytes en dos valores de **uint2** .</span><span class="sxs-lookup"><span data-stu-id="eb23d-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="eb23d-114"><span id="accum"></span><span id="ACCUM"></span>*acumulación*</span><span class="sxs-lookup"><span data-stu-id="eb23d-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="eb23d-115">\[en \] un vector de 4 valores.</span><span class="sxs-lookup"><span data-stu-id="eb23d-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="eb23d-116">**msad4** agrega este vector a la suma enmascarada de diferencias absolutas de las diferentes alineaciones de bytes entre el valor de referencia y el valor de origen.</span><span class="sxs-lookup"><span data-stu-id="eb23d-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb23d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb23d-117">Return Value</span></span>

<span data-ttu-id="eb23d-118">Vector de 4 sumas.</span><span class="sxs-lookup"><span data-stu-id="eb23d-118">A vector of 4 sums.</span></span> <span data-ttu-id="eb23d-119">Cada suma corresponde a la suma enmascarada de diferencias absolutas de diferentes alineaciones de bytes entre el valor de referencia y el valor de origen.</span><span class="sxs-lookup"><span data-stu-id="eb23d-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="eb23d-120">**msad4** no incluye una diferencia en la suma si esa diferencia se enmascara (es decir, el byte de referencia es 0).</span><span class="sxs-lookup"><span data-stu-id="eb23d-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb23d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb23d-121">Remarks</span></span>

<span data-ttu-id="eb23d-122">Para usar la función intrínseca **msad4** en el código del sombreador, llame al método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ las opciones D3D11 de la característica D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para comprobar que el dispositivo Direct3D admite la opción de la característica [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="eb23d-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="eb23d-123">La función intrínseca **msad4** requiere un controlador de pantalla WDDM 1,2 y todos los controladores de pantalla WDDM 1,2 deben admitir **msad4**.</span><span class="sxs-lookup"><span data-stu-id="eb23d-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="eb23d-124">Si la aplicación crea un dispositivo de representación con el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 y el destino de compilación es el modelo de sombreador 5 o posterior, el código fuente de HLSL puede usar la función intrínseca **msad4** .</span><span class="sxs-lookup"><span data-stu-id="eb23d-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="eb23d-125">Los valores devueltos solo son precisos hasta 65535.</span><span class="sxs-lookup"><span data-stu-id="eb23d-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="eb23d-126">Si llama a la función intrínseca **msad4** con entradas que pueden dar lugar a valores devueltos mayores que 65535, **msad4** produce resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="eb23d-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="eb23d-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="eb23d-127">Minimum Shader Model</span></span>

<span data-ttu-id="eb23d-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eb23d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb23d-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="eb23d-129">Shader Model</span></span>                                                | <span data-ttu-id="eb23d-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="eb23d-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="eb23d-131">Modelo de sombreador 5 o posterior</span><span class="sxs-lookup"><span data-stu-id="eb23d-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="eb23d-132">sí</span><span class="sxs-lookup"><span data-stu-id="eb23d-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="eb23d-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eb23d-133">Examples</span></span>

<span data-ttu-id="eb23d-134">Este es un ejemplo de cálculo de resultados para **msad4**:</span><span class="sxs-lookup"><span data-stu-id="eb23d-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="eb23d-135">Este es un ejemplo de cómo se puede usar **msad4** para buscar un patrón de referencia en un búfer:</span><span class="sxs-lookup"><span data-stu-id="eb23d-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="eb23d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb23d-136">Requirements</span></span>



| <span data-ttu-id="eb23d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb23d-137">Requirement</span></span> | <span data-ttu-id="eb23d-138">Value</span><span class="sxs-lookup"><span data-stu-id="eb23d-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="eb23d-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb23d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="eb23d-140">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb23d-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="eb23d-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb23d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="eb23d-142">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="eb23d-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb23d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb23d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb23d-144">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="eb23d-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

