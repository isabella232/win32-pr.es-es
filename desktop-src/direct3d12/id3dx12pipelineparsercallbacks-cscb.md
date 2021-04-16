---
title: Método ID3DX12PipelineParserCallbacks CSCb (D3DX12. h)
description: Llama a la devolución de llamada de subobjeto del sombreador de cálculo de un objeto que implementa esta interfaz.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Método CSCb
- Método CSCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método CSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707979"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a><span data-ttu-id="81426-106">ID3DX12PipelineParserCallbacks:: CSCb (método)</span><span class="sxs-lookup"><span data-stu-id="81426-106">ID3DX12PipelineParserCallbacks::CSCb method</span></span>

<span data-ttu-id="81426-107">Llama a la devolución de llamada de subobjeto del sombreador de cálculo de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="81426-107">Calls the compute shader subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="81426-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81426-108">Syntax</span></span>


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a><span data-ttu-id="81426-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81426-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81426-110">*CS* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="81426-110">*CS* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="81426-111">Tipo: **const [**D3D12 \_ código de \_ byte del sombreador**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span><span class="sxs-lookup"><span data-stu-id="81426-111">Type: **const [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**</span></span>

<span data-ttu-id="81426-112">Detalles del subobjeto del sombreador de cálculo analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="81426-112">Details of the compute shader subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81426-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81426-113">Return value</span></span>

<span data-ttu-id="81426-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="81426-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="81426-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81426-115">Requirements</span></span>



| <span data-ttu-id="81426-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="81426-116">Requirement</span></span> | <span data-ttu-id="81426-117">Value</span><span class="sxs-lookup"><span data-stu-id="81426-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81426-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81426-118">Header</span></span><br/>  | <dl> <span data-ttu-id="81426-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="81426-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="81426-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81426-120">Library</span></span><br/> | <dl> <span data-ttu-id="81426-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81426-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="81426-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81426-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="81426-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81426-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81426-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="81426-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81426-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="81426-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="81426-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="81426-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[<span data-ttu-id="81426-127">**\_Código de bytes del sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="81426-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





