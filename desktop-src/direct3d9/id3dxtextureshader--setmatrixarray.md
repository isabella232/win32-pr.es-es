---
description: Establece una matriz de matrices no transpuestas.
ms.assetid: 27f230bd-9aee-4673-aa70-5ecda541b1be
title: 'ID3DXTextureShader:: SetMatrixArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b0545d48e16698f44cc48ad467f9454ac94db030
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718235"
---
# <a name="id3dxtextureshadersetmatrixarray-method"></a><span data-ttu-id="0df2b-103">ID3DXTextureShader:: SetMatrixArray (método)</span><span class="sxs-lookup"><span data-stu-id="0df2b-103">ID3DXTextureShader::SetMatrixArray method</span></span>

<span data-ttu-id="0df2b-104">Establece una matriz de matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="0df2b-104">Sets an array of non-transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0df2b-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="0df2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0df2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df2b-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0df2b-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df2b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0df2b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0df2b-109">Identificador único de la matriz de matrices de constantes.</span><span class="sxs-lookup"><span data-stu-id="0df2b-109">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="0df2b-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="0df2b-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="0df2b-111">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0df2b-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df2b-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0df2b-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0df2b-113">Matriz de matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="0df2b-113">Array of non-transposed matrices.</span></span> <span data-ttu-id="0df2b-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0df2b-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0df2b-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0df2b-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df2b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0df2b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0df2b-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0df2b-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df2b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0df2b-118">Return value</span></span>

<span data-ttu-id="0df2b-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0df2b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0df2b-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0df2b-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0df2b-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0df2b-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df2b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0df2b-122">Remarks</span></span>

<span data-ttu-id="0df2b-123">Una matriz no transpuesta contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="0df2b-123">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df2b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0df2b-124">Requirements</span></span>



| <span data-ttu-id="0df2b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df2b-125">Requirement</span></span> | <span data-ttu-id="0df2b-126">Value</span><span class="sxs-lookup"><span data-stu-id="0df2b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df2b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0df2b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0df2b-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df2b-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0df2b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0df2b-129">Library</span></span><br/> | <dl> <span data-ttu-id="0df2b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0df2b-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0df2b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0df2b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df2b-132">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="0df2b-132">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
