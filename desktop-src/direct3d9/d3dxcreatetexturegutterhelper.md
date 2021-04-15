---
description: Crea un objeto ID3DXTextureGutterHelper a partir de una malla de entrada y datos de textura.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Función D3DXCreateTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707891"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="ed15a-103">D3DXCreateTextureGutterHelper función)</span><span class="sxs-lookup"><span data-stu-id="ed15a-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="ed15a-104">Crea un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) a partir de una malla de entrada y datos de textura.</span><span class="sxs-lookup"><span data-stu-id="ed15a-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed15a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed15a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ed15a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed15a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed15a-107">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ed15a-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed15a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed15a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed15a-109">Ancho de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ed15a-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ed15a-110">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ed15a-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed15a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed15a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed15a-112">Alto de la textura, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ed15a-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ed15a-113">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed15a-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed15a-114">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ed15a-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ed15a-115">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed15a-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="ed15a-116">*GutterSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed15a-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed15a-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed15a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed15a-118">Número de textura por el que se va a obtener el muestreo de la textura y se creará la región de medianil.</span><span class="sxs-lookup"><span data-stu-id="ed15a-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="ed15a-119">Debe ser al menos 1.</span><span class="sxs-lookup"><span data-stu-id="ed15a-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="ed15a-120">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ed15a-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed15a-121">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed15a-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="ed15a-122">Puntero a un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="ed15a-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed15a-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed15a-123">Return value</span></span>

<span data-ttu-id="ed15a-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed15a-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed15a-125">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed15a-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ed15a-126">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ed15a-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed15a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed15a-127">Remarks</span></span>

<span data-ttu-id="ed15a-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para transformar una escena en nuevas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="ed15a-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed15a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed15a-129">Requirements</span></span>



| <span data-ttu-id="ed15a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed15a-130">Requirement</span></span> | <span data-ttu-id="ed15a-131">Value</span><span class="sxs-lookup"><span data-stu-id="ed15a-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed15a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed15a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ed15a-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed15a-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ed15a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed15a-134">Library</span></span><br/> | <dl> <span data-ttu-id="ed15a-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed15a-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed15a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed15a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed15a-137">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="ed15a-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
