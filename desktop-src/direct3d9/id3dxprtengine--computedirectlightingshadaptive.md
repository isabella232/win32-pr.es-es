---
description: Calcula la contribución de iluminación directa a objetos 3D en los que el Radiance de origen se representa mediante una aproximación de armónico (SH) esférico, mediante el muestreo adaptable.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821522"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="30a71-103">ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive (método)</span><span class="sxs-lookup"><span data-stu-id="30a71-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="30a71-104">Calcula la contribución de iluminación directa a objetos 3D en los que el Radiance de origen se representa mediante una aproximación de armónico (SH) esférico, mediante el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="30a71-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="30a71-105">Este método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada.</span><span class="sxs-lookup"><span data-stu-id="30a71-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a71-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30a71-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="30a71-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30a71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a71-108">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="30a71-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a71-109">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a71-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a71-110">Orden de la evaluación de SH.</span><span class="sxs-lookup"><span data-stu-id="30a71-110">Order of the SH evaluation.</span></span> <span data-ttu-id="30a71-111">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="30a71-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="30a71-112">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="30a71-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="30a71-113">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="30a71-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="30a71-114">*AdaptiveThresh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30a71-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a71-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a71-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a71-116">Umbral del vector de PRT que se va a usar para subdividir los vértices de malla y caras.</span><span class="sxs-lookup"><span data-stu-id="30a71-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="30a71-117">Si es menor que 1E-6F, se especifica un valor predeterminado de 1E-6F.</span><span class="sxs-lookup"><span data-stu-id="30a71-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="30a71-118">*MinEdgeLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30a71-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a71-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a71-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a71-120">Longitud mínima del borde de la superficie que se generará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="30a71-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="30a71-121">Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo.</span><span class="sxs-lookup"><span data-stu-id="30a71-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="30a71-122">Si es cero, se especifica un valor predeterminado de 4.</span><span class="sxs-lookup"><span data-stu-id="30a71-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="30a71-123">*MaxSubdiv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30a71-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a71-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a71-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a71-125">Nivel máximo de subdivisión de una esfera que se usará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="30a71-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="30a71-126">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30a71-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a71-127">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="30a71-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="30a71-128">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="30a71-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="30a71-129">Este búfer debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="30a71-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a71-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30a71-130">Return value</span></span>

<span data-ttu-id="30a71-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30a71-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30a71-132">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30a71-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30a71-133">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="30a71-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a71-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30a71-134">Requirements</span></span>



| <span data-ttu-id="30a71-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="30a71-135">Requirement</span></span> | <span data-ttu-id="30a71-136">Value</span><span class="sxs-lookup"><span data-stu-id="30a71-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30a71-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30a71-137">Header</span></span><br/>  | <dl> <span data-ttu-id="30a71-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="30a71-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="30a71-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30a71-139">Library</span></span><br/> | <dl> <span data-ttu-id="30a71-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30a71-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30a71-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="30a71-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a71-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="30a71-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="30a71-143">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="30a71-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
