---
title: Método ID3DX12PipelineParserCallbacks HSCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto del sombreador de casco de un objeto que implementa esta interfaz.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Método HSCb
- Método HSCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método HSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7d351e0b3827087cb51c38af173badd28d698c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718342"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a><span data-ttu-id="ca810-106">ID3DX12PipelineParserCallbacks:: HSCb (método)</span><span class="sxs-lookup"><span data-stu-id="ca810-106">ID3DX12PipelineParserCallbacks::HSCb method</span></span>

<span data-ttu-id="ca810-107">Llama a la devolución de llamada del subobjeto del sombreador de casco de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="ca810-107">Calls the hull shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca810-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca810-108">Syntax</span></span>


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a><span data-ttu-id="ca810-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca810-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca810-110">*HS* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="ca810-110">*HS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ca810-111">Tipo: **const [**D3D12 \_ código de \_ byte del sombreador**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="ca810-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="ca810-112">Detalles del subobjeto del sombreador de casco analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="ca810-112">Details of the hull shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca810-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca810-113">Return value</span></span>

<span data-ttu-id="ca810-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="ca810-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca810-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca810-115">Requirements</span></span>



| <span data-ttu-id="ca810-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca810-116">Requirement</span></span> | <span data-ttu-id="ca810-117">Value</span><span class="sxs-lookup"><span data-stu-id="ca810-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca810-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca810-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ca810-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca810-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="ca810-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca810-120">Library</span></span><br/> | <dl> <span data-ttu-id="ca810-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca810-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca810-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca810-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca810-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca810-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca810-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca810-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca810-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ca810-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="ca810-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="ca810-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="ca810-127">**\_Código de bytes del sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="ca810-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





