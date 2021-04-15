---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) (DSV)
description: Llama a la devoluciones de llamada de subobjeto de formato de valor de estarcido de profundidad de un objeto que implementa esta interfaz.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
keywords:
- Método DepthStencilStateCb
- Método DepthStencilStateCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d26c13c70976c67bbe8d5910c4f3573010ff580
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105709282"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="e9206-106">Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="e9206-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="e9206-107">Llama a la devoluciones de llamada de subobjeto de formato de valor de estarcido de profundidad de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="e9206-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9206-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9206-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="e9206-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9206-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9206-110">*DepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="e9206-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="e9206-111">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e9206-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e9206-112">Detalles del subobjeto de formato de valor de estarcido de profundidad analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="e9206-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9206-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9206-113">Return value</span></span>

<span data-ttu-id="e9206-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="e9206-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9206-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9206-115">Requirements</span></span>



| <span data-ttu-id="e9206-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9206-116">Requirement</span></span> | <span data-ttu-id="e9206-117">Value</span><span class="sxs-lookup"><span data-stu-id="e9206-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e9206-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9206-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e9206-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9206-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e9206-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9206-120">Library</span></span><br/> | <dl> <span data-ttu-id="e9206-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9206-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9206-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9206-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9206-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9206-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9206-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9206-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9206-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e9206-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="e9206-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="e9206-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="e9206-127">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="e9206-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

