---
description: 'Calcula el Radiance de origen resultante de la dispersión de subsuperficies, mediante las propiedades de material establecidas por ID3DXPRTEngine:: SetMeshMaterials. Este método solo se puede usar para los materiales definidos por vértice en un objeto Mesh.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'ID3DXPRTEngine:: Compute Method (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362812"
---
# <a name="id3dxprtenginecomputess-method"></a><span data-ttu-id="f2f3d-104">ID3DXPRTEngine:: Compute (método)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-104">ID3DXPRTEngine::ComputeSS method</span></span>

<span data-ttu-id="f2f3d-105">Calcula el Radiance de origen resultante de la dispersión de subsuperficies, mediante las propiedades de material establecidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="f2f3d-105">Computes the source radiance resulting from subsurface scattering, using material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="f2f3d-106">Este método solo se puede usar para los materiales definidos por vértice en un objeto Mesh.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f3d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2f3d-107">Syntax</span></span>


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="f2f3d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f3d-109">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f3d-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f3d-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f2f3d-111">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="f2f3d-112">Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="f2f3d-113">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f2f3d-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f3d-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f2f3d-115">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela un único rebote de la luz dispersa por subsuperficie.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="f2f3d-116">Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="f2f3d-117">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f2f3d-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f3d-118">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f2f3d-119">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma de todas las salidas pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="f2f3d-120">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f3d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f3d-121">Return value</span></span>

<span data-ttu-id="f2f3d-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2f3d-123">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2f3d-124">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f3d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2f3d-125">Remarks</span></span>

<span data-ttu-id="f2f3d-126">Para modelar la dispersión de subsuperficies, llame a este método para cada rebote de luz después de llamar a un método ID3DXPRTEngine:: ComputeDirectLighting.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-126">To model subsurface scattering, call this method for each light bounce after an ID3DXPRTEngine::ComputeDirectLighting method is called.</span></span>

<span data-ttu-id="f2f3d-127">Use la siguiente secuencia de llamada para modelar la dispersión de subsuperficies.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-127">Use the following calling sequence to model subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



<span data-ttu-id="f2f3d-128">La salida de este método no incluye albedo y solo la luz entrante está integrada en el simulador.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="f2f3d-129">Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="f2f3d-130">Llame a [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia de Radiance previamente calculado (PRT) por Albedo.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f3d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f3d-131">Requirements</span></span>



| <span data-ttu-id="f2f3d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f3d-132">Requirement</span></span> | <span data-ttu-id="f2f3d-133">Value</span><span class="sxs-lookup"><span data-stu-id="f2f3d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f3d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f3d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f2f3d-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f3d-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f2f3d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2f3d-136">Library</span></span><br/> | <dl> <span data-ttu-id="f2f3d-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2f3d-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2f3d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f3d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f3d-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f2f3d-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f2f3d-140">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-140">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




