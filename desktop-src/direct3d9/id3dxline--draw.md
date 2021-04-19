---
description: Dibuja una franja de líneas en el espacio de la pantalla. La entrada está en forma de una matriz que define los puntos (de D3DXVECTOR2) en la franja de línea.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine::D método RAW (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698378"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="eab95-104">ID3DXLine::D método sin formato</span><span class="sxs-lookup"><span data-stu-id="eab95-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="eab95-105">Dibuja una franja de líneas en el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="eab95-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="eab95-106">La entrada está en forma de una matriz que define los puntos (de [**D3DXVECTOR2**](d3dxvector2.md)) en la franja de línea.</span><span class="sxs-lookup"><span data-stu-id="eab95-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab95-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eab95-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="eab95-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eab95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab95-109">*pVertexList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eab95-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab95-110">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="eab95-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="eab95-111">Matriz de vértices que forman la línea.</span><span class="sxs-lookup"><span data-stu-id="eab95-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="eab95-112">Vea [**D3DXVECTOR2**](d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="eab95-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="eab95-113">*dwVertexListCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eab95-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab95-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eab95-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eab95-115">Número de vértices en la lista de vértices.</span><span class="sxs-lookup"><span data-stu-id="eab95-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="eab95-116">*Color* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="eab95-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab95-117">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="eab95-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="eab95-118">Color de la línea.</span><span class="sxs-lookup"><span data-stu-id="eab95-118">Color of the line.</span></span> <span data-ttu-id="eab95-119">Vea [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="eab95-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab95-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eab95-120">Return value</span></span>

<span data-ttu-id="eab95-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eab95-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eab95-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eab95-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eab95-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="eab95-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab95-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eab95-124">Requirements</span></span>



| <span data-ttu-id="eab95-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab95-125">Requirement</span></span> | <span data-ttu-id="eab95-126">Value</span><span class="sxs-lookup"><span data-stu-id="eab95-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eab95-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eab95-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eab95-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab95-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="eab95-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eab95-129">Library</span></span><br/> | <dl> <span data-ttu-id="eab95-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eab95-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eab95-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="eab95-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab95-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="eab95-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
