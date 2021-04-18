---
title: Método ID3DX12PipelineParserCallbacks VSCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto del sombreador de vértices de un objeto que implementa esta interfaz.
ms.assetid: 65A185B7-C790-4254-A3C5-EBBE9C38CA4E
keywords:
- Método VSCb
- Método VSCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método VSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.VSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef9ab27b2f9fd4b93190e2eea453397de297013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718333"
---
# <a name="id3dx12pipelineparsercallbacksvscb-method"></a><span data-ttu-id="b1887-106">ID3DX12PipelineParserCallbacks:: VSCb (método)</span><span class="sxs-lookup"><span data-stu-id="b1887-106">ID3DX12PipelineParserCallbacks::VSCb method</span></span>

<span data-ttu-id="b1887-107">Llama a la devolución de llamada de subobjeto del sombreador de vértices de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b1887-107">Calls the vertex shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1887-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1887-108">Syntax</span></span>


```C++
void VSCb(
  [ref] const D3D12_SHADER_BYTECODE &VS
);
```



## <a name="parameters"></a><span data-ttu-id="b1887-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1887-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1887-110">*Vs* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="b1887-110">*VS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b1887-111">Tipo: **const [**D3D12 \_ código de \_ byte del sombreador**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="b1887-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="b1887-112">Detalles del subobjeto del sombreador de vértices analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="b1887-112">Details of the vertex shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1887-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1887-113">Return value</span></span>

<span data-ttu-id="b1887-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="b1887-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1887-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1887-115">Requirements</span></span>



| <span data-ttu-id="b1887-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1887-116">Requirement</span></span> | <span data-ttu-id="b1887-117">Value</span><span class="sxs-lookup"><span data-stu-id="b1887-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1887-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1887-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b1887-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1887-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1887-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1887-120">Library</span></span><br/> | <dl> <span data-ttu-id="b1887-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1887-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1887-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1887-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1887-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1887-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1887-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1887-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1887-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b1887-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b1887-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b1887-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b1887-127">**\_Código de bytes del sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b1887-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





