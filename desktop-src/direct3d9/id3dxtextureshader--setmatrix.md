---
description: 'Método ID3DXTextureShader::SetMatrix: establece una matriz no transpuesta.'
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: Método ID3DXTextureShader::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15ba6b289ad106a8fad4a932b9c5d01e0a52dc18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090223"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="06edb-103">Método ID3DXTextureShader::SetMatrix</span><span class="sxs-lookup"><span data-stu-id="06edb-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="06edb-104">Establece una matriz no transpuesta.</span><span class="sxs-lookup"><span data-stu-id="06edb-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="06edb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06edb-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="06edb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06edb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06edb-107">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="06edb-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06edb-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="06edb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="06edb-109">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="06edb-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="06edb-110">Vea [D3DXHANDLE.](d3dxfx.md)</span><span class="sxs-lookup"><span data-stu-id="06edb-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="06edb-111">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="06edb-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06edb-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="06edb-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="06edb-113">Puntero a una matriz no transpuesta.</span><span class="sxs-lookup"><span data-stu-id="06edb-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="06edb-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="06edb-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06edb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06edb-115">Return value</span></span>

<span data-ttu-id="06edb-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06edb-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06edb-117">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06edb-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06edb-118">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="06edb-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="06edb-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06edb-119">Remarks</span></span>

<span data-ttu-id="06edb-120">Una matriz no transpuesta contiene datos principales de fila; es decir, cada vector está contenido en una fila.</span><span class="sxs-lookup"><span data-stu-id="06edb-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="06edb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06edb-121">Requirements</span></span>



| <span data-ttu-id="06edb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="06edb-122">Requirement</span></span> | <span data-ttu-id="06edb-123">Value</span><span class="sxs-lookup"><span data-stu-id="06edb-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06edb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06edb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="06edb-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="06edb-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="06edb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06edb-126">Library</span></span><br/> | <dl> <span data-ttu-id="06edb-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="06edb-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="06edb-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="06edb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06edb-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="06edb-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




