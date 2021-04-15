---
description: Calcula una proyección de iluminación distanl en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708061"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="46197-103">ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (método)</span><span class="sxs-lookup"><span data-stu-id="46197-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="46197-104">Calcula una proyección de iluminación distanl en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="46197-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="46197-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46197-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="46197-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46197-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46197-107">*Ordenar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46197-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46197-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46197-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46197-109">Orden de la representación SH de la iluminación Distant.</span><span class="sxs-lookup"><span data-stu-id="46197-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="46197-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="46197-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="46197-111">El grado de evaluación es Orderen-1.</span><span class="sxs-lookup"><span data-stu-id="46197-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="46197-112">*OrderOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46197-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46197-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46197-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46197-114">Orden de la representación SH de la iluminación local.</span><span class="sxs-lookup"><span data-stu-id="46197-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="46197-115">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="46197-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="46197-116">El grado de evaluación es OrderOut-1.</span><span class="sxs-lookup"><span data-stu-id="46197-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="46197-117">*NumVolSamples.xml* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46197-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46197-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46197-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46197-119">Número de ubicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="46197-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="46197-120">*pSampleLocs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46197-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46197-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="46197-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="46197-122">Posición de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="46197-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="46197-123">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="46197-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46197-124">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="46197-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="46197-125">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que proyecta la iluminación lejana en vectores de base SH.</span><span class="sxs-lookup"><span data-stu-id="46197-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="46197-126">Este búfer debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="46197-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="46197-127">Este método genera orderis ² \* OrderOut "² scalars per Channel en cada ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="46197-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46197-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46197-128">Return value</span></span>

<span data-ttu-id="46197-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46197-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46197-130">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46197-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46197-131">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="46197-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46197-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46197-132">Remarks</span></span>

<span data-ttu-id="46197-133">Este método calcula cómo llega la luz de un origen distante en cada punto del espacio especificado por pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="46197-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="46197-134">Los coeficientes SH representan la asignación, en cada punto de pSampleLocs, de Radiance de origen a Radiance de incidente transferido.</span><span class="sxs-lookup"><span data-stu-id="46197-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="46197-135">Para usar este método correctamente, debe establecer el muestreo en una esfera con UseSphere = **true** y UseCosine = **false** en [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); de lo contrario, este método devolverá un error con D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="46197-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="46197-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46197-136">Requirements</span></span>



| <span data-ttu-id="46197-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="46197-137">Requirement</span></span> | <span data-ttu-id="46197-138">Value</span><span class="sxs-lookup"><span data-stu-id="46197-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46197-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46197-139">Header</span></span><br/>  | <dl> <span data-ttu-id="46197-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="46197-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="46197-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46197-141">Library</span></span><br/> | <dl> <span data-ttu-id="46197-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46197-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46197-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="46197-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46197-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="46197-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="46197-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span><span class="sxs-lookup"><span data-stu-id="46197-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
