---
description: Calcular los IMT por triángulo desde datos por vértices. Esta función permite calcular el IMT basándose en cualquier valor de una malla (color, normal, etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Función D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718265"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="33be3-104">D3DXComputeIMTFromPerVertexSignal función)</span><span class="sxs-lookup"><span data-stu-id="33be3-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="33be3-105">Calcular los IMT por triángulo desde datos por vértices.</span><span class="sxs-lookup"><span data-stu-id="33be3-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="33be3-106">Esta función permite calcular el IMT basándose en cualquier valor de una malla (color, normal, etc.).</span><span class="sxs-lookup"><span data-stu-id="33be3-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="33be3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33be3-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="33be3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33be3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33be3-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33be3-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33be3-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="33be3-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="33be3-111">Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.</span><span class="sxs-lookup"><span data-stu-id="33be3-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="33be3-112">*pfVertexSignal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33be3-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33be3-113">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="33be3-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33be3-114">Un puntero a una matriz de datos por vértice a partir de la cual se calculará IMT.</span><span class="sxs-lookup"><span data-stu-id="33be3-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="33be3-115">El tamaño de la matriz es uSignalStride \* v, donde v es el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="33be3-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="33be3-116">*uSignalDimension* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33be3-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33be3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33be3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33be3-118">Número de flotantes por vértice.</span><span class="sxs-lookup"><span data-stu-id="33be3-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="33be3-119">*uSignalStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33be3-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33be3-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33be3-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33be3-121">Número de bytes por vértice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="33be3-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="33be3-122">Debe ser un múltiplo de sizeof (float)</span><span class="sxs-lookup"><span data-stu-id="33be3-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="33be3-123">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33be3-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33be3-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33be3-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33be3-125">Opciones de ajuste de textura.</span><span class="sxs-lookup"><span data-stu-id="33be3-125">Texture wrap options.</span></span> <span data-ttu-id="33be3-126">Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="33be3-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="33be3-127">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="33be3-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="33be3-128">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="33be3-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="33be3-129">Un puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.</span><span class="sxs-lookup"><span data-stu-id="33be3-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="33be3-130">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="33be3-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="33be3-131">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33be3-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33be3-132">Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="33be3-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="33be3-133">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="33be3-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="33be3-134">*ppIMTData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33be3-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33be3-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="33be3-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="33be3-136">Un puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta.</span><span class="sxs-lookup"><span data-stu-id="33be3-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="33be3-137">Esta matriz se puede proporcionar como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) de D3DX a fin de dar prioridad a la asignación de espacio de textura en la parametrización de textura.</span><span class="sxs-lookup"><span data-stu-id="33be3-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33be3-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33be3-138">Return value</span></span>

<span data-ttu-id="33be3-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33be3-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33be3-140">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="33be3-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="33be3-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33be3-141">Requirements</span></span>



| <span data-ttu-id="33be3-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="33be3-142">Requirement</span></span> | <span data-ttu-id="33be3-143">Value</span><span class="sxs-lookup"><span data-stu-id="33be3-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33be3-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33be3-144">Header</span></span><br/>  | <dl> <span data-ttu-id="33be3-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="33be3-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="33be3-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33be3-146">Library</span></span><br/> | <dl> <span data-ttu-id="33be3-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33be3-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33be3-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="33be3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33be3-149">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="33be3-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="33be3-150">Usar UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="33be3-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
