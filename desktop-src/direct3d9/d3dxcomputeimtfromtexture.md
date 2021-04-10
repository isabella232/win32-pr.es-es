---
description: Calcula el IMT por triángulo a partir de una textura asignada a una malla, que se usará opcionalmente como entrada para las funciones de UVAtlas de D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Función D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083776"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="6be7e-103">D3DXComputeIMTFromTexture función)</span><span class="sxs-lookup"><span data-stu-id="6be7e-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="6be7e-104">Calcula el IMT por triángulo a partir de una textura asignada a una malla, que se usará opcionalmente como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)de D3DX.</span><span class="sxs-lookup"><span data-stu-id="6be7e-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6be7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6be7e-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="6be7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6be7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be7e-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6be7e-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7e-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6be7e-109">Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.</span><span class="sxs-lookup"><span data-stu-id="6be7e-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="6be7e-110">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6be7e-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7e-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="6be7e-112">Puntero a la textura (vea [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) que está asignada a la malla.</span><span class="sxs-lookup"><span data-stu-id="6be7e-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6be7e-113">*dwTextureIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6be7e-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7e-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6be7e-115">Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6be7e-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="6be7e-116">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6be7e-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7e-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6be7e-118">Opciones de ajuste de textura.</span><span class="sxs-lookup"><span data-stu-id="6be7e-118">Texture wrap options.</span></span> <span data-ttu-id="6be7e-119">Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6be7e-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6be7e-120">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="6be7e-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="6be7e-121">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="6be7e-122">Un puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.</span><span class="sxs-lookup"><span data-stu-id="6be7e-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="6be7e-123">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="6be7e-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="6be7e-124">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6be7e-125">Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="6be7e-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="6be7e-126">Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6be7e-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="6be7e-127">*ppIMTData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6be7e-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6be7e-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6be7e-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6be7e-129">Un puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta.</span><span class="sxs-lookup"><span data-stu-id="6be7e-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="6be7e-130">Esta matriz se puede proporcionar como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) de D3DX a fin de dar prioridad a la asignación de espacio de textura en la parametrización de textura.</span><span class="sxs-lookup"><span data-stu-id="6be7e-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be7e-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6be7e-131">Return value</span></span>

<span data-ttu-id="6be7e-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6be7e-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6be7e-133">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6be7e-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be7e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6be7e-134">Remarks</span></span>

<span data-ttu-id="6be7e-135">Dada una textura que se asigna a través de la superficie de la malla, el algoritmo calcula el IMT para cada cara.</span><span class="sxs-lookup"><span data-stu-id="6be7e-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="6be7e-136">Esto hará que los triángulos que contienen datos de señal de menor frecuencia ocupen menos espacio en el Atlas de textura final cuando se parametrizan con las funciones de UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="6be7e-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="6be7e-137">Se supone que la textura se interpola a través de la malla bilinealmente.</span><span class="sxs-lookup"><span data-stu-id="6be7e-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be7e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6be7e-138">Requirements</span></span>



| <span data-ttu-id="6be7e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be7e-139">Requirement</span></span> | <span data-ttu-id="6be7e-140">Value</span><span class="sxs-lookup"><span data-stu-id="6be7e-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6be7e-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6be7e-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6be7e-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6be7e-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6be7e-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6be7e-143">Library</span></span><br/> | <dl> <span data-ttu-id="6be7e-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6be7e-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6be7e-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6be7e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be7e-146">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="6be7e-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="6be7e-147">Usar UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6be7e-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
