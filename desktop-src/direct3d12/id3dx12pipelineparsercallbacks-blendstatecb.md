---
title: Método ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de Descripción del estado de Blend de un objeto que implementa esta interfaz.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Método BlendStateCb
- Método BlendStateCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método BlendStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707981"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a><span data-ttu-id="90142-106">ID3DX12PipelineParserCallbacks:: BlendStateCb (método)</span><span class="sxs-lookup"><span data-stu-id="90142-106">ID3DX12PipelineParserCallbacks::BlendStateCb method</span></span>

<span data-ttu-id="90142-107">Llama a la devolución de llamada de subobjeto de Descripción del estado de Blend de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="90142-107">Calls the blend state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="90142-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90142-108">Syntax</span></span>


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a><span data-ttu-id="90142-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90142-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90142-110">*BlendState* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="90142-110">*BlendState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="90142-111">Tipo: **const [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span><span class="sxs-lookup"><span data-stu-id="90142-111">Type: **const [**D3D12\_BLEND\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**</span></span>

<span data-ttu-id="90142-112">Detalles del subobjeto de Descripción del estado de Blend analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="90142-112">Details of the blend state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90142-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90142-113">Return value</span></span>

<span data-ttu-id="90142-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="90142-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="90142-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90142-115">Requirements</span></span>



| <span data-ttu-id="90142-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="90142-116">Requirement</span></span> | <span data-ttu-id="90142-117">Value</span><span class="sxs-lookup"><span data-stu-id="90142-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90142-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90142-118">Header</span></span><br/>  | <dl> <span data-ttu-id="90142-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="90142-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="90142-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90142-120">Library</span></span><br/> | <dl> <span data-ttu-id="90142-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90142-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="90142-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90142-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="90142-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90142-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90142-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="90142-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90142-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="90142-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="90142-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="90142-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="90142-127">**D3D12 \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="90142-127">**D3D12\_BLEND\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





