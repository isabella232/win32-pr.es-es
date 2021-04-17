---
title: CD3DX12_PIPELINE_STATE_STREAM estructura (D3dx12. h)
description: Una estructura auxiliar para crear y trabajar con los Estados de canalización de gráficos y proceso a través de una interfaz combinada. Consulte D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC and D3D12 \_ Compute \_ Pipeline \_ State \_ desc. | CD3DX12_PIPELINE_STATE_STREAM estructura (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717612"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="a2bf3-106">\_Estructura de \_ flujo de estado de CANALización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="a2bf3-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="a2bf3-107">Una estructura auxiliar para crear y trabajar con los Estados de canalización de gráficos y proceso a través de una interfaz combinada.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="a2bf3-108">Consulte [**D3D12 \_ Graphics \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ Compute \_ Pipeline \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="a2bf3-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="a2bf3-109">\_ \_ La secuencia de estado de la canalización CD3DX12 \_ admite Windows 10 Creators Update y versiones más recientes, pero no admite las nuevas características de Fall Creators Update, como View Instancing.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="a2bf3-110">Para admitir las características de Fall Creators Update, use [**el \_ Estado de canalización de CD3DX12 \_ \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bf3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2bf3-111">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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



## <a name="members"></a><span data-ttu-id="a2bf3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2bf3-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2bf3-113">**Secuencia de estado de la \_ canalización CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-114">Crea una nueva instancia no inicializada de una secuencia de estado de la \_ canalización CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a2bf3-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-115">**Secuencia de estado de la \_ canalización CD3DX12 \_ \_ (const D3D12 \_ gráfico de estado de \_ canalización, \_ \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-116">Crea una nueva instancia de una secuencia de estado de la \_ canalización CD3DX12 \_ \_ , inicializada con los valores copiados de una estructura de flujo de estado de la **\_ canalización \_ \_ CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="a2bf3-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-117">**\_Secuencia de estado de canalización de CD3DX12 \_ \_ (const D3D12 \_ Estado de canalización de proceso \_ \_ \_ DESC& DESC)**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-118">Crea una nueva instancia de una secuencia de estado de la \_ canalización CD3DX12 \_ \_ , inicializada con los valores copiados de una estructura de flujo de estado de la **\_ canalización \_ \_ CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="a2bf3-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-119">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-120">Devuelve el contenido del objeto de \_ flujo de estado de la canalización CD3DX12 \_ \_ como una \_ \_ estructura DESC de estado de canalización de gráficos D3D12 \_ \_ por valor.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="a2bf3-121">Tenga en cuenta \_ que \_ \_ \_ la descripción del estado de canalización de gráficos D3D12 no incluye el miembro **CS** , por lo que este valor se pierde en la conversión.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-122">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-123">Devuelve el contenido del objeto de \_ flujo de estado de la canalización CD3DX12 \_ \_ como una \_ estructura DESC de estado de la canalización de cálculo D3D12 \_ \_ \_ por valor.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="a2bf3-124">Tenga en cuenta que \_ \_ la descripción del estado de la canalización de proceso de D3D12 \_ \_ no incluye los miembros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** o **SampleMask** , por lo que estos valores se pierden en la conversión.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-125">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-126">Describe las marcas de estado de canalización, que controlan características como "depuración de la herramienta".</span><span class="sxs-lookup"><span data-stu-id="a2bf3-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-127">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-128">Describe la máscara de nodo de estado de canalización, que se usa para identificar los nodos (adaptadores físicos del dispositivo) a los que se aplica el PSO en escenarios de varios adaptadores. cada bit de la máscara corresponde a un solo nodo.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="a2bf3-129">En escenarios de un solo adaptador, establezca este valor en 0.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-130">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-131">Describe la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-132">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-133">Describe el formato de búfer de entrada para la fase de ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-134">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-135">Describe el valor de índice especial del búfer de entrada que indica un corte (discontinuidad) cuando se usa la topología de franja triangular.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-136">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-137">Describe la topología primitiva y su orden.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-138">**VIRTUAL**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-139">Describe el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-141">Describe el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-142">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-143">Describe el búfer de salida de streaming.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-144">**!**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-145">Describe el sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-147">Describe el sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-148">**PS**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-149">Describe el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-151">Describe el sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-152">**BlendState**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-153">Describe el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-154">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-155">Describe el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-156">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-157">Describe el formato de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-158">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-159">Describe el estado del rasterizador.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-160">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-161">Describe los formatos de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-162">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-163">Describe el recuento y la calidad de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-164">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-165">Describe la máscara de ejemplo utilizada con el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="a2bf3-166">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="a2bf3-167">Describe un PSO almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2bf3-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2bf3-168">Remarks</span></span>

<span data-ttu-id="a2bf3-169">La \_ \_ secuencia de estado de la canalización CD3DX12 \_ admite Windows 10 Creators Update y versiones más recientes, pero no admite los tipos de subobjetos agregados en Windows 10 Fall Creators Update, como para la creación de instancias de la vista.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="a2bf3-170">Para admitir los tipos de subobjetos agregados en Fall Creators Update, use el [**\_ Estado de canalización de CD3DX12 \_ \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="a2bf3-171">Las variables de miembro accesibles de esta estructura son todas las definiciones de \_ tipo de la plantilla de subobjeto de flujo de estado de canalización de CD3DX12 \_ \_ \_ , que combina los datos de marcador y tipo de subobjeto en un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="a2bf3-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="a2bf3-172">Estas typedefs son:</span><span class="sxs-lookup"><span data-stu-id="a2bf3-172">Those typedefs are:</span></span>

<span data-ttu-id="a2bf3-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="a2bf3-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a2bf3-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2bf3-174">Requirements</span></span>



| <span data-ttu-id="a2bf3-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2bf3-175">Requirement</span></span> | <span data-ttu-id="a2bf3-176">Value</span><span class="sxs-lookup"><span data-stu-id="a2bf3-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2bf3-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2bf3-177">Header</span></span><br/> | <dl> <span data-ttu-id="a2bf3-178"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2bf3-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2bf3-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2bf3-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2bf3-180">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="a2bf3-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a2bf3-181">**\_Estado de canalización de CD3DX12 \_ \_ STREAM1**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="a2bf3-182">**\_Descripción de \_ Estado de canalización de gráficos de \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="a2bf3-183">**\_Descripción de \_ Estado de canalización de proceso de \_ D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="a2bf3-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





