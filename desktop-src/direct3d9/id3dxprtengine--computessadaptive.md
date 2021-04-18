---
description: 'Calcula un vector de transferencia que asigna Radiance de origen para salir de Radiance resultante de la dispersión de subsuperficies, mediante el muestreo adaptable y las propiedades de material establecidas por ID3DXPRTEngine:: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine:: ComputeSSAdaptive (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718549"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="bc446-103">ID3DXPRTEngine:: ComputeSSAdaptive (método)</span><span class="sxs-lookup"><span data-stu-id="bc446-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="bc446-104">Calcula un vector de transferencia que asigna Radiance de origen para salir de Radiance resultante de la dispersión de subsuperficies, mediante el muestreo adaptable y las propiedades de material establecidas por [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="bc446-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="bc446-105">El método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada.</span><span class="sxs-lookup"><span data-stu-id="bc446-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="bc446-106">Este método solo se puede usar para los materiales definidos por vértice en un objeto Mesh.</span><span class="sxs-lookup"><span data-stu-id="bc446-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc446-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc446-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="bc446-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc446-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc446-109">*pDataIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc446-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc446-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bc446-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bc446-111">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior.</span><span class="sxs-lookup"><span data-stu-id="bc446-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="bc446-112">Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="bc446-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="bc446-113">*AdaptiveThresh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc446-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc446-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc446-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc446-115">Umbral del vector de PRT que se va a usar para subdividir los vértices de malla y caras.</span><span class="sxs-lookup"><span data-stu-id="bc446-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="bc446-116">Si es menor que 1E-6F, se especifica un valor predeterminado de 1E-6F.</span><span class="sxs-lookup"><span data-stu-id="bc446-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="bc446-117">*MinEdgeLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc446-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc446-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc446-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc446-119">Longitud mínima del borde de la superficie que se generará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="bc446-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="bc446-120">Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo.</span><span class="sxs-lookup"><span data-stu-id="bc446-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="bc446-121">*MaxSubdiv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc446-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc446-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc446-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc446-123">Nivel máximo de subdivisión de una esfera que se usará en el muestreo adaptable.</span><span class="sxs-lookup"><span data-stu-id="bc446-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="bc446-124">Si es cero, se especifica un valor predeterminado de 4.</span><span class="sxs-lookup"><span data-stu-id="bc446-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="bc446-125">*pDataOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc446-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc446-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bc446-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bc446-127">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela un único rebote de la luz dispersa por subsuperficie.</span><span class="sxs-lookup"><span data-stu-id="bc446-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="bc446-128">Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.</span><span class="sxs-lookup"><span data-stu-id="bc446-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="bc446-129">*pDataTotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc446-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc446-130">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="bc446-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="bc446-131">Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma de todas las salidas pDataOut anteriores.</span><span class="sxs-lookup"><span data-stu-id="bc446-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="bc446-132">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="bc446-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc446-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc446-133">Return value</span></span>

<span data-ttu-id="bc446-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc446-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc446-135">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc446-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bc446-136">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bc446-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc446-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc446-137">Remarks</span></span>

<span data-ttu-id="bc446-138">Para modelar la dispersión de subsuperficies, llame a este método para cada rebote de luz después de llamar a un método [**ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) .</span><span class="sxs-lookup"><span data-stu-id="bc446-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="bc446-139">La salida de este método no incluye albedo y solo la luz entrante está integrada en el simulador.</span><span class="sxs-lookup"><span data-stu-id="bc446-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="bc446-140">Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.</span><span class="sxs-lookup"><span data-stu-id="bc446-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="bc446-141">Llame a [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de PRT por el albedo.</span><span class="sxs-lookup"><span data-stu-id="bc446-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc446-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc446-142">Requirements</span></span>



| <span data-ttu-id="bc446-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc446-143">Requirement</span></span> | <span data-ttu-id="bc446-144">Value</span><span class="sxs-lookup"><span data-stu-id="bc446-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc446-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc446-145">Header</span></span><br/>  | <dl> <span data-ttu-id="bc446-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc446-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bc446-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc446-147">Library</span></span><br/> | <dl> <span data-ttu-id="bc446-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc446-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc446-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc446-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc446-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="bc446-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="bc446-151">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="bc446-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="bc446-152">**ID3DXPRTEngine:: Compute (no es)**</span><span class="sxs-lookup"><span data-stu-id="bc446-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
