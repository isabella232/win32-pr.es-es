---
description: 'Método ID3DXBaseEffect::SetMatrixPointerArray: establece una matriz de punteros en matrices no transaccionadas.'
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: Método ID3DXBaseEffect::SetMatrixPointerArray (D3DX9Shader.h)
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
ms.openlocfilehash: cfe30e0132cfa237ddbccc24758b35e102a62b0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093773"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a><span data-ttu-id="8bcf4-103">Método ID3DXBaseEffect::SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="8bcf4-103">ID3DXBaseEffect::SetMatrixPointerArray method</span></span>

<span data-ttu-id="8bcf4-104">Establece una matriz de punteros a matrices no transaccionadas.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcf4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bcf4-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="8bcf4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bcf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bcf4-107">*hParameter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8bcf4-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf4-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8bcf4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8bcf4-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-109">Unique identifier.</span></span> <span data-ttu-id="8bcf4-110">Vea [Identificadores (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="8bcf4-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bcf4-111">*ppMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8bcf4-111">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf4-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="8bcf4-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="8bcf4-113">Matriz de punteros a matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="8bcf4-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="8bcf4-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bcf4-115">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8bcf4-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bcf4-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bcf4-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8bcf4-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bcf4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bcf4-118">Return value</span></span>

<span data-ttu-id="8bcf4-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8bcf4-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8bcf4-120">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8bcf4-121">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bcf4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bcf4-122">Remarks</span></span>

<span data-ttu-id="8bcf4-123">Una matriz no transaccional contiene datos principales de fila; es decir, cada vector está contenido en una fila.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="8bcf4-124">Si las matrices de destino son menores que las matrices de origen, se omitirán los componentes adicionales de las matrices de origen.</span><span class="sxs-lookup"><span data-stu-id="8bcf4-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bcf4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bcf4-125">Requirements</span></span>



| <span data-ttu-id="8bcf4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcf4-126">Requirement</span></span> | <span data-ttu-id="8bcf4-127">Value</span><span class="sxs-lookup"><span data-stu-id="8bcf4-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcf4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bcf4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8bcf4-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="8bcf4-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8bcf4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bcf4-130">Library</span></span><br/> | <dl> <span data-ttu-id="8bcf4-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bcf4-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8bcf4-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8bcf4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcf4-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="8bcf4-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="8bcf4-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="8bcf4-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
