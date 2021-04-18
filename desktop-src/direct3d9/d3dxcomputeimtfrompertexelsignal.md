---
description: Calcular los IMT por triángulo a partir de los datos de textura. Esta función es similar a D3DXComputeIMTFromTexture, pero usa una matriz Float para pasar los datos y puede calcular valores de mayor dimensiones que 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: Función D3DXComputeIMTFromPerTexelSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721465"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="82144-104">D3DXComputeIMTFromPerTexelSignal función)</span><span class="sxs-lookup"><span data-stu-id="82144-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="82144-105">Calcular los IMT por triángulo a partir de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="82144-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="82144-106">Esta función es similar a [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), pero usa una matriz Float para pasar los datos y puede calcular valores de mayor dimensiones que 4.</span><span class="sxs-lookup"><span data-stu-id="82144-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="82144-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82144-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="82144-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82144-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82144-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="82144-111">Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.</span><span class="sxs-lookup"><span data-stu-id="82144-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="82144-112">*dwTextureIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-114">Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="82144-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="82144-115">*pfTexelSignal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-116">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="82144-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="82144-117">Puntero a una matriz de textura de entrada de la que se calculará IMT.</span><span class="sxs-lookup"><span data-stu-id="82144-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="82144-118">El tamaño de la matriz es uWidth \* uHeight \* uComponents.</span><span class="sxs-lookup"><span data-stu-id="82144-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="82144-119">*uWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-121">Ancho de la textura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="82144-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="82144-122">*uHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-124">Alto de textura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="82144-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="82144-125">*uSignalDimension* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-127">Número de elementos flotantes por componente en cada elemento de la matriz de señal.</span><span class="sxs-lookup"><span data-stu-id="82144-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="82144-128">*uComponents* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-130">El número de componentes de cada textura.</span><span class="sxs-lookup"><span data-stu-id="82144-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="82144-131">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82144-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-133">Opciones de ajuste de textura.</span><span class="sxs-lookup"><span data-stu-id="82144-133">Texture wrap options.</span></span> <span data-ttu-id="82144-134">Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="82144-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="82144-135">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="82144-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="82144-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="82144-137">Un puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.</span><span class="sxs-lookup"><span data-stu-id="82144-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="82144-138">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="82144-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="82144-139">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82144-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82144-140">Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="82144-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="82144-141">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="82144-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="82144-142">*ppIMTData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82144-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82144-143">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82144-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82144-144">Un puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta.</span><span class="sxs-lookup"><span data-stu-id="82144-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="82144-145">Esta matriz se puede proporcionar como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) de D3DX a fin de dar prioridad a la asignación de espacio de textura en la parametrización de textura.</span><span class="sxs-lookup"><span data-stu-id="82144-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82144-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82144-146">Return value</span></span>

<span data-ttu-id="82144-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82144-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82144-148">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="82144-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="82144-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82144-149">Requirements</span></span>



| <span data-ttu-id="82144-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="82144-150">Requirement</span></span> | <span data-ttu-id="82144-151">Value</span><span class="sxs-lookup"><span data-stu-id="82144-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82144-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82144-152">Header</span></span><br/>  | <dl> <span data-ttu-id="82144-153"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="82144-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="82144-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82144-154">Library</span></span><br/> | <dl> <span data-ttu-id="82144-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82144-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82144-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="82144-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82144-157">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="82144-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="82144-158">Usar UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="82144-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
