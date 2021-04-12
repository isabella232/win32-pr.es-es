---
description: Calcula muestras de transferencia Radiance (PRT) precalculadas para un punto arbitrario (y un vector normal).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'ID3DXPRTEngine:: ComputeSurfSamplesBounce (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362810"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="38291-103">ID3DXPRTEngine:: ComputeSurfSamplesBounce (método)</span><span class="sxs-lookup"><span data-stu-id="38291-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="38291-104">Calcula muestras de transferencia Radiance (PRT) precalculadas para un punto arbitrario (y un vector normal).</span><span class="sxs-lookup"><span data-stu-id="38291-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="38291-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38291-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="38291-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38291-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38291-107">*pSurfDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38291-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38291-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="38291-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="38291-109">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el Radiance de origen del objeto 3D.</span><span class="sxs-lookup"><span data-stu-id="38291-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="38291-110">Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="38291-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="38291-111">*NumSamples* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38291-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38291-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38291-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38291-113">Número de ubicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="38291-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="38291-114">*pSampleLocs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38291-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38291-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38291-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="38291-116">Posición de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="38291-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="38291-117">*pSampleNorms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38291-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38291-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38291-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="38291-119">Vector normal para cada ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="38291-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="38291-120">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38291-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38291-121">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="38291-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="38291-122">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela la contribución de iluminación directa hasta el punto mediante la aproximación armónica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="38291-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="38291-123">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38291-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38291-124">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="38291-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="38291-125">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma de todas las salidas pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="38291-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="38291-126">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="38291-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38291-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38291-127">Return value</span></span>

<span data-ttu-id="38291-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38291-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38291-129">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38291-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38291-130">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="38291-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="38291-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38291-131">Requirements</span></span>



| <span data-ttu-id="38291-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="38291-132">Requirement</span></span> | <span data-ttu-id="38291-133">Value</span><span class="sxs-lookup"><span data-stu-id="38291-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38291-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38291-134">Header</span></span><br/>  | <dl> <span data-ttu-id="38291-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="38291-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="38291-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38291-136">Library</span></span><br/> | <dl> <span data-ttu-id="38291-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38291-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38291-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="38291-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38291-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="38291-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="38291-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="38291-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
