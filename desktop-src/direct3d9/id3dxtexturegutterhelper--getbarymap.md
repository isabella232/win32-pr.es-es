---
description: Recupera las coordenadas de Barycentric de textura.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper:: GetBaryMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707950"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="d0d30-103">ID3DXTextureGutterHelper:: GetBaryMap (método)</span><span class="sxs-lookup"><span data-stu-id="d0d30-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="d0d30-104">Recupera las coordenadas de Barycentric de textura.</span><span class="sxs-lookup"><span data-stu-id="d0d30-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0d30-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="d0d30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0d30-107">*pBaryData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d0d30-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d30-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0d30-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0d30-109">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que contiene las dos primeras coordenadas Barycentric de cada textura.</span><span class="sxs-lookup"><span data-stu-id="d0d30-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0d30-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0d30-110">Return value</span></span>

<span data-ttu-id="d0d30-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0d30-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0d30-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0d30-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d0d30-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d0d30-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="d0d30-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0d30-114">Remarks</span></span>

<span data-ttu-id="d0d30-115">La tercera coordenada Barycentric se proporciona mediante:</span><span class="sxs-lookup"><span data-stu-id="d0d30-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="d0d30-116">Las coordenadas Barycentric siempre se especifican con respecto al triángulo devuelto por [**ID3DXTextureGutterHelper:: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span><span class="sxs-lookup"><span data-stu-id="d0d30-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="d0d30-117">Las coordenadas Barycentric devueltas por este método solo son válidas para textura válida (que no es de clase 0).</span><span class="sxs-lookup"><span data-stu-id="d0d30-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="d0d30-118">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para textura válido.</span><span class="sxs-lookup"><span data-stu-id="d0d30-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="d0d30-119">Los [**textura de clase 2**](id3dxtexturegutterhelper.md) se asignan al punto más cercano del triángulo en el espacio textura.</span><span class="sxs-lookup"><span data-stu-id="d0d30-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="d0d30-120">La aplicación debe asignar y administrar pBaryData.</span><span class="sxs-lookup"><span data-stu-id="d0d30-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="d0d30-121">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="d0d30-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="d0d30-122">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="d0d30-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0d30-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0d30-123">Requirements</span></span>



| <span data-ttu-id="d0d30-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0d30-124">Requirement</span></span> | <span data-ttu-id="d0d30-125">Value</span><span class="sxs-lookup"><span data-stu-id="d0d30-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d30-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0d30-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d0d30-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0d30-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d0d30-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0d30-128">Library</span></span><br/> | <dl> <span data-ttu-id="d0d30-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0d30-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0d30-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0d30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0d30-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="d0d30-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




