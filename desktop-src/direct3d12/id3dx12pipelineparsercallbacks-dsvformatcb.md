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
ms.openlocfilehash: fd40b138c357c143deafffe01252b3c8b3e87cda
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187910"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h-for-depth-stencil-value"></a><span data-ttu-id="0973f-106">Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h) para el valor de la galería de símbolos de profundidad</span><span class="sxs-lookup"><span data-stu-id="0973f-106">ID3DX12PipelineParserCallbacks DepthStencilStateCb method (D3DX12.h) for depth stencil value</span></span>

<span data-ttu-id="0973f-107">Llama a la devoluciones de llamada de subobjeto de formato de valor de estarcido de profundidad de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0973f-107">Calls the depth stencil value format subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0973f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0973f-108">Syntax</span></span>


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="0973f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0973f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0973f-110">*DepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="0973f-110">*DepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="0973f-111">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="0973f-111">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="0973f-112">Detalles del subobjeto de formato de valor de estarcido de profundidad analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="0973f-112">Details of the depth stencil value format subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0973f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0973f-113">Return value</span></span>

<span data-ttu-id="0973f-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="0973f-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0973f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0973f-115">Requirements</span></span>



| <span data-ttu-id="0973f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0973f-116">Requirement</span></span> | <span data-ttu-id="0973f-117">Value</span><span class="sxs-lookup"><span data-stu-id="0973f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0973f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0973f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0973f-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0973f-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="0973f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0973f-120">Library</span></span><br/> | <dl> <span data-ttu-id="0973f-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0973f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="0973f-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0973f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0973f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0973f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0973f-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0973f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0973f-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0973f-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="0973f-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="0973f-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="0973f-127">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="0973f-127">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

