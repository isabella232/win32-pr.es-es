---
description: Remuestrea un búfer de ID3DXPRTBuffer de entrada y lo guarda en un búfer de salida. Este método se puede usar para convertir un búfer de vértice en un búfer de textura y viceversa. También se puede usar para convertir búferes de canal único en búferes de 3 canales y viceversa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'ID3DXPRTEngine:: ResampleBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821410"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="b080f-105">ID3DXPRTEngine:: ResampleBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="b080f-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="b080f-106">Remuestrea un búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada y lo guarda en un búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b080f-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="b080f-107">Este método se puede usar para convertir un búfer de vértice en un búfer de textura y viceversa.</span><span class="sxs-lookup"><span data-stu-id="b080f-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="b080f-108">También se puede usar para convertir búferes de canal único en búferes de 3 canales y viceversa.</span><span class="sxs-lookup"><span data-stu-id="b080f-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="b080f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b080f-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="b080f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b080f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b080f-111">*pBufferIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b080f-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b080f-112">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b080f-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b080f-113">Puntero al búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="b080f-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b080f-114">*pBufferOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b080f-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b080f-115">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="b080f-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="b080f-116">Puntero al búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="b080f-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b080f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b080f-117">Return value</span></span>

<span data-ttu-id="b080f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b080f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b080f-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b080f-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b080f-120">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b080f-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b080f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b080f-121">Requirements</span></span>



| <span data-ttu-id="b080f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b080f-122">Requirement</span></span> | <span data-ttu-id="b080f-123">Value</span><span class="sxs-lookup"><span data-stu-id="b080f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b080f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b080f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b080f-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b080f-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b080f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b080f-126">Library</span></span><br/> | <dl> <span data-ttu-id="b080f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b080f-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b080f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b080f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b080f-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b080f-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




