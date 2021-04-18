---
title: Método ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Llama a la devolución de llamada de error de parámetro de entrada incorrecto de un objeto que implementa esta interfaz.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Método ErrorBadInputParameter
- Método ErrorBadInputParameter, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718350"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a><span data-ttu-id="3ce22-106">ID3DX12PipelineParserCallbacks:: ErrorBadInputParameter (método)</span><span class="sxs-lookup"><span data-stu-id="3ce22-106">ID3DX12PipelineParserCallbacks::ErrorBadInputParameter method</span></span>

<span data-ttu-id="3ce22-107">Llama a la devolución de llamada de error de parámetro de entrada incorrecto de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="3ce22-107">Calls the bad input parameter error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce22-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ce22-108">Syntax</span></span>


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a><span data-ttu-id="3ce22-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ce22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce22-110">*ParameterIndex*</span><span class="sxs-lookup"><span data-stu-id="3ce22-110">*ParameterIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="3ce22-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3ce22-111">Type: **UINT**</span></span>

<span data-ttu-id="3ce22-112">La posición del parámetro que contiene una entrada incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3ce22-112">The position of the parameter that contains bad input.</span></span> <span data-ttu-id="3ce22-113">El parámetro situado más a la izquierda está en la posición 1, no en la posición 0.</span><span class="sxs-lookup"><span data-stu-id="3ce22-113">The left-most parameter is at position 1, not position 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce22-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ce22-114">Return value</span></span>

<span data-ttu-id="3ce22-115">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="3ce22-115">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce22-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce22-116">Requirements</span></span>



| <span data-ttu-id="3ce22-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce22-117">Requirement</span></span> | <span data-ttu-id="3ce22-118">Value</span><span class="sxs-lookup"><span data-stu-id="3ce22-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce22-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ce22-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3ce22-120"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce22-120"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="3ce22-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ce22-121">Library</span></span><br/> | <dl> <span data-ttu-id="3ce22-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ce22-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ce22-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ce22-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ce22-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ce22-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce22-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ce22-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce22-126">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3ce22-126">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="3ce22-127">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="3ce22-127">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





