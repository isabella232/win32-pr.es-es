---
title: Método ID3DX12PipelineParserCallbacks RootSignatureCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto de firma raíz de un objeto que implementa esta interfaz.
ms.assetid: FD467001-41B1-4A73-8E54-12C6B5EEAC3E
keywords:
- Método RootSignatureCb
- Método RootSignatureCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método RootSignatureCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RootSignatureCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78160ff1e61432a0711876934215ff15afb918de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717581"
---
# <a name="id3dx12pipelineparsercallbacksrootsignaturecb-method"></a><span data-ttu-id="6ef14-106">ID3DX12PipelineParserCallbacks:: RootSignatureCb (método)</span><span class="sxs-lookup"><span data-stu-id="6ef14-106">ID3DX12PipelineParserCallbacks::RootSignatureCb method</span></span>

<span data-ttu-id="6ef14-107">Llama a la devolución de llamada de subobjeto de firma raíz de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6ef14-107">Calls the root signature subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef14-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ef14-108">Syntax</span></span>


```C++
void RootSignatureCb(
   ID3D12RootSignature *RootSignature
);
```



## <a name="parameters"></a><span data-ttu-id="6ef14-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ef14-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef14-110">*RootSignature*</span><span class="sxs-lookup"><span data-stu-id="6ef14-110">*RootSignature*</span></span> 
</dt> <dd>

<span data-ttu-id="6ef14-111">Tipo: **[ **ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span><span class="sxs-lookup"><span data-stu-id="6ef14-111">Type: **[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)\***</span></span>

<span data-ttu-id="6ef14-112">Detalles del subobjeto de firma raíz analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="6ef14-112">Details of the root signature subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef14-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ef14-113">Return value</span></span>

<span data-ttu-id="6ef14-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="6ef14-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef14-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ef14-115">Requirements</span></span>



| <span data-ttu-id="6ef14-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ef14-116">Requirement</span></span> | <span data-ttu-id="6ef14-117">Value</span><span class="sxs-lookup"><span data-stu-id="6ef14-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef14-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ef14-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6ef14-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ef14-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="6ef14-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ef14-120">Library</span></span><br/> | <dl> <span data-ttu-id="6ef14-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ef14-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ef14-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ef14-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ef14-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef14-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef14-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ef14-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef14-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6ef14-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6ef14-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="6ef14-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="6ef14-127">**ID3D12RootSignature**</span><span class="sxs-lookup"><span data-stu-id="6ef14-127">**ID3D12RootSignature**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> </dl>

 

