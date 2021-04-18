---
title: Método ID3DX12PipelineParserCallbacks RTVFormatsCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Método RTVFormatsCb
- Método RTVFormatsCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método RTVFormatsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caaa1df508e1a448de3851d408f9aad5ac94d957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718334"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a><span data-ttu-id="b2fcb-106">ID3DX12PipelineParserCallbacks:: RTVFormatsCb (método)</span><span class="sxs-lookup"><span data-stu-id="b2fcb-106">ID3DX12PipelineParserCallbacks::RTVFormatsCb method</span></span>

<span data-ttu-id="b2fcb-107">Llama a la devolución de llamada de subobjeto de matriz de formato de destino de representación de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b2fcb-107">Calls the render target format array subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2fcb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2fcb-108">Syntax</span></span>


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a><span data-ttu-id="b2fcb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2fcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2fcb-110">*RTVFormats* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="b2fcb-110">*RTVFormats* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fcb-111">Type: **const [**D3D12 \_ RT \_ format \_ array**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span><span class="sxs-lookup"><span data-stu-id="b2fcb-111">Type: **const [**D3D12\_RT\_FORMAT\_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**</span></span>

<span data-ttu-id="b2fcb-112">Detalles del subobjeto de matriz de formato de destino de representación analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="b2fcb-112">Details of the render target format array subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2fcb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2fcb-113">Return value</span></span>

<span data-ttu-id="b2fcb-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="b2fcb-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2fcb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2fcb-115">Requirements</span></span>



| <span data-ttu-id="b2fcb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2fcb-116">Requirement</span></span> | <span data-ttu-id="b2fcb-117">Value</span><span class="sxs-lookup"><span data-stu-id="b2fcb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2fcb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2fcb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b2fcb-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2fcb-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b2fcb-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2fcb-120">Library</span></span><br/> | <dl> <span data-ttu-id="b2fcb-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2fcb-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2fcb-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2fcb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="b2fcb-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2fcb-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2fcb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2fcb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2fcb-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b2fcb-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b2fcb-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="b2fcb-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="b2fcb-127">**\_Matriz de \_ formato D3D12 RT \_**</span><span class="sxs-lookup"><span data-stu-id="b2fcb-127">**D3D12\_RT\_FORMAT\_ARRAY**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





