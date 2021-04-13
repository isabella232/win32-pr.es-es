---
description: Establece una matriz de matrices nontransposed.
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: 'ID3DXBaseEffect:: SetMatrixArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c48dcb3288930a9170c932f335a4b20c258acbb4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362420"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="8fd29-103">ID3DXBaseEffect:: SetMatrixArray (método)</span><span class="sxs-lookup"><span data-stu-id="8fd29-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="8fd29-104">Establece una matriz de matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="8fd29-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fd29-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="8fd29-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fd29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fd29-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fd29-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fd29-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8fd29-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8fd29-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="8fd29-109">Unique identifier.</span></span> <span data-ttu-id="8fd29-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8fd29-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd29-111">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fd29-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fd29-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fd29-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8fd29-113">Matriz de matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="8fd29-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="8fd29-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="8fd29-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd29-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fd29-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fd29-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fd29-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fd29-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8fd29-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fd29-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fd29-118">Return value</span></span>

<span data-ttu-id="8fd29-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fd29-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fd29-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8fd29-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8fd29-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8fd29-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fd29-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fd29-122">Remarks</span></span>

<span data-ttu-id="8fd29-123">Una matriz nontransposed contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="8fd29-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="8fd29-124">Si las matrices de destino son más pequeñas que las matrices de origen, se omitirán los componentes adicionales de las matrices de origen.</span><span class="sxs-lookup"><span data-stu-id="8fd29-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd29-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fd29-125">Requirements</span></span>



| <span data-ttu-id="8fd29-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd29-126">Requirement</span></span> | <span data-ttu-id="8fd29-127">Value</span><span class="sxs-lookup"><span data-stu-id="8fd29-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd29-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fd29-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8fd29-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fd29-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8fd29-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8fd29-130">Library</span></span><br/> | <dl> <span data-ttu-id="8fd29-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fd29-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8fd29-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fd29-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd29-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8fd29-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8fd29-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="8fd29-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
