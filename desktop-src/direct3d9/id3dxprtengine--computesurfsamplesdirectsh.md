---
description: Calcula, en un punto arbitrario que no está en una malla, un vector de transferencia que asigna Radiance de origen (representado mediante una aproximación de armónico (SH)) para salir de radiance.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'ID3DXPRTEngine:: ComputeSurfSamplesDirectSH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362808"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="51c2c-103">ID3DXPRTEngine:: ComputeSurfSamplesDirectSH (método)</span><span class="sxs-lookup"><span data-stu-id="51c2c-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="51c2c-104">Calcula, en un punto arbitrario que no está en una malla, un vector de transferencia que asigna Radiance de origen (representado mediante una aproximación de armónico (SH)) para salir de radiance.</span><span class="sxs-lookup"><span data-stu-id="51c2c-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51c2c-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="51c2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51c2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c2c-107">*SHOrder* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51c2c-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c2c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51c2c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51c2c-109">Orden de la aproximación de SH que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="51c2c-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="51c2c-110">*NumSamples* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51c2c-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c2c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51c2c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="51c2c-112">Número de ubicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="51c2c-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="51c2c-113">*pSampleLocs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51c2c-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c2c-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="51c2c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="51c2c-115">Posición de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="51c2c-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="51c2c-116">*pSampleNorms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51c2c-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51c2c-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="51c2c-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="51c2c-118">Vector normal para cada ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="51c2c-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="51c2c-119">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="51c2c-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51c2c-120">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="51c2c-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="51c2c-121">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela la contribución de iluminación directa al punto mediante la aproximación SH.</span><span class="sxs-lookup"><span data-stu-id="51c2c-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c2c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51c2c-122">Return value</span></span>

<span data-ttu-id="51c2c-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="51c2c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="51c2c-124">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="51c2c-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="51c2c-125">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="51c2c-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="51c2c-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51c2c-126">Remarks</span></span>

<span data-ttu-id="51c2c-127">No utilice un búfer de textura al llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="51c2c-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="51c2c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51c2c-128">Requirements</span></span>



| <span data-ttu-id="51c2c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c2c-129">Requirement</span></span> | <span data-ttu-id="51c2c-130">Value</span><span class="sxs-lookup"><span data-stu-id="51c2c-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51c2c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51c2c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="51c2c-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c2c-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="51c2c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51c2c-133">Library</span></span><br/> | <dl> <span data-ttu-id="51c2c-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51c2c-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="51c2c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="51c2c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c2c-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="51c2c-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="51c2c-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="51c2c-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="51c2c-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span><span class="sxs-lookup"><span data-stu-id="51c2c-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
