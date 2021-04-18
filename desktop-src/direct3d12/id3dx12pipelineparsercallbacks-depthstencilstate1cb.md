---
title: Método ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Llama a la \_ devolución de llamada de estado de la galería de símbolos de profundidad (D3D12 Depth \_ stencil \_ DESC1) de un objeto que implementa esta interfaz.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Método DepthStencilState1Cb
- Método DepthStencilState1Cb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707751"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a><span data-ttu-id="8ce31-106">ID3DX12PipelineParserCallbacks::D método epthStencilState1Cb</span><span class="sxs-lookup"><span data-stu-id="8ce31-106">ID3DX12PipelineParserCallbacks::DepthStencilState1Cb method</span></span>

<span data-ttu-id="8ce31-107">Llama a la devolución de llamada de estado de la galería de símbolos de profundidad ([**D3D12 \_ Depth \_ stencil \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="8ce31-107">Calls the depth stencil state ([**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce31-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ce31-108">Syntax</span></span>


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="8ce31-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ce31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce31-110">*DepthStencilState* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="8ce31-110">*DepthStencilState* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce31-111">Tipo: **D3D12 de la galería de símbolos de [**profundidad const \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span><span class="sxs-lookup"><span data-stu-id="8ce31-111">Type: **const [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**</span></span>

<span data-ttu-id="8ce31-112">Detalles del subobjeto de estado de estarcido de profundidad analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="8ce31-112">Details of the depth stencil state subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce31-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ce31-113">Return value</span></span>

<span data-ttu-id="8ce31-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="8ce31-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce31-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ce31-115">Requirements</span></span>



| <span data-ttu-id="8ce31-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ce31-116">Requirement</span></span> | <span data-ttu-id="8ce31-117">Value</span><span class="sxs-lookup"><span data-stu-id="8ce31-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce31-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ce31-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8ce31-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ce31-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="8ce31-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ce31-120">Library</span></span><br/> | <dl> <span data-ttu-id="8ce31-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ce31-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ce31-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ce31-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ce31-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ce31-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce31-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ce31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce31-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8ce31-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8ce31-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="8ce31-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="8ce31-127">**Galería de símbolos de profundidad de D3D12 \_ \_ \_ DESC1**</span><span class="sxs-lookup"><span data-stu-id="8ce31-127">**D3D12\_DEPTH\_STENCIL\_DESC1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





