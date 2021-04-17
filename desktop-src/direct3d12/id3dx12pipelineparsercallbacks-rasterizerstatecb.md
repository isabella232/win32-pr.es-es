---
title: Método ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de Descripción del estado de rasterizador de un objeto que implementa esta interfaz.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Método RasterizerStateCb
- Método RasterizerStateCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a970e8061ed9199ba5a6a334c7b670218e93936
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718335"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a><span data-ttu-id="bc66d-106">ID3DX12PipelineParserCallbacks:: RasterizerStateCb (método)</span><span class="sxs-lookup"><span data-stu-id="bc66d-106">ID3DX12PipelineParserCallbacks::RasterizerStateCb method</span></span>

<span data-ttu-id="bc66d-107">Llama a la devolución de llamada de subobjeto de Descripción del estado de rasterizador de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="bc66d-107">Calls the rasterizer state description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc66d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc66d-108">Syntax</span></span>


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="bc66d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc66d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc66d-110">*RasterizerState* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="bc66d-110">*RasterizerState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bc66d-111">Tipo: **const [**D3D12 \_ rasterizador \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span><span class="sxs-lookup"><span data-stu-id="bc66d-111">Type: **const [**D3D12\_RASTERIZER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**</span></span>

<span data-ttu-id="bc66d-112">Detalles del subobjeto de descripción de estado de rasterizador analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="bc66d-112">Details of the rasterizer state description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc66d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc66d-113">Return value</span></span>

<span data-ttu-id="bc66d-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="bc66d-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc66d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc66d-115">Requirements</span></span>



| <span data-ttu-id="bc66d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc66d-116">Requirement</span></span> | <span data-ttu-id="bc66d-117">Value</span><span class="sxs-lookup"><span data-stu-id="bc66d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bc66d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc66d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bc66d-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc66d-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="bc66d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc66d-120">Library</span></span><br/> | <dl> <span data-ttu-id="bc66d-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc66d-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc66d-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc66d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc66d-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc66d-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc66d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc66d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc66d-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bc66d-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="bc66d-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="bc66d-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="bc66d-127">**Descripción de D3D12 \_ rasterizador \_**</span><span class="sxs-lookup"><span data-stu-id="bc66d-127">**D3D12\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





