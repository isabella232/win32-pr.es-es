---
title: Método ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto de Descripción del ejemplo de un objeto que implementa esta interfaz.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Método SampleDescCb
- Método SampleDescCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717578"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a><span data-ttu-id="d2a63-106">ID3DX12PipelineParserCallbacks:: SampleDescCb (método)</span><span class="sxs-lookup"><span data-stu-id="d2a63-106">ID3DX12PipelineParserCallbacks::SampleDescCb method</span></span>

<span data-ttu-id="d2a63-107">Llama a la devolución de llamada del subobjeto de Descripción del ejemplo de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d2a63-107">Calls the sample description subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a63-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2a63-108">Syntax</span></span>


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d2a63-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2a63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a63-110">*SampleDesc* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="d2a63-110">*SampleDesc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a63-111">Tipo: **const [**DXGI \_ Sample \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span><span class="sxs-lookup"><span data-stu-id="d2a63-111">Type: **const [**DXGI\_SAMPLE\_DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**</span></span>

<span data-ttu-id="d2a63-112">Detalles del subobjeto de descripción de ejemplo analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="d2a63-112">Details of the sample description subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2a63-113">Return value</span></span>

<span data-ttu-id="d2a63-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="d2a63-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a63-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2a63-115">Requirements</span></span>



| <span data-ttu-id="d2a63-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a63-116">Requirement</span></span> | <span data-ttu-id="d2a63-117">Value</span><span class="sxs-lookup"><span data-stu-id="d2a63-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a63-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2a63-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d2a63-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2a63-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d2a63-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2a63-120">Library</span></span><br/> | <dl> <span data-ttu-id="d2a63-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2a63-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2a63-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2a63-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2a63-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a63-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a63-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2a63-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a63-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d2a63-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="d2a63-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="d2a63-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="d2a63-127">**\_DESC de ejemplo de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="d2a63-127">**DXGI\_SAMPLE\_DESC**</span></span>](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

