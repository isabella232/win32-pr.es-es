---
description: 'Método ID3DXTextureShader::SetMatrixTransposeArray: establece una matriz de matrices transpuestas.'
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: Método ID3DXTextureShader::SetMatrixTransposeArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663f49f600c000ff37974c8ecd4da56ba59630d1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090213"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a><span data-ttu-id="bda67-103">Método ID3DXTextureShader::SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="bda67-103">ID3DXTextureShader::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="bda67-104">Establece una matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="bda67-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bda67-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="bda67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bda67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda67-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bda67-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda67-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bda67-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bda67-109">Identificador único de la matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="bda67-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="bda67-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="bda67-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="bda67-111">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bda67-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda67-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bda67-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bda67-113">Matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="bda67-113">Array of transposed matrices.</span></span> <span data-ttu-id="bda67-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="bda67-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="bda67-115">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bda67-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda67-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bda67-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bda67-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="bda67-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda67-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bda67-118">Return value</span></span>

<span data-ttu-id="bda67-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bda67-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bda67-120">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bda67-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bda67-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bda67-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda67-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bda67-122">Remarks</span></span>

<span data-ttu-id="bda67-123">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector se encuentra en una columna.</span><span class="sxs-lookup"><span data-stu-id="bda67-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda67-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bda67-124">Requirements</span></span>



| <span data-ttu-id="bda67-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda67-125">Requirement</span></span> | <span data-ttu-id="bda67-126">Value</span><span class="sxs-lookup"><span data-stu-id="bda67-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda67-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bda67-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bda67-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="bda67-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bda67-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bda67-129">Library</span></span><br/> | <dl> <span data-ttu-id="bda67-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bda67-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bda67-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bda67-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda67-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="bda67-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
