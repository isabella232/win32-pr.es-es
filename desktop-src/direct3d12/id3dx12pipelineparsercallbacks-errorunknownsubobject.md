---
title: Método ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Llama a la devolución de llamada de error de subobjeto desconocido de un objeto que implementa esta interfaz.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Método ErrorUnknownSubobject
- Método ErrorUnknownSubobject, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718347"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a><span data-ttu-id="5c4bf-106">ID3DX12PipelineParserCallbacks:: ErrorUnknownSubobject (método)</span><span class="sxs-lookup"><span data-stu-id="5c4bf-106">ID3DX12PipelineParserCallbacks::ErrorUnknownSubobject method</span></span>

<span data-ttu-id="5c4bf-107">Llama a la devolución de llamada de error de subobjeto desconocido de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-107">Calls the unknown subobject error callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c4bf-108">Syntax</span></span>


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a><span data-ttu-id="5c4bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c4bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4bf-110">*UnknownTypeValue*</span><span class="sxs-lookup"><span data-stu-id="5c4bf-110">*UnknownTypeValue*</span></span> 
</dt> <dd>

<span data-ttu-id="5c4bf-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5c4bf-111">Type: **UINT**</span></span>

<span data-ttu-id="5c4bf-112">Tipo de subobjeto no reconocido del subobjeto intentado.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-112">The unrecognized subobject type of the attempted subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4bf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c4bf-113">Return value</span></span>

<span data-ttu-id="5c4bf-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4bf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c4bf-115">Requirements</span></span>



| <span data-ttu-id="5c4bf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c4bf-116">Requirement</span></span> | <span data-ttu-id="5c4bf-117">Value</span><span class="sxs-lookup"><span data-stu-id="5c4bf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4bf-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c4bf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5c4bf-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c4bf-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5c4bf-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c4bf-120">Library</span></span><br/> | <dl> <span data-ttu-id="5c4bf-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c4bf-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c4bf-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c4bf-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c4bf-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c4bf-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c4bf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c4bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4bf-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5c4bf-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5c4bf-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="5c4bf-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





