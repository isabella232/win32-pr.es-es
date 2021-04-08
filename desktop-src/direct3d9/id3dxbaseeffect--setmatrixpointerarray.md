---
description: Establece una matriz de punteros a matrices de nontransposed.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'ID3DXBaseEffect:: SetMatrixPointerArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003760"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="818eb-103">ID3DXBaseEffect:: SetMatrixPointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="818eb-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="818eb-104">Establece una matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="818eb-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="818eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="818eb-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="818eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="818eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="818eb-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="818eb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="818eb-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="818eb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="818eb-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="818eb-109">Unique identifier.</span></span> <span data-ttu-id="818eb-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="818eb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="818eb-111">*ppMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="818eb-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="818eb-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="818eb-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="818eb-113">Matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="818eb-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="818eb-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="818eb-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="818eb-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="818eb-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="818eb-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="818eb-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="818eb-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="818eb-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="818eb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="818eb-118">Return value</span></span>

<span data-ttu-id="818eb-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="818eb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="818eb-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="818eb-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="818eb-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="818eb-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="818eb-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="818eb-122">Remarks</span></span>

<span data-ttu-id="818eb-123">Una matriz nontransposed contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="818eb-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="818eb-124">Si las matrices de destino son más pequeñas que las matrices de origen, se omitirán los componentes adicionales de las matrices de origen.</span><span class="sxs-lookup"><span data-stu-id="818eb-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="818eb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="818eb-125">Requirements</span></span>



| <span data-ttu-id="818eb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="818eb-126">Requirement</span></span> | <span data-ttu-id="818eb-127">Value</span><span class="sxs-lookup"><span data-stu-id="818eb-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="818eb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="818eb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="818eb-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="818eb-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="818eb-130">Library</span></span><br/> | <dl> <span data-ttu-id="818eb-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="818eb-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="818eb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="818eb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="818eb-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="818eb-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="818eb-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="818eb-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
