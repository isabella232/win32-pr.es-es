---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER estructura (D3dx12. h)
description: Compila un \_ \_ \_ objeto de flujo de estado de canalización CD3DX12 interno a partir de los detalles de subobjeto pasados a las funciones miembro correspondientes. Este struct implementa la interfaz ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698192"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="5d45b-105">\_Estructura de \_ la \_ \_ \_ aplicación auxiliar de análisis de flujo de estado de canalización CD3DX12</span><span class="sxs-lookup"><span data-stu-id="5d45b-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="5d45b-106">Compila un \_ \_ \_ objeto de flujo de estado de canalización CD3DX12 interno a partir de los detalles de subobjeto pasados a las funciones miembro correspondientes.</span><span class="sxs-lookup"><span data-stu-id="5d45b-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="5d45b-107">Este struct implementa la interfaz [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="5d45b-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d45b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d45b-108">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a><span data-ttu-id="5d45b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d45b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d45b-110">**PipelineStream**</span><span class="sxs-lookup"><span data-stu-id="5d45b-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-111">El estado interno de la [**\_ canalización de CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md).</span><span class="sxs-lookup"><span data-stu-id="5d45b-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="5d45b-112">Su estado actual representa el efecto acumulativo de los métodos de devolución de llamada a los que se ha llamado en este objeto.</span><span class="sxs-lookup"><span data-stu-id="5d45b-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-113">**FlagsCb (D3D12 \_ marcas de marcas de estado de canalización \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="5d45b-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-114">Inicializa el miembro **Flags** de **PipelineStream** con el valor del parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-115">**NodeMaskCb (UINT NodeMask)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-116">Inicializa el miembro **NodeMask** de **PipelineStream** con el valor del parámetro *NodeMask* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-117">**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-118">Inicializa el miembro **pRootSignature** de **PipelineStream** con el valor del parámetro *pRootSignature* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-119">**InputLayoutCb (D3D12 de \_ diseño de entrada const \_ \_& InputLayout)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-120">Inicializa el miembro **InputLayout** de **PipelineStream** con el valor del parámetro *InputLayout* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-121">**IBStripCutValueCb (D3D12 \_ valor de corte de la \_ franja del búfer de índice \_ \_ \_ IBStripCutValue)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-122">Inicializa el miembro **IBStripCutValue** de **PipelineStream** con el valor del parámetro *IBStripCutValue* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-123">**PrimitiveTopologyTypeCb ( \_ tipo de \_ topología primitiva D3D12 \_ PrimitiveTopologyType)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-124">Inicializa el miembro **PrimitiveTopologyType** de **PipelineStream** con el valor del parámetro *PrimitiveTopologyType* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-125">**VSCb (D3D12 de \_ código de byte del sombreador const \_& vs)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-126">Inicializa el miembro de **vs** (sombreador de vértices) de **PipelineStream** con el valor del parámetro de *vs* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-127">**GSCb (código de \_ bytes del sombreador const D3D12 \_& GS)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-128">Inicializa el miembro **GS** (sombreador de geometría) de **PipelineStream** con el valor del parámetro *GS* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-129">**StreamOutputCb (D3D12 de \_ salida de flujo const \_ \_& StreamOutput)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-130">Inicializa el miembro **StreamOutput** de **PipelineStream** con el valor del parámetro *StreamOutput* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-131">**HSCb (D3D12 de \_ código de \_ byte del sombreador const& HS)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-132">Inicializa el miembro **HS** (sombreador de casco) de **PipelineStream** con el valor del parámetro *HS* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-133">**DSCb (D3D12 de \_ código de \_ byte del sombreador const& DS)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-134">Inicializa el miembro **DS** (sombreador de dominios) de **PipelineStream** con el valor del parámetro *DS* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-135">**PSCb (el \_ código de bytes del sombreador const D3D12 \_& PS)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-136">Inicializa el miembro **PS** (sombreador de píxeles) de **PipelineStream** con el valor del parámetro *PS* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-137">**CSCb (constante de \_ bytes de sombreador const D3D12 \_& CS)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-138">Inicializa el miembro **CS** de **PipelineStream** con el valor del parámetro *CS* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-139">**BlendStateCb (const D3D12 \_ BLEND \_& BlendState)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-140">Inicializa el miembro **BlendState** de **PipelineStream** con el valor del parámetro *BlendState* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-141">**DepthStencilStateCb (const D3D12 \_ Depth \_ estarcido \_ DESC& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-142">Inicializa el miembro **DepthStencilState** de **PipelineStream** con el valor del parámetro *DepthStencilState* , una descripción de [**la \_ Galería \_ de \_ símbolos de profundidad D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span><span class="sxs-lookup"><span data-stu-id="5d45b-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-143">**DepthStencilState1Cb (const D3D12 \_ Depth \_ STENCIL \_ DESC1& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-144">Inicializa el miembro **DepthStencilState** de **PipelineStream** con el valor del parámetro *DepthStencilState* , una galería de [**símbolos de \_ profundidad D3D12 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span><span class="sxs-lookup"><span data-stu-id="5d45b-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-145">**DSVFormatCb (formato de DXGI \_ DSVFormat)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-146">Inicializa el miembro **DSVFormat** de **PipelineStream** con el valor del parámetro *DSVFormat* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-147">**RasterizerStateCb (const D3D12 \_ rasterizador \_ DESC& RasterizerState)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-148">Inicializa el miembro **RasterizerState** de **PipelineStream** con el valor del parámetro *RasterizerState* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-149">**RTVFormatsCb (matriz de \_ formato const D3D12 RT \_ \_& RTVFormats)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-150">Inicializa el miembro **RTVFormats** de **PipelineStream** con el valor del parámetro *RTVFormats* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-151">**SampleDescCb (ejemplo const de DXGI \_ \_& SampleDesc)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-152">Inicializa el miembro **SampleDesc** de **PipelineStream** con el valor del parámetro *SampleDesc* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-153">**SampleMaskCb (UINT SampleMask)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-154">Inicializa el miembro **SampleMask** de **PipelineStream** con el valor del parámetro *SampleMask* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-155">**ViewInstancingCb (const D3D12 \_ View \_ INSTANCING \_ DESC& ViewInstancingDesc)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-156">Inicializa el miembro **ViewInstancingDesc** de **PipelineStream** con el valor del parámetro *ViewInstancingDesc* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-157">**CachedPSOCb (const D3D12 \_ Estado de \_ canalización en caché \_& CachedPSO)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-158">Inicializa el miembro **CachedPSO** de **PipelineStream** con el valor del parámetro *CachedPSO* .</span><span class="sxs-lookup"><span data-stu-id="5d45b-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-159">**ErrorBadInputParameter (UINT)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-160">No hace nada.</span><span class="sxs-lookup"><span data-stu-id="5d45b-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-161">**ErrorDuplicateSubobject ( \_ tipo de \_ subobjeto de estado de canalización D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="5d45b-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-162">No hace nada.</span><span class="sxs-lookup"><span data-stu-id="5d45b-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="5d45b-163">**ErrorUnknownSubobject (UINT)**</span><span class="sxs-lookup"><span data-stu-id="5d45b-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="5d45b-164">No hace nada.</span><span class="sxs-lookup"><span data-stu-id="5d45b-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d45b-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d45b-165">Remarks</span></span>

<span data-ttu-id="5d45b-166">Cuando se pasa como el segundo parámetro a la función [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , los detalles del objeto [**\_ STREAM1 de \_ estado \_ de canalización CD3DX12**](cd3dx12-pipeline-state-stream1.md) interno se clonan desde la [**DESC de flujo de \_ Estado de canalización \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) pasada como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="5d45b-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="5d45b-167">Este proceso valida la descripción del flujo de origen.</span><span class="sxs-lookup"><span data-stu-id="5d45b-167">This process validates the source stream description.</span></span> <span data-ttu-id="5d45b-168">Si D3DX12ParsePipelineStream devuelve **S \_ OK**, la descripción de la secuencia de origen y el **\_ Estado de canalización CD3DX12 resultante \_ \_ STREAM1PipelineStream** son válidos; de lo contrario, ambos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="5d45b-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="5d45b-169">Los flujos no válidos y otros errores solo se muestran a través del valor devuelto de D3DX12ParsePipelineStream; Esta estructura implementa las devoluciones de llamada de error para no hacer nada.</span><span class="sxs-lookup"><span data-stu-id="5d45b-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d45b-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d45b-170">Requirements</span></span>



| <span data-ttu-id="5d45b-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d45b-171">Requirement</span></span> | <span data-ttu-id="5d45b-172">Value</span><span class="sxs-lookup"><span data-stu-id="5d45b-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d45b-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d45b-173">Header</span></span><br/> | <dl> <span data-ttu-id="5d45b-174"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d45b-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d45b-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d45b-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d45b-176">Estructuras auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5d45b-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5d45b-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5d45b-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





