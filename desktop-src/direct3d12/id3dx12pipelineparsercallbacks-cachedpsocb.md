---
title: Método ID3DX12PipelineParserCallbacks CachedPSOCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto PSO (objeto de estado de canalización) almacenada en caché de un objeto que implementa esta interfaz.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Método CachedPSOCb
- Método CachedPSOCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método CachedPSOCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707980"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a><span data-ttu-id="d207a-106">ID3DX12PipelineParserCallbacks:: CachedPSOCb (método)</span><span class="sxs-lookup"><span data-stu-id="d207a-106">ID3DX12PipelineParserCallbacks::CachedPSOCb method</span></span>

<span data-ttu-id="d207a-107">Llama a la devolución de llamada del subobjeto PSO (objeto de estado de canalización) almacenada en caché de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d207a-107">Calls the cached PSO (Pipeline State Object) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d207a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d207a-108">Syntax</span></span>


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a><span data-ttu-id="d207a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d207a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d207a-110">*CachedPSO* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="d207a-110">*CachedPSO* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d207a-111">Tipo: **const [**D3D12 \_ Estado de \_ la \_ canalización en caché**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span><span class="sxs-lookup"><span data-stu-id="d207a-111">Type: **const [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**</span></span>

<span data-ttu-id="d207a-112">Detalles del subobjeto PSO (objeto de estado de canalización) almacenado en caché analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="d207a-112">Details of the cached PSO (Pipeline State Object) subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d207a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d207a-113">Return value</span></span>

<span data-ttu-id="d207a-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="d207a-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d207a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d207a-115">Requirements</span></span>



| <span data-ttu-id="d207a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d207a-116">Requirement</span></span> | <span data-ttu-id="d207a-117">Value</span><span class="sxs-lookup"><span data-stu-id="d207a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d207a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d207a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d207a-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d207a-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d207a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d207a-120">Library</span></span><br/> | <dl> <span data-ttu-id="d207a-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d207a-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d207a-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d207a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d207a-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d207a-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d207a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d207a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d207a-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d207a-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d207a-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d207a-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d207a-127">**D3D12 \_ Estado de \_ canalización en caché \_**</span><span class="sxs-lookup"><span data-stu-id="d207a-127">**D3D12\_CACHED\_PIPELINE\_STATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





