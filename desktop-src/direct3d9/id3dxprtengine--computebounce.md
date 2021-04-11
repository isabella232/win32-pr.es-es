---
description: Calcula el Radiance de origen resultante de un único rebote de luz interreflejada. Este método se puede usar para cualquier escena iluminada, incluido un modelo Radiance (PRT) precalculado basado en armónico (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine:: ComputeBounce (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362740"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="e7b41-104">ID3DXPRTEngine:: ComputeBounce (método)</span><span class="sxs-lookup"><span data-stu-id="e7b41-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="e7b41-105">Calcula el Radiance de origen resultante de un único rebote de luz interreflejada.</span><span class="sxs-lookup"><span data-stu-id="e7b41-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="e7b41-106">Este método se puede usar para cualquier escena iluminada, incluido un modelo Radiance (PRT) precalculado basado en armónico (SH).</span><span class="sxs-lookup"><span data-stu-id="e7b41-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b41-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7b41-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="e7b41-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7b41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b41-109">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7b41-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b41-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b41-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e7b41-111">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior.</span><span class="sxs-lookup"><span data-stu-id="e7b41-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="e7b41-112">Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="e7b41-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e7b41-113">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e7b41-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b41-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b41-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e7b41-115">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela un único rebote de la luz interreflejada.</span><span class="sxs-lookup"><span data-stu-id="e7b41-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="e7b41-116">Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="e7b41-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e7b41-117">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e7b41-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b41-118">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e7b41-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e7b41-119">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma de todas las salidas pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="e7b41-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="e7b41-120">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="e7b41-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b41-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7b41-121">Return value</span></span>

<span data-ttu-id="e7b41-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7b41-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7b41-123">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7b41-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7b41-124">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e7b41-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b41-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7b41-125">Remarks</span></span>

<span data-ttu-id="e7b41-126">Utilice la siguiente secuencia de llamada para modelar varios rebotes claros con iluminación directa.</span><span class="sxs-lookup"><span data-stu-id="e7b41-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="e7b41-127">Use la siguiente secuencia de llamada para modelar varios rebotes claros con dispersión de subsuperficies.</span><span class="sxs-lookup"><span data-stu-id="e7b41-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="e7b41-128">La salida de este método no incluye albedo y solo la luz entrante está integrada en el simulador.</span><span class="sxs-lookup"><span data-stu-id="e7b41-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="e7b41-129">Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.</span><span class="sxs-lookup"><span data-stu-id="e7b41-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="e7b41-130">Llame a [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de PRT por el albedo.</span><span class="sxs-lookup"><span data-stu-id="e7b41-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b41-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b41-131">Requirements</span></span>



| <span data-ttu-id="e7b41-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b41-132">Requirement</span></span> | <span data-ttu-id="e7b41-133">Value</span><span class="sxs-lookup"><span data-stu-id="e7b41-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b41-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7b41-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b41-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b41-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e7b41-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7b41-136">Library</span></span><br/> | <dl> <span data-ttu-id="e7b41-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7b41-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7b41-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b41-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b41-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e7b41-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e7b41-140">**ID3DXPRTEngine:: Compute (no es)**</span><span class="sxs-lookup"><span data-stu-id="e7b41-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




