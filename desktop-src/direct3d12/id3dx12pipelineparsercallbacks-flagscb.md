---
title: Método ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto flags de un objeto que implementa esta interfaz.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Método FlagsCb
- Método FlagsCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718345"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a><span data-ttu-id="6c4da-106">ID3DX12PipelineParserCallbacks:: FlagsCb (método)</span><span class="sxs-lookup"><span data-stu-id="6c4da-106">ID3DX12PipelineParserCallbacks::FlagsCb method</span></span>

<span data-ttu-id="6c4da-107">Llama a la devolución de llamada del subobjeto flags de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6c4da-107">Calls the flags subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4da-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c4da-108">Syntax</span></span>


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="6c4da-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c4da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4da-110">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="6c4da-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4da-111">Tipo: **[ **\_ marcas de \_ estado \_ de canalización de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span><span class="sxs-lookup"><span data-stu-id="6c4da-111">Type: **[**D3D12\_PIPELINE\_STATE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**</span></span>

<span data-ttu-id="6c4da-112">Detalles del subobjeto Flags analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="6c4da-112">Details of the flags subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4da-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c4da-113">Return value</span></span>

<span data-ttu-id="6c4da-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="6c4da-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c4da-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c4da-115">Requirements</span></span>



| <span data-ttu-id="6c4da-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4da-116">Requirement</span></span> | <span data-ttu-id="6c4da-117">Value</span><span class="sxs-lookup"><span data-stu-id="6c4da-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4da-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c4da-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6c4da-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c4da-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6c4da-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c4da-120">Library</span></span><br/> | <dl> <span data-ttu-id="6c4da-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c4da-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c4da-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c4da-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c4da-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c4da-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4da-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c4da-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4da-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6c4da-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6c4da-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="6c4da-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="6c4da-127">**\_Marcas de estado de canalización de D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c4da-127">**D3D12\_PIPELINE\_STATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





