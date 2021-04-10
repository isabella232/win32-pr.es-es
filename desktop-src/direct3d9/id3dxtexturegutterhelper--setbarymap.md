---
description: Establece las coordenadas de Barycentric de textura.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper:: SetBaryMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280464"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="d2857-103">ID3DXTextureGutterHelper:: SetBaryMap (método)</span><span class="sxs-lookup"><span data-stu-id="d2857-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="d2857-104">Establece las coordenadas de Barycentric de textura.</span><span class="sxs-lookup"><span data-stu-id="d2857-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2857-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2857-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="d2857-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2857-107">*pBaryData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2857-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2857-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2857-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d2857-109">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que contiene las dos primeras coordenadas Barycentric de cada textura.</span><span class="sxs-lookup"><span data-stu-id="d2857-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2857-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2857-110">Return value</span></span>

<span data-ttu-id="d2857-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2857-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2857-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2857-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d2857-113">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d2857-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="d2857-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2857-114">Remarks</span></span>

<span data-ttu-id="d2857-115">La tercera coordenada Barycentric se proporciona mediante:</span><span class="sxs-lookup"><span data-stu-id="d2857-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="d2857-116">El Barycentric coordina la entrada a este método solo es válido para textura válido (que no es de clase 0).</span><span class="sxs-lookup"><span data-stu-id="d2857-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="d2857-117">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para textura válidos.</span><span class="sxs-lookup"><span data-stu-id="d2857-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="d2857-118">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="d2857-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="d2857-119">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="d2857-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2857-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2857-120">Requirements</span></span>



| <span data-ttu-id="d2857-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2857-121">Requirement</span></span> | <span data-ttu-id="d2857-122">Value</span><span class="sxs-lookup"><span data-stu-id="d2857-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2857-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2857-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d2857-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2857-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d2857-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2857-125">Library</span></span><br/> | <dl> <span data-ttu-id="d2857-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2857-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2857-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2857-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2857-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="d2857-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




