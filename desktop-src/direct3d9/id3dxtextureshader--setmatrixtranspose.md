---
description: 'Método ID3DXTextureShader::SetMatrixTranspose: establece una matriz transpuesta.'
ms.assetid: 5339a9de-528f-4404-880b-73964192b766
title: Método ID3DXTextureShader::SetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91216b49dba7fabb25c128f3801d11bfa2fd95c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114303"
---
# <a name="id3dxtextureshadersetmatrixtranspose-method"></a><span data-ttu-id="da515-103">Método ID3DXTextureShader::SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="da515-103">ID3DXTextureShader::SetMatrixTranspose method</span></span>

<span data-ttu-id="da515-104">Establece una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="da515-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="da515-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da515-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="da515-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da515-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da515-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="da515-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da515-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="da515-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="da515-109">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="da515-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="da515-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="da515-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="da515-111">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="da515-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da515-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="da515-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da515-113">Puntero a una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="da515-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="da515-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="da515-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da515-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da515-115">Return value</span></span>

<span data-ttu-id="da515-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da515-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da515-117">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da515-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da515-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="da515-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="da515-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da515-119">Remarks</span></span>

<span data-ttu-id="da515-120">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector se encuentra en una columna.</span><span class="sxs-lookup"><span data-stu-id="da515-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="da515-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da515-121">Requirements</span></span>



| <span data-ttu-id="da515-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="da515-122">Requirement</span></span> | <span data-ttu-id="da515-123">Value</span><span class="sxs-lookup"><span data-stu-id="da515-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da515-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da515-124">Header</span></span><br/>  | <dl> <span data-ttu-id="da515-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="da515-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="da515-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da515-126">Library</span></span><br/> | <dl> <span data-ttu-id="da515-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="da515-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="da515-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="da515-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da515-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="da515-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




