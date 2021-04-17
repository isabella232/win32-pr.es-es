---
title: Método ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de descripción de salida de flujo de un objeto que implementa esta interfaz.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Método StreamOutputCb
- Método StreamOutputCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717576"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a><span data-ttu-id="b5e29-106">ID3DX12PipelineParserCallbacks:: StreamOutputCb (método)</span><span class="sxs-lookup"><span data-stu-id="b5e29-106">ID3DX12PipelineParserCallbacks::StreamOutputCb method</span></span>

<span data-ttu-id="b5e29-107">Llama a la devolución de llamada de subobjeto de descripción de salida de flujo de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b5e29-107">Calls the stream output description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e29-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5e29-108">Syntax</span></span>


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a><span data-ttu-id="b5e29-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5e29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5e29-110">*StreamOutput* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="b5e29-110">*StreamOutput* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b5e29-111">Tipo: **[**D3D12 de \_ \_ salida de \_ flujo**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) const**</span><span class="sxs-lookup"><span data-stu-id="b5e29-111">Type: **const [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**</span></span>

<span data-ttu-id="b5e29-112">Detalles del subobjeto de descripción de salida de flujo analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="b5e29-112">Details of the stream output description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5e29-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5e29-113">Return value</span></span>

<span data-ttu-id="b5e29-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="b5e29-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e29-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5e29-115">Requirements</span></span>



| <span data-ttu-id="b5e29-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5e29-116">Requirement</span></span> | <span data-ttu-id="b5e29-117">Value</span><span class="sxs-lookup"><span data-stu-id="b5e29-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e29-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5e29-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5e29-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5e29-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b5e29-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5e29-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5e29-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5e29-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5e29-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5e29-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5e29-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5e29-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5e29-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5e29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e29-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b5e29-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b5e29-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b5e29-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b5e29-127">**DESC. de \_ salida de flujo D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5e29-127">**D3D12\_STREAM\_OUTPUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





