---
description: 'Método ID3DXTextureShader::SetMatrixTransposePointerArray: establece una matriz de punteros en matrices transpuestas.'
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: Método ID3DXTextureShader::SetMatrixTransposePointerArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 46e04c8c86bd0cdf7acea44872d00ad19f620ee6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090153"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="d23d1-103">Método ID3DXTextureShader::SetMatrixTransposePointerArray</span><span class="sxs-lookup"><span data-stu-id="d23d1-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="d23d1-104">Establece una matriz de punteros para matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="d23d1-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d23d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d23d1-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="d23d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d23d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d23d1-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d23d1-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d23d1-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d23d1-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d23d1-109">Identificador único de la matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="d23d1-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="d23d1-110">Vea [D3DXHANDLE.](d3dxfx.md)</span><span class="sxs-lookup"><span data-stu-id="d23d1-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23d1-111">*ppMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d23d1-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d23d1-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="d23d1-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="d23d1-113">Matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="d23d1-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="d23d1-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d23d1-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d23d1-115">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d23d1-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d23d1-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d23d1-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d23d1-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d23d1-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d23d1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d23d1-118">Return value</span></span>

<span data-ttu-id="d23d1-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d23d1-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d23d1-120">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d23d1-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d23d1-121">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d23d1-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d23d1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d23d1-122">Remarks</span></span>

<span data-ttu-id="d23d1-123">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="d23d1-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="d23d1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d23d1-124">Requirements</span></span>



| <span data-ttu-id="d23d1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d23d1-125">Requirement</span></span> | <span data-ttu-id="d23d1-126">Value</span><span class="sxs-lookup"><span data-stu-id="d23d1-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d23d1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d23d1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d23d1-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d23d1-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d23d1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d23d1-129">Library</span></span><br/> | <dl> <span data-ttu-id="d23d1-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d23d1-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d23d1-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d23d1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d23d1-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d23d1-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
