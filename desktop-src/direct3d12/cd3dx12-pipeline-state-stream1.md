---
title: CD3DX12_PIPELINE_STATE_STREAM1 estructura (D3dx12. h)
description: Una estructura auxiliar para crear y trabajar con los Estados de canalización de gráficos y proceso a través de una interfaz combinada. Consulte D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC and D3D12 \_ Compute \_ Pipeline \_ State \_ desc. | CD3DX12_PIPELINE_STATE_STREAM1 estructura (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717611"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a><span data-ttu-id="4e831-106">\_ \_ Estructura STREAM1 de estado de CANALización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4e831-106">CD3DX12\_PIPELINE\_STATE\_STREAM1 structure</span></span>

<span data-ttu-id="4e831-107">Una estructura auxiliar para crear y trabajar con los Estados de canalización de gráficos y proceso a través de una interfaz combinada.</span><span class="sxs-lookup"><span data-stu-id="4e831-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="4e831-108">Consulte [**D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ Compute \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="4e831-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="4e831-109">\_El estado de canalización \_ de CD3DX12 \_ STREAM1 admite Windows 10 Fall Creators Update con nuevas características, como la creación de instancias de la vista.</span><span class="sxs-lookup"><span data-stu-id="4e831-109">CD3DX12\_PIPELINE\_STATE\_STREAM1 supports the Windows 10 Fall Creators Update with new features such as view instancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e831-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e831-110">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a><span data-ttu-id="4e831-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e831-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e831-112">**\_Estado de canalización de CD3DX12 \_ \_ STREAM1 ()**</span><span class="sxs-lookup"><span data-stu-id="4e831-112">**CD3DX12\_PIPELINE\_STATE\_STREAM1()**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-113">Crea una nueva instancia no inicializada de un \_ STREAM1 de estado de canalización CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4e831-113">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-114">**\_Estado de canalización de CD3DX12 \_ \_ STREAM1 (const D3D12 \_ gráfico de estado de \_ canalización \_ \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="4e831-114">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-115">Crea una nueva instancia de un \_ STREAM1 de estado de canalización de CD3DX12 \_ \_ , inicializada con los valores copiados de una estructura de STREAM1 de **\_ \_ estado \_ de canalización de CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="4e831-115">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-116">**\_Estado de canalización de CD3DX12 \_ \_ STREAM1 (const D3D12 \_ Estado de canalización de proceso \_ \_ \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="4e831-116">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-117">Crea una nueva instancia de un \_ STREAM1 de estado de canalización de CD3DX12 \_ \_ , inicializada con los valores copiados de una estructura de STREAM1 de **\_ \_ estado \_ de canalización de CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="4e831-117">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-118">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="4e831-118">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-119">Devuelve el contenido del \_ objeto STREAM1 de estado de la canalización CD3DX12 \_ \_ como una \_ estructura de DESC de estado de canalización de gráficos D3D12 \_ \_ \_ por valor.</span><span class="sxs-lookup"><span data-stu-id="4e831-119">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="4e831-120">Tenga en cuenta \_ que \_ \_ \_ la descripción del estado de canalización de gráficos D3D12 no incluye el miembro **CS** , por lo que este valor se pierde en la conversión.</span><span class="sxs-lookup"><span data-stu-id="4e831-120">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-121">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="4e831-121">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-122">Devuelve el contenido del \_ objeto STREAM1 de estado de la canalización de CD3DX12 \_ \_ como una \_ estructura de DESC de estado de canalización de D3D12 \_ \_ \_ por valor.</span><span class="sxs-lookup"><span data-stu-id="4e831-122">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="4e831-123">Tenga en cuenta que \_ \_ la descripción del estado de la canalización de proceso de D3D12 \_ \_ no incluye los miembros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask** , por lo que estos valores se pierden en la conversión.</span><span class="sxs-lookup"><span data-stu-id="4e831-123">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-124">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="4e831-124">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-125">Describe las marcas de estado de canalización, que controlan características como "depuración de la herramienta".</span><span class="sxs-lookup"><span data-stu-id="4e831-125">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="4e831-126">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="4e831-126">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-127">Describe la máscara de nodo de estado de canalización, que se usa para identificar los nodos (adaptadores físicos del dispositivo) a los que se aplica el PSO en escenarios de varios adaptadores. cada bit de la máscara corresponde a un solo nodo.</span><span class="sxs-lookup"><span data-stu-id="4e831-127">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="4e831-128">En escenarios de un solo adaptador, establezca este valor en 0.</span><span class="sxs-lookup"><span data-stu-id="4e831-128">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-129">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4e831-129">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-130">Describe la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="4e831-130">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-131">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="4e831-131">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-132">Describe el formato de búfer de entrada para la fase de ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4e831-132">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="4e831-133">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="4e831-133">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-134">Describe el valor de índice especial del búfer de entrada que indica un corte (discontinuidad) cuando se usa la topología de franja triangular.</span><span class="sxs-lookup"><span data-stu-id="4e831-134">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-135">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="4e831-135">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-136">Describe la topología primitiva y su orden.</span><span class="sxs-lookup"><span data-stu-id="4e831-136">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-137">**VIRTUAL**</span><span class="sxs-lookup"><span data-stu-id="4e831-137">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-138">Describe el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="4e831-138">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-139">**GS**</span><span class="sxs-lookup"><span data-stu-id="4e831-139">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-140">Describe el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="4e831-140">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-141">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="4e831-141">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-142">Describe el búfer de salida de streaming.</span><span class="sxs-lookup"><span data-stu-id="4e831-142">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-143">**!**</span><span class="sxs-lookup"><span data-stu-id="4e831-143">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-144">Describe el sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="4e831-144">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-145">**DS**</span><span class="sxs-lookup"><span data-stu-id="4e831-145">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-146">Describe el sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="4e831-146">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-147">**PS**</span><span class="sxs-lookup"><span data-stu-id="4e831-147">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-148">Describe el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="4e831-148">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-149">**CS**</span><span class="sxs-lookup"><span data-stu-id="4e831-149">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-150">Describe el sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4e831-150">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-151">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="4e831-151">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-152">Describe el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="4e831-152">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-153">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4e831-153">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-154">Describe el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4e831-154">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-155">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="4e831-155">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-156">Describe el formato de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="4e831-156">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-157">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="4e831-157">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-158">Describe el estado del rasterizador.</span><span class="sxs-lookup"><span data-stu-id="4e831-158">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-159">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="4e831-159">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-160">Describe los formatos de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4e831-160">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-161">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="4e831-161">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-162">Describe el recuento y la calidad de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e831-162">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-163">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="4e831-163">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-164">Describe la máscara de ejemplo utilizada con el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="4e831-164">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4e831-165">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="4e831-165">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="4e831-166">Describe un PSO almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="4e831-166">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e831-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e831-167">Remarks</span></span>

<span data-ttu-id="4e831-168">[**CD3DX12 \_ El \_ \_ flujo de estado de la canalización**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) es compatible con Windows 10 Fall Creators Update, pero no admite los tipos de subobjetos agregados en Windows 10 Fall Creators Update, como para la creación de instancias de la vista.</span><span class="sxs-lookup"><span data-stu-id="4e831-168">[**CD3DX12\_PIPELINE\_STATE\_STREAM**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supports the Windows 10 Fall Creators Update, but doesn't support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="4e831-169">Para admitir los nuevos tipos de subobjeto, use el \_ Estado de canalización de CD3DX12 \_ \_ STREAM1 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4e831-169">To support the new subobject types, use CD3DX12\_PIPELINE\_STATE\_STREAM1 instead.</span></span>

<span data-ttu-id="4e831-170">Las variables de miembro accesibles de esta estructura son todas las definiciones de \_ tipo de la plantilla de subobjeto de flujo de estado de canalización de CD3DX12 \_ \_ \_ , que combina los datos de marcador y tipo de subobjeto en un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="4e831-170">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="4e831-171">Estas typedefs son:</span><span class="sxs-lookup"><span data-stu-id="4e831-171">Those typedefs are:</span></span>

<span data-ttu-id="4e831-172"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="4e831-172"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4e831-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e831-173">Requirements</span></span>



| <span data-ttu-id="4e831-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e831-174">Requirement</span></span> | <span data-ttu-id="4e831-175">Value</span><span class="sxs-lookup"><span data-stu-id="4e831-175">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4e831-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e831-176">Header</span></span><br/> | <dl> <span data-ttu-id="4e831-177"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e831-177"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e831-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e831-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e831-179">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="4e831-179">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4e831-180">**Secuencia de estado de la \_ canalización CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4e831-180">**CD3DX12\_PIPELINE\_STATE\_STREAM**</span></span>](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[<span data-ttu-id="4e831-181">**\_Descripción de \_ Estado de canalización de gráficos de \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4e831-181">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="4e831-182">**\_Descripción de \_ Estado de canalización de proceso de \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4e831-182">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





