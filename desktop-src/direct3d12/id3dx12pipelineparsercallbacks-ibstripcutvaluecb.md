---
title: Método ID3DX12PipelineParserCallbacks IBStripCutValueCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de valor de corte de franja del búfer de índice de un objeto que implementa esta interfaz.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Método IBStripCutValueCb
- Método IBStripCutValueCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método IBStripCutValueCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79fca93e76f43b97ffc8e133594805214fe84cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718340"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a><span data-ttu-id="586cf-106">ID3DX12PipelineParserCallbacks:: IBStripCutValueCb (método)</span><span class="sxs-lookup"><span data-stu-id="586cf-106">ID3DX12PipelineParserCallbacks::IBStripCutValueCb method</span></span>

<span data-ttu-id="586cf-107">Llama a la devolución de llamada de subobjeto de valor de corte de franja del búfer de índice de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="586cf-107">Calls the index buffer strip-cut value subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="586cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="586cf-108">Syntax</span></span>


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a><span data-ttu-id="586cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="586cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="586cf-110">*IBStripCutValue*</span><span class="sxs-lookup"><span data-stu-id="586cf-110">*IBStripCutValue*</span></span> 
</dt> <dd>

<span data-ttu-id="586cf-111">Tipo: **[ **\_ valor de \_ \_ corte de \_ \_ franja de búfer de índice de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span><span class="sxs-lookup"><span data-stu-id="586cf-111">Type: **[**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**</span></span>

<span data-ttu-id="586cf-112">Detalles del subobjeto de valor de corte de franja del búfer de índice analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="586cf-112">Details of the index buffer strip-cut value subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="586cf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="586cf-113">Return value</span></span>

<span data-ttu-id="586cf-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="586cf-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="586cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="586cf-115">Requirements</span></span>



| <span data-ttu-id="586cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="586cf-116">Requirement</span></span> | <span data-ttu-id="586cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="586cf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="586cf-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="586cf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="586cf-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="586cf-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="586cf-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="586cf-120">Library</span></span><br/> | <dl> <span data-ttu-id="586cf-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="586cf-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="586cf-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="586cf-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="586cf-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="586cf-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586cf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="586cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586cf-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="586cf-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="586cf-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="586cf-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="586cf-127">**D3D12 \_ \_ valor de \_ corte de franja de búfer de \_ Índice \_**</span><span class="sxs-lookup"><span data-stu-id="586cf-127">**D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





