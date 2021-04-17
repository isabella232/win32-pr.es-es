---
title: Método ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12. h)
description: Llama a la devolución de llamada del subobjeto nodemask de un objeto que implementa esta interfaz.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Método NodemaskCb
- Método NodemaskCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717584"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a><span data-ttu-id="efe72-106">ID3DX12PipelineParserCallbacks:: NodemaskCb (método)</span><span class="sxs-lookup"><span data-stu-id="efe72-106">ID3DX12PipelineParserCallbacks::NodemaskCb method</span></span>

<span data-ttu-id="efe72-107">Llama a la devolución de llamada del subobjeto nodemask de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="efe72-107">Calls the nodemask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe72-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efe72-108">Syntax</span></span>


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a><span data-ttu-id="efe72-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efe72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe72-110">*Nodemask*</span><span class="sxs-lookup"><span data-stu-id="efe72-110">*Nodemask*</span></span> 
</dt> <dd>

<span data-ttu-id="efe72-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="efe72-111">Type: **UINT**</span></span>

<span data-ttu-id="efe72-112">Detalles del subobjeto nodemask analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="efe72-112">Details of the nodemask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe72-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efe72-113">Return value</span></span>

<span data-ttu-id="efe72-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="efe72-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe72-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe72-115">Requirements</span></span>



| <span data-ttu-id="efe72-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe72-116">Requirement</span></span> | <span data-ttu-id="efe72-117">Value</span><span class="sxs-lookup"><span data-stu-id="efe72-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="efe72-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efe72-118">Header</span></span><br/>  | <dl> <span data-ttu-id="efe72-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="efe72-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="efe72-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efe72-120">Library</span></span><br/> | <dl> <span data-ttu-id="efe72-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efe72-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="efe72-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efe72-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="efe72-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe72-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe72-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="efe72-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe72-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="efe72-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="efe72-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="efe72-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





