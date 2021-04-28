---
description: 'Método ID3DXBaseEffect::SetMatrix: establece una matriz no transpuesta.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: Método ID3DXBaseEffect::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097503"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="b7eb0-103">Método ID3DXBaseEffect::SetMatrix</span><span class="sxs-lookup"><span data-stu-id="b7eb0-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="b7eb0-104">Establece una matriz no transpuesta.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7eb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7eb0-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="b7eb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7eb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7eb0-107">*hParameter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b7eb0-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb0-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b7eb0-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-109">Unique identifier.</span></span> <span data-ttu-id="b7eb0-110">Vea [Identificadores (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7eb0-111">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b7eb0-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7eb0-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b7eb0-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b7eb0-113">Puntero a una matriz sin transacciones.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="b7eb0-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb0-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7eb0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7eb0-115">Return value</span></span>

<span data-ttu-id="b7eb0-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7eb0-117">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7eb0-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7eb0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7eb0-119">Remarks</span></span>

<span data-ttu-id="b7eb0-120">Una matriz no transpuesta contiene datos principales de fila.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="b7eb0-121">En otras palabras, cada vector se encuentra en una fila.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="b7eb0-122">Si la matriz de destino es menor que la matriz de origen, se omitirán los componentes adicionales de la matriz de origen.</span><span class="sxs-lookup"><span data-stu-id="b7eb0-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7eb0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7eb0-123">Requirements</span></span>



| <span data-ttu-id="b7eb0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7eb0-124">Requirement</span></span> | <span data-ttu-id="b7eb0-125">Value</span><span class="sxs-lookup"><span data-stu-id="b7eb0-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7eb0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7eb0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b7eb0-127"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb0-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b7eb0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7eb0-128">Library</span></span><br/> | <dl> <span data-ttu-id="b7eb0-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb0-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b7eb0-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7eb0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7eb0-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b7eb0-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b7eb0-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="b7eb0-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




