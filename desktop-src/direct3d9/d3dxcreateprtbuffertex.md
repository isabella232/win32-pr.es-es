---
description: Crea un búfer de transferencia Radiance (PRT) precalculado que se puede comprimir o rellenar con un simulador. Esta función debe usarse para crear búferes por píxel.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: Función D3DXCreatePRTBufferTex (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718221"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="194d6-104">D3DXCreatePRTBufferTex función)</span><span class="sxs-lookup"><span data-stu-id="194d6-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="194d6-105">Crea un búfer de transferencia Radiance (PRT) precalculado que se puede comprimir o rellenar con un simulador.</span><span class="sxs-lookup"><span data-stu-id="194d6-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="194d6-106">Esta función debe usarse para crear búferes por píxel.</span><span class="sxs-lookup"><span data-stu-id="194d6-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="194d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="194d6-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="194d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="194d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="194d6-109">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="194d6-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194d6-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194d6-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="194d6-111">Ancho de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="194d6-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="194d6-112">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="194d6-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194d6-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194d6-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="194d6-114">Alto de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="194d6-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="194d6-115">*NumCoeffs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="194d6-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194d6-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194d6-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="194d6-117">Número de coeficientes por ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="194d6-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="194d6-118">Cuando se usa el PRT esférico (SH) PRT, el número de coeficientes debe ser Order ², donde Order es el orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="194d6-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="194d6-119">El orden debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="194d6-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="194d6-120">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="194d6-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="194d6-121">*NumChannels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="194d6-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194d6-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194d6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="194d6-123">Número de canales de color que se van a establecer en la malla.</span><span class="sxs-lookup"><span data-stu-id="194d6-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="194d6-124">Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.</span><span class="sxs-lookup"><span data-stu-id="194d6-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="194d6-125">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="194d6-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="194d6-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="194d6-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="194d6-127">Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creado.</span><span class="sxs-lookup"><span data-stu-id="194d6-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="194d6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="194d6-128">Return value</span></span>

<span data-ttu-id="194d6-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="194d6-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="194d6-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="194d6-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="194d6-131">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="194d6-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="194d6-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="194d6-132">Remarks</span></span>

<span data-ttu-id="194d6-133">Cuando se crea el búfer, todos los valores se inicializan en cero.</span><span class="sxs-lookup"><span data-stu-id="194d6-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="194d6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="194d6-134">Requirements</span></span>



| <span data-ttu-id="194d6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="194d6-135">Requirement</span></span> | <span data-ttu-id="194d6-136">Value</span><span class="sxs-lookup"><span data-stu-id="194d6-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="194d6-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="194d6-137">Header</span></span><br/>  | <dl> <span data-ttu-id="194d6-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="194d6-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="194d6-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="194d6-139">Library</span></span><br/> | <dl> <span data-ttu-id="194d6-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="194d6-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="194d6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="194d6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194d6-142">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="194d6-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="194d6-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="194d6-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
