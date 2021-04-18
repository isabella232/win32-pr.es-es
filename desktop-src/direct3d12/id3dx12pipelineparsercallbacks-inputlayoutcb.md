---
title: Método ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de diseño de entrada de un objeto que implementa esta interfaz.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Método InputLayoutCb
- Método InputLayoutCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc28276ef893247577cf41de8f4aba5582c101d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718337"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a><span data-ttu-id="95b54-106">ID3DX12PipelineParserCallbacks:: InputLayoutCb (método)</span><span class="sxs-lookup"><span data-stu-id="95b54-106">ID3DX12PipelineParserCallbacks::InputLayoutCb method</span></span>

<span data-ttu-id="95b54-107">Llama a la devolución de llamada de subobjeto de diseño de entrada de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="95b54-107">Calls the input layout subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b54-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95b54-108">Syntax</span></span>


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a><span data-ttu-id="95b54-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95b54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b54-110">*InputLayout* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="95b54-110">*InputLayout* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="95b54-111">Tipo: **const [**D3D12 \_ diseño de entrada \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span><span class="sxs-lookup"><span data-stu-id="95b54-111">Type: **const [**D3D12\_INPUT\_LAYOUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**</span></span>

<span data-ttu-id="95b54-112">Detalles del subobjeto de diseño de entrada analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="95b54-112">Details of the input layout subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b54-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95b54-113">Return value</span></span>

<span data-ttu-id="95b54-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="95b54-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b54-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95b54-115">Requirements</span></span>



| <span data-ttu-id="95b54-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b54-116">Requirement</span></span> | <span data-ttu-id="95b54-117">Value</span><span class="sxs-lookup"><span data-stu-id="95b54-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95b54-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95b54-118">Header</span></span><br/>  | <dl> <span data-ttu-id="95b54-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b54-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="95b54-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95b54-120">Library</span></span><br/> | <dl> <span data-ttu-id="95b54-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95b54-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="95b54-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95b54-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="95b54-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b54-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b54-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="95b54-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b54-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95b54-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="95b54-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="95b54-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="95b54-127">**\_Descripción del \_ diseño de entrada de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="95b54-127">**D3D12\_INPUT\_LAYOUT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





