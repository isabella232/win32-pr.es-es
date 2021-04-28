---
description: 'Método ID3DXBaseEffect::SetMatrixArray: establece una matriz de matrices no transaccionadas.'
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: Método ID3DXBaseEffect::SetMatrixArray (D3DX9Shader.h)
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
ms.openlocfilehash: ae603708be4b34c9aa12722fe282df470c85d476
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107433"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="0796f-103">Método ID3DXBaseEffect::SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="0796f-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="0796f-104">Establece una matriz de matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="0796f-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0796f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0796f-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="0796f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0796f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0796f-107">*hParameter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0796f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0796f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0796f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0796f-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="0796f-109">Unique identifier.</span></span> <span data-ttu-id="0796f-110">Vea [Identificadores (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="0796f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0796f-111">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0796f-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0796f-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0796f-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0796f-113">Matriz de matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="0796f-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="0796f-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="0796f-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0796f-115">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0796f-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0796f-116">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0796f-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0796f-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0796f-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0796f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0796f-118">Return value</span></span>

<span data-ttu-id="0796f-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0796f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0796f-120">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0796f-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0796f-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0796f-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0796f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0796f-122">Remarks</span></span>

<span data-ttu-id="0796f-123">Una matriz no transaccional contiene datos principales de fila; es decir, cada vector está contenido en una fila.</span><span class="sxs-lookup"><span data-stu-id="0796f-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="0796f-124">Si las matrices de destino son menores que las matrices de origen, se omitirán los componentes adicionales de las matrices de origen.</span><span class="sxs-lookup"><span data-stu-id="0796f-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0796f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0796f-125">Requirements</span></span>



| <span data-ttu-id="0796f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0796f-126">Requirement</span></span> | <span data-ttu-id="0796f-127">Value</span><span class="sxs-lookup"><span data-stu-id="0796f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0796f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0796f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0796f-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="0796f-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0796f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0796f-130">Library</span></span><br/> | <dl> <span data-ttu-id="0796f-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0796f-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0796f-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0796f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0796f-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0796f-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0796f-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="0796f-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
