---
description: Remuestrea una textura en la parametrización de esta gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper:: ResampleTex (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280438"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="1e277-103">ID3DXTextureGutterHelper:: ResampleTex (método)</span><span class="sxs-lookup"><span data-stu-id="1e277-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="1e277-104">Remuestrea una textura en la parametrización de esta gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="1e277-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e277-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e277-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="1e277-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e277-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e277-107">*pTextureIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e277-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e277-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="1e277-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="1e277-109">Textura que corresponde a la parametrización original en pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="1e277-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="1e277-110">Esta textura se usará para crear pTextureOut.</span><span class="sxs-lookup"><span data-stu-id="1e277-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="1e277-111">*pMeshIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e277-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e277-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1e277-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1e277-113">Malla que contiene las parametrizaciones originales y nuevas.</span><span class="sxs-lookup"><span data-stu-id="1e277-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="1e277-114">Es necesario almacenar la nueva parametrización en el \_ índice 0 de D3DDECLUSAGE TEXCOORD.</span><span class="sxs-lookup"><span data-stu-id="1e277-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="1e277-115">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1e277-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e277-116">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="1e277-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="1e277-117">Uso de datos de vértices (se usa en combinación con UsageIndex), que identifica el componente de la declaración de vértice que contiene la parametrización original en pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="1e277-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="1e277-118">Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="1e277-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e277-119">*UsageIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e277-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e277-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e277-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e277-121">Índice de base cero (utilizado en combinación con uso), que identifica el componente de la declaración de vértice que contiene la parametrización original en pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="1e277-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="1e277-122">La combinación de D3DDECLUSAGE \_ TEXCOORD y index 0 es necesaria para la nueva parametrización; se puede usar cualquier combinación de uso/Índice.</span><span class="sxs-lookup"><span data-stu-id="1e277-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="1e277-123">*pTextureOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1e277-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e277-124">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="1e277-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="1e277-125">Textura remuestreada.</span><span class="sxs-lookup"><span data-stu-id="1e277-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e277-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e277-126">Return value</span></span>

<span data-ttu-id="1e277-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e277-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e277-128">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e277-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e277-129">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1e277-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e277-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e277-130">Remarks</span></span>

<span data-ttu-id="1e277-131">Una parametrización en el caso de esta función es un conjunto de coordenadas de textura que asigna los triángulos de una malla a los triángulos de una textura.</span><span class="sxs-lookup"><span data-stu-id="1e277-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="1e277-132">La nueva parametrización es el conjunto de coordenadas de textura contenidas en la interfaz auxiliar de medianil y la parametrización original es el conjunto de coordenadas de textura que contiene la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="1e277-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="1e277-133">Se supone que las coordenadas de textura están entre 0 y 1, ambos inclusive, y la nueva parametrización debe declararse en la declaración de vértices como índice de coordenadas de textura 0.</span><span class="sxs-lookup"><span data-stu-id="1e277-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="1e277-134">La textura original y la textura remuestreada deben tener el mismo ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="1e277-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="1e277-135">Por ejemplo, para prepararse para volver a muestrear una textura:</span><span class="sxs-lookup"><span data-stu-id="1e277-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="1e277-136">Cree la interfaz de textura original (pOriginalTex a continuación) mediante una función como [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="1e277-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="1e277-137">Cree la nueva interfaz de textura para la textura remuestreada (pResampledTex a continuación).</span><span class="sxs-lookup"><span data-stu-id="1e277-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="1e277-138">El tamaño de esta textura debe coincidir con el tamaño (ancho y alto) de la textura de la aplicación auxiliar de medianil.</span><span class="sxs-lookup"><span data-stu-id="1e277-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="1e277-139">Llame a [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) para obtener la nueva parametrización como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="1e277-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



<span data-ttu-id="1e277-140">Un escenario común podría ser usar UVAtlas para crear un Atlas de textura y, después, usar ResampleTex para volver a muestrear la textura en la nueva parametrización.</span><span class="sxs-lookup"><span data-stu-id="1e277-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="1e277-141">Para obtener más información sobre Atlases, vea [uso de UVAtlas (Direct3D 9)](using-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="1e277-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e277-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e277-142">Requirements</span></span>



| <span data-ttu-id="1e277-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e277-143">Requirement</span></span> | <span data-ttu-id="1e277-144">Value</span><span class="sxs-lookup"><span data-stu-id="1e277-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e277-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e277-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1e277-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e277-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1e277-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e277-147">Library</span></span><br/> | <dl> <span data-ttu-id="1e277-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e277-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e277-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e277-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e277-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="1e277-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="1e277-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="1e277-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
