---
description: Establece una matriz no transpuesta.
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'ID3DXBaseEffect:: SetMatrix (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547822"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="320e7-103">ID3DXBaseEffect:: SetMatrix (método)</span><span class="sxs-lookup"><span data-stu-id="320e7-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="320e7-104">Establece una matriz no transpuesta.</span><span class="sxs-lookup"><span data-stu-id="320e7-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="320e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="320e7-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="320e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="320e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="320e7-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="320e7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="320e7-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="320e7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="320e7-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="320e7-109">Unique identifier.</span></span> <span data-ttu-id="320e7-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="320e7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="320e7-111">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="320e7-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="320e7-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="320e7-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="320e7-113">Puntero a una matriz nontransposed.</span><span class="sxs-lookup"><span data-stu-id="320e7-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="320e7-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="320e7-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="320e7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="320e7-115">Return value</span></span>

<span data-ttu-id="320e7-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="320e7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="320e7-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="320e7-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="320e7-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="320e7-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="320e7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="320e7-119">Remarks</span></span>

<span data-ttu-id="320e7-120">Una matriz no transpuesta contiene datos principales de fila.</span><span class="sxs-lookup"><span data-stu-id="320e7-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="320e7-121">En otras palabras, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="320e7-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="320e7-122">Si la matriz de destino es menor que la matriz de origen, se omitirán los componentes adicionales de la matriz de origen.</span><span class="sxs-lookup"><span data-stu-id="320e7-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="320e7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="320e7-123">Requirements</span></span>



| <span data-ttu-id="320e7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="320e7-124">Requirement</span></span> | <span data-ttu-id="320e7-125">Value</span><span class="sxs-lookup"><span data-stu-id="320e7-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="320e7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="320e7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="320e7-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="320e7-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="320e7-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="320e7-128">Library</span></span><br/> | <dl> <span data-ttu-id="320e7-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="320e7-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="320e7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="320e7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="320e7-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="320e7-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="320e7-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="320e7-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




