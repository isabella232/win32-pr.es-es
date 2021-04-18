---
description: Crea un búfer de transferencia Radiance (PRT) precalculado que se puede comprimir o rellenar con un simulador. Esta función debe usarse para crear búferes de volumen o por vértices.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Función D3DXCreatePRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718222"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="c7c2e-104">D3DXCreatePRTBuffer función)</span><span class="sxs-lookup"><span data-stu-id="c7c2e-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="c7c2e-105">Crea un búfer de transferencia Radiance (PRT) precalculado que se puede comprimir o rellenar con un simulador.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="c7c2e-106">Esta función debe usarse para crear búferes de volumen o por vértices.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c2e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7c2e-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="c7c2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7c2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c2e-109">*NumSamples* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7c2e-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c2e-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c2e-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c2e-111">Número de vértices (o textura) muestreados.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="c7c2e-112">*NumCoeffs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7c2e-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c2e-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c2e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c2e-114">Número de coeficientes por ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="c7c2e-115">Cuando se usa el PRT esférico (SH) PRT, el número de coeficientes debe ser Order ², donde Order es el orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="c7c2e-116">El orden debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c7c2e-117">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c7c2e-118">*NumChannels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7c2e-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c2e-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7c2e-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7c2e-120">Número de canales de color que se van a establecer en la malla.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="c7c2e-121">Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="c7c2e-122">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c7c2e-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c2e-123">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7c2e-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="c7c2e-124">Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creado.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c2e-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7c2e-125">Return value</span></span>

<span data-ttu-id="c7c2e-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7c2e-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7c2e-127">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c7c2e-128">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c2e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7c2e-129">Remarks</span></span>

<span data-ttu-id="c7c2e-130">Cuando se crea el búfer, todos los valores se inicializan en cero.</span><span class="sxs-lookup"><span data-stu-id="c7c2e-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c2e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c2e-131">Requirements</span></span>



| <span data-ttu-id="c7c2e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c2e-132">Requirement</span></span> | <span data-ttu-id="c7c2e-133">Value</span><span class="sxs-lookup"><span data-stu-id="c7c2e-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c2e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7c2e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c7c2e-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c2e-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c7c2e-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7c2e-136">Library</span></span><br/> | <dl> <span data-ttu-id="c7c2e-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7c2e-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7c2e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7c2e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c2e-139">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="c7c2e-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="c7c2e-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="c7c2e-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
