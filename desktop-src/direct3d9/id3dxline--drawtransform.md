---
description: Dibuja una franja de líneas en el espacio de la pantalla con una matriz de transformación de entrada especificada.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: ID3DXLine::D método rawTransform (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698377"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="8b5c8-103">ID3DXLine::D método rawTransform</span><span class="sxs-lookup"><span data-stu-id="8b5c8-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="8b5c8-104">Dibuja una franja de líneas en el espacio de la pantalla con una matriz de transformación de entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b5c8-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="8b5c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b5c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5c8-107">*pVertexList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b5c8-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c8-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b5c8-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8b5c8-109">Matriz de vértices que forman la línea.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="8b5c8-110">Vea [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b5c8-111">*dwVertexListCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b5c8-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c8-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5c8-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b5c8-113">Número de vértices en la lista de vértices.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="8b5c8-114">*pTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b5c8-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c8-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b5c8-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8b5c8-116">Una matriz de escala, giro y traslación (SRT) para transformar los puntos.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="8b5c8-117">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="8b5c8-118">Si esta matriz es una matriz de proyección, las líneas punteadas se dibujarán con un patrón punteado de perspectiva-correct.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="8b5c8-119">O bien, puede transformar los vértices y usar [**ID3DXLine::D RAW**](id3dxline--draw.md) para dibujar la línea con un patrón punteado de no perspectiva.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="8b5c8-120">*Color* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8b5c8-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5c8-121">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="8b5c8-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="8b5c8-122">Color de la línea.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-122">Color of the line.</span></span> <span data-ttu-id="8b5c8-123">Vea [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c8-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5c8-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b5c8-124">Return value</span></span>

<span data-ttu-id="8b5c8-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b5c8-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b5c8-126">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8b5c8-127">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8b5c8-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5c8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b5c8-128">Requirements</span></span>



| <span data-ttu-id="8b5c8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b5c8-129">Requirement</span></span> | <span data-ttu-id="8b5c8-130">Value</span><span class="sxs-lookup"><span data-stu-id="8b5c8-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5c8-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b5c8-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8b5c8-132"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5c8-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8b5c8-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b5c8-133">Library</span></span><br/> | <dl> <span data-ttu-id="8b5c8-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b5c8-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b5c8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b5c8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5c8-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="8b5c8-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
