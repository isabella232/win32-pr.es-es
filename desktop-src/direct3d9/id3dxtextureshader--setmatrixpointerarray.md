---
description: Establece una matriz de punteros a matrices no transpuestas.
ms.assetid: 5ad83abd-1895-4838-85b5-c437c23a3d91
title: 'ID3DXTextureShader:: SetMatrixPointerArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bde5250ae8ceeab7522b9df15c99070e9471608
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362498"
---
# <a name="id3dxtextureshadersetmatrixpointerarray-method"></a><span data-ttu-id="5c44f-103">ID3DXTextureShader:: SetMatrixPointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="5c44f-103">ID3DXTextureShader::SetMatrixPointerArray method</span></span>

<span data-ttu-id="5c44f-104">Establece una matriz de punteros a matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="5c44f-104">Sets an array of pointers to non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c44f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c44f-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="5c44f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c44f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c44f-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c44f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c44f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5c44f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5c44f-109">Identificador único de una matriz de matrices de constantes.</span><span class="sxs-lookup"><span data-stu-id="5c44f-109">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="5c44f-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="5c44f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c44f-111">*ppMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c44f-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c44f-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="5c44f-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="5c44f-113">Matriz de punteros a matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="5c44f-113">Array of pointers to non-transposed matrices.</span></span> <span data-ttu-id="5c44f-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5c44f-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c44f-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c44f-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c44f-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c44f-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c44f-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5c44f-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c44f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c44f-118">Return value</span></span>

<span data-ttu-id="5c44f-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c44f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c44f-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c44f-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5c44f-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5c44f-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c44f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c44f-122">Remarks</span></span>

<span data-ttu-id="5c44f-123">Una matriz no transpuesta contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="5c44f-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c44f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c44f-124">Requirements</span></span>



| <span data-ttu-id="5c44f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c44f-125">Requirement</span></span> | <span data-ttu-id="5c44f-126">Value</span><span class="sxs-lookup"><span data-stu-id="5c44f-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c44f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c44f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5c44f-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c44f-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5c44f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c44f-129">Library</span></span><br/> | <dl> <span data-ttu-id="5c44f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c44f-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5c44f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c44f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c44f-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="5c44f-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
