---
description: Calcula los IMT por triángulo a partir de una señal personalizada especificada por la aplicación que varía en la superficie de la malla (generalmente con una frecuencia mayor que los datos del vértice). La señal se evalúa mediante una función de devolución de llamada especificada por el usuario.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Función D3DXComputeIMTFromSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718315"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="2fcfc-104">D3DXComputeIMTFromSignal función)</span><span class="sxs-lookup"><span data-stu-id="2fcfc-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="2fcfc-105">Calcula los IMT por triángulo a partir de una señal personalizada especificada por la aplicación que varía en la superficie de la malla (generalmente con una frecuencia mayor que los datos del vértice).</span><span class="sxs-lookup"><span data-stu-id="2fcfc-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="2fcfc-106">La señal se evalúa mediante una función de devolución de llamada especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcfc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fcfc-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="2fcfc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fcfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fcfc-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="2fcfc-111">Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-112">*dwTextureIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fcfc-114">Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-115">*uSignalDimension* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fcfc-117">El número de componentes de cada punto de datos de la señal.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-118">*fMaxUVDistance* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fcfc-120">Distancia máxima entre los vértices; el algoritmo continúa subdividiendo hasta que la distancia entre todos los vértices es menor o igual que fMaxUVDistance.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-121">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fcfc-123">Opciones de ajuste de textura.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-123">Texture wrap options.</span></span> <span data-ttu-id="2fcfc-124">Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2fcfc-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-125">*pSignalCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-126">Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="2fcfc-127">Puntero a una función evaluadora proporcionada por el usuario, que se utilizará para calcular el valor de la señal en coordenadas U, V arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="2fcfc-128">La función sigue el prototipo de [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span><span class="sxs-lookup"><span data-stu-id="2fcfc-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-129">*pUserData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-130">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="2fcfc-130">Type: **VOID\***</span></span>

<span data-ttu-id="2fcfc-131">Un puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada de la señal.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="2fcfc-132">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-133">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="2fcfc-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="2fcfc-134">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="2fcfc-135">Un puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-136">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="2fcfc-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="2fcfc-137">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fcfc-138">Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="2fcfc-139">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="2fcfc-140">*ppIMTData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2fcfc-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcfc-141">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fcfc-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2fcfc-142">Un puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="2fcfc-143">Esta matriz se puede proporcionar como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) de D3DX a fin de dar prioridad a la asignación de espacio de textura en la parametrización de textura.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fcfc-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fcfc-144">Return value</span></span>

<span data-ttu-id="2fcfc-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fcfc-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fcfc-146">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcfc-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fcfc-147">Remarks</span></span>

<span data-ttu-id="2fcfc-148">Esta función requiere que la malla de entrada contenga una asignación de textura de señal a malla (es decir, coordenadas de textura).</span><span class="sxs-lookup"><span data-stu-id="2fcfc-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="2fcfc-149">Permite al usuario definir una señal arbitrariamente a través de la superficie de la malla.</span><span class="sxs-lookup"><span data-stu-id="2fcfc-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcfc-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fcfc-150">Requirements</span></span>



| <span data-ttu-id="2fcfc-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fcfc-151">Requirement</span></span> | <span data-ttu-id="2fcfc-152">Value</span><span class="sxs-lookup"><span data-stu-id="2fcfc-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcfc-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fcfc-153">Header</span></span><br/>  | <dl> <span data-ttu-id="2fcfc-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fcfc-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2fcfc-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fcfc-155">Library</span></span><br/> | <dl> <span data-ttu-id="2fcfc-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fcfc-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2fcfc-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fcfc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcfc-158">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="2fcfc-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="2fcfc-159">Usar UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2fcfc-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
