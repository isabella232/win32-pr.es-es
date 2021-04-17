---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de estado de estarcido de profundidad de un objeto que implementa esta interfaz.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
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
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698182"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a><span data-ttu-id="27e75-106">Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)</span><span class="sxs-lookup"><span data-stu-id="27e75-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h)</span></span>

<span data-ttu-id="27e75-107">Llama a la devolución de llamada de subobjeto de estado de estarcido de profundidad de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="27e75-107">Calls the depth stencil state subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e75-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27e75-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="27e75-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27e75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27e75-110">*DepthStencilState* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="27e75-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="27e75-111">Tipo: **D3D12 de la [**Galería de \_ \_ símbolos \_ de profundidad**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) const**</span><span class="sxs-lookup"><span data-stu-id="27e75-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**</span></span>

<span data-ttu-id="27e75-112">Detalles del subobjeto de estado de estarcido de profundidad analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="27e75-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27e75-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27e75-113">Return value</span></span>

<span data-ttu-id="27e75-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="27e75-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="27e75-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27e75-115">Requirements</span></span>



| <span data-ttu-id="27e75-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27e75-116">Requirement</span></span> | <span data-ttu-id="27e75-117">Value</span><span class="sxs-lookup"><span data-stu-id="27e75-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27e75-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27e75-118">Header</span></span><br/>  | <dl> <span data-ttu-id="27e75-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="27e75-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="27e75-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27e75-120">Library</span></span><br/> | <dl> <span data-ttu-id="27e75-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27e75-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="27e75-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27e75-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="27e75-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27e75-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e75-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="27e75-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e75-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="27e75-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="27e75-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="27e75-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="27e75-127">**D3D12 de la \_ Galería de símbolos de profundidad \_ \_**</span><span class="sxs-lookup"><span data-stu-id="27e75-127">**D3D12\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





