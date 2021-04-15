---
description: Calcula una proyección de la iluminación directa desde el rebote de luz anterior en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine:: ComputeVolumeSamples (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708062"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="83bd3-103">ID3DXPRTEngine:: ComputeVolumeSamples (método)</span><span class="sxs-lookup"><span data-stu-id="83bd3-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="83bd3-104">Calcula una proyección de la iluminación directa desde el rebote de luz anterior en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="83bd3-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="83bd3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83bd3-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="83bd3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83bd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bd3-107">*pSurfDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83bd3-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bd3-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="83bd3-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="83bd3-109">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior.</span><span class="sxs-lookup"><span data-stu-id="83bd3-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="83bd3-110">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="83bd3-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bd3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83bd3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83bd3-112">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="83bd3-112">Order of the SH evaluation.</span></span> <span data-ttu-id="83bd3-113">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="83bd3-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="83bd3-114">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="83bd3-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="83bd3-115">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="83bd3-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="83bd3-116">*NumVolSamples.xml* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83bd3-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bd3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83bd3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83bd3-118">Número de ubicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="83bd3-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="83bd3-119">*pSampleLocs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83bd3-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bd3-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="83bd3-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="83bd3-121">Posición de cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="83bd3-121">Position for each sample.</span></span> <span data-ttu-id="83bd3-122">Si pSampleLocs es **null**, ComputeVolumeSamples calculará las matrices de transferencia en cada vértice de la malla.</span><span class="sxs-lookup"><span data-stu-id="83bd3-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="83bd3-123">Sin embargo, si pSampleLocs no es **null**, debe muestrear en una esfera (Set UseSphere = **true** y UseCosine = **false** en [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); de lo contrario, ComputeVolumeSamples devolverá D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="83bd3-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="83bd3-124">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83bd3-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83bd3-125">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="83bd3-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="83bd3-126">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que proyecta la iluminación directa del rebote de luz anterior en vectores de base SH.</span><span class="sxs-lookup"><span data-stu-id="83bd3-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="83bd3-127">Este búfer debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="83bd3-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bd3-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83bd3-128">Return value</span></span>

<span data-ttu-id="83bd3-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83bd3-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83bd3-130">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83bd3-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83bd3-131">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="83bd3-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="83bd3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83bd3-132">Remarks</span></span>

<span data-ttu-id="83bd3-133">Este método calcula cómo la luz de la función Radiance de origen se refleja en la superficie que representa la escena (pSurfDataIn) y llega en cada punto en el espacio especificado por pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="83bd3-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="83bd3-134">Los coeficientes SH representan la asignación, en cada punto de pSampleLocs, de Radiance de origen a Radiance de incidente transferido.</span><span class="sxs-lookup"><span data-stu-id="83bd3-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="83bd3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83bd3-135">Requirements</span></span>



| <span data-ttu-id="83bd3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="83bd3-136">Requirement</span></span> | <span data-ttu-id="83bd3-137">Value</span><span class="sxs-lookup"><span data-stu-id="83bd3-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83bd3-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83bd3-138">Header</span></span><br/>  | <dl> <span data-ttu-id="83bd3-139"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="83bd3-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="83bd3-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83bd3-140">Library</span></span><br/> | <dl> <span data-ttu-id="83bd3-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83bd3-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83bd3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="83bd3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bd3-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="83bd3-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="83bd3-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="83bd3-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
