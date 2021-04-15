---
description: Calcula el Radiance de origen resultante de un único rebote de luz interreflejada mediante el muestreo adaptable.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'ID3DXPRTEngine:: ComputeBounceAdaptive (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708064"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="f783c-103">ID3DXPRTEngine:: ComputeBounceAdaptive (método)</span><span class="sxs-lookup"><span data-stu-id="f783c-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="f783c-104">Calcula el Radiance de origen resultante de un único rebote de luz interreflejada mediante el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="f783c-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="f783c-105">Este método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada.</span><span class="sxs-lookup"><span data-stu-id="f783c-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="f783c-106">Este método se puede usar para cualquier escena iluminada, incluido un modelo PRT basado en armónico (SH).</span><span class="sxs-lookup"><span data-stu-id="f783c-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="f783c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f783c-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="f783c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f783c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f783c-109">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f783c-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f783c-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f783c-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f783c-111">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior.</span><span class="sxs-lookup"><span data-stu-id="f783c-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="f783c-112">Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="f783c-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="f783c-113">*AdaptiveThresh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f783c-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f783c-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f783c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f783c-115">Umbral del vector de PRT que se va a usar para subdividir los vértices de malla y caras.</span><span class="sxs-lookup"><span data-stu-id="f783c-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="f783c-116">Si es menor que 1E-6F, se especifica un valor predeterminado de 1E-6F.</span><span class="sxs-lookup"><span data-stu-id="f783c-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="f783c-117">*MinEdgeLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f783c-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f783c-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f783c-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f783c-119">Longitud mínima del borde de la superficie que se generará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="f783c-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="f783c-120">Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo.</span><span class="sxs-lookup"><span data-stu-id="f783c-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="f783c-121">Si es cero, se especifica un valor predeterminado de 4.</span><span class="sxs-lookup"><span data-stu-id="f783c-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="f783c-122">*MaxSubdiv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f783c-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f783c-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f783c-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f783c-124">Nivel máximo de subdivisión de una esfera que se usará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="f783c-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f783c-125">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f783c-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f783c-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f783c-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f783c-127">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="f783c-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="f783c-128">Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="f783c-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="f783c-129">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f783c-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f783c-130">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f783c-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f783c-131">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que mantiene una suma en ejecución de pDataOut con cada cálculo de rebote de luz.</span><span class="sxs-lookup"><span data-stu-id="f783c-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="f783c-132">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f783c-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f783c-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f783c-133">Return value</span></span>

<span data-ttu-id="f783c-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f783c-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f783c-135">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f783c-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f783c-136">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f783c-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f783c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f783c-137">Requirements</span></span>



| <span data-ttu-id="f783c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f783c-138">Requirement</span></span> | <span data-ttu-id="f783c-139">Value</span><span class="sxs-lookup"><span data-stu-id="f783c-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f783c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f783c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="f783c-141"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f783c-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f783c-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f783c-142">Library</span></span><br/> | <dl> <span data-ttu-id="f783c-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f783c-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f783c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f783c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f783c-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f783c-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f783c-146">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="f783c-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
