---
description: Establece una matriz de punteros a matrices transpuestas.
ms.assetid: 2b9f1efe-b2ea-416b-a370-202db57b1925
title: 'ID3DXTextureShader:: SetMatrixTransposePointerArray (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: cd7c81dcb0fd9b9354c2536a91abaebfe8e4315b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670239"
---
# <a name="id3dxtextureshadersetmatrixtransposepointerarray-method"></a><span data-ttu-id="95cef-103">ID3DXTextureShader:: SetMatrixTransposePointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="95cef-103">ID3DXTextureShader::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="95cef-104">Establece una matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="95cef-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="95cef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95cef-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="95cef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95cef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95cef-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95cef-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95cef-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="95cef-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="95cef-109">Identificador único de la matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="95cef-109">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="95cef-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="95cef-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="95cef-111">*ppMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95cef-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95cef-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="95cef-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="95cef-113">Matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="95cef-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="95cef-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="95cef-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="95cef-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95cef-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95cef-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95cef-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95cef-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="95cef-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95cef-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95cef-118">Return value</span></span>

<span data-ttu-id="95cef-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95cef-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95cef-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95cef-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95cef-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="95cef-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="95cef-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95cef-122">Remarks</span></span>

<span data-ttu-id="95cef-123">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="95cef-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="95cef-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95cef-124">Requirements</span></span>



| <span data-ttu-id="95cef-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="95cef-125">Requirement</span></span> | <span data-ttu-id="95cef-126">Value</span><span class="sxs-lookup"><span data-stu-id="95cef-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95cef-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95cef-127">Header</span></span><br/>  | <dl> <span data-ttu-id="95cef-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="95cef-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="95cef-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95cef-129">Library</span></span><br/> | <dl> <span data-ttu-id="95cef-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95cef-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="95cef-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="95cef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95cef-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="95cef-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
