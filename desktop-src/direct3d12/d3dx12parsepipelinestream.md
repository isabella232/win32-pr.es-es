---
title: Función D3DX12ParsePipelineStream (D3dx12. h)
description: Analiza una descripción de flujo de estado de canalización, que llama a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- D3DX12ParsePipelineStream función)
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6778c29793f01ff7f1e5fd6424fb6795a29e64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721436"
---
# <a name="d3dx12parsepipelinestream-function"></a><span data-ttu-id="02c72-104">D3DX12ParsePipelineStream función)</span><span class="sxs-lookup"><span data-stu-id="02c72-104">D3DX12ParsePipelineStream function</span></span>

<span data-ttu-id="02c72-105">Analiza una descripción de flujo de estado de canalización, que llama a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.</span><span class="sxs-lookup"><span data-stu-id="02c72-105">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c72-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02c72-106">Syntax</span></span>


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a><span data-ttu-id="02c72-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02c72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c72-108">*DESC* \[ . CLI\]</span><span class="sxs-lookup"><span data-stu-id="02c72-108">*Desc* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="02c72-109">Tipo: **const [**D3D12 de la secuencia de \_ \_ estado \_ \_ de canalización**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span><span class="sxs-lookup"><span data-stu-id="02c72-109">Type: **const [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**</span></span>

<span data-ttu-id="02c72-110">La descripción del flujo de estado de la canalización que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="02c72-110">The pipeline state stream description to parse.</span></span>

</dd> <dt>

<span data-ttu-id="02c72-111">*pCallbacks*</span><span class="sxs-lookup"><span data-stu-id="02c72-111">*pCallbacks*</span></span> 
</dt> <dd>

<span data-ttu-id="02c72-112">Tipo: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span><span class="sxs-lookup"><span data-stu-id="02c72-112">Type: **[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***</span></span>

<span data-ttu-id="02c72-113">Estructura que especifica las devoluciones de llamada que se van a llamar para cada tipo de subobjeto y devoluciones de llamada adicionales que se van a llamar en caso de un error de análisis.</span><span class="sxs-lookup"><span data-stu-id="02c72-113">A structure that specifies the callbacks to call for each subobject type and additional callbacks to call in the event of a parsing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c72-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02c72-114">Return value</span></span>

<span data-ttu-id="02c72-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02c72-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02c72-116">Este método devuelve un error HRESULT Success (**S \_ OK** o **E \_ INVALIDARG** ) si se encuentra un tipo de subobjeto desconocido, si la descripción del flujo está vacía, es null o contiene subobjetos duplicados (incluidos los subobjetos derivados) o si *pCallbacks* es NULL.</span><span class="sxs-lookup"><span data-stu-id="02c72-116">This method returns an HRESULT success (**S\_OK** or **E\_INVALIDARG** error if an unknown subobject type is encountered, if the stream description is empty, null, or contains duplicate subobjects (including derived subobjects), or if *pCallbacks* is null.</span></span> <span data-ttu-id="02c72-117">En cada caso en \_ el que se devuelve E INVALIDARG, primero se llama a una devolución de llamada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="02c72-117">In each case that E\_INVALIDARG is returned, a corresponding callback is first called.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c72-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02c72-118">Requirements</span></span>



| <span data-ttu-id="02c72-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c72-119">Requirement</span></span> | <span data-ttu-id="02c72-120">Value</span><span class="sxs-lookup"><span data-stu-id="02c72-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02c72-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02c72-121">Header</span></span><br/>  | <dl> <span data-ttu-id="02c72-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c72-122"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="02c72-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02c72-123">Library</span></span><br/> | <dl> <span data-ttu-id="02c72-124"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02c72-124"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="02c72-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02c72-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="02c72-126"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02c72-126"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c72-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="02c72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c72-128">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="02c72-128">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





