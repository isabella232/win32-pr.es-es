---
description: Soldaduras juntas los vértices replicados que tienen los mismos atributos. Este método usa valores de épsilon especificados para comparaciones de igualdad.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Función D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821135"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="6e0d8-104">D3DXWeldVertices función)</span><span class="sxs-lookup"><span data-stu-id="6e0d8-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="6e0d8-105">Soldaduras juntas los vértices replicados que tienen los mismos atributos.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="6e0d8-106">Este método usa valores de épsilon especificados para comparaciones de igualdad.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0d8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e0d8-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="6e0d8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e0d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0d8-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6e0d8-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6e0d8-111">Puntero a un objeto [**ID3DXMesh**](id3dxmesh.md) , la malla desde la que se van a soldar los vértices.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d8-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e0d8-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e0d8-114">Combinación de una o varias marcas de [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span><span class="sxs-lookup"><span data-stu-id="6e0d8-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e0d8-115">*pEpsilons* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-116">Tipo: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e0d8-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="6e0d8-117">Puntero a una estructura [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , que especifica los valores de épsilon que se usarán para este método.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="6e0d8-118">Use **null** para inicializar todos los miembros de la estructura con un valor predeterminado de 1,0 e-6F.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d8-119">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-120">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e0d8-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6e0d8-121">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="6e0d8-122">Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="6e0d8-123">Si este parámetro se establece en **null**, se llamará a [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) para crear información lógica de proximidad.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d8-124">*pAdjacencyOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e0d8-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6e0d8-126">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="6e0d8-127">Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d8-128">*pFaceRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e0d8-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6e0d8-130">Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla soldada.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6e0d8-131">*ppVertexRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e0d8-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0d8-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e0d8-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6e0d8-133">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="6e0d8-134">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0d8-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e0d8-135">Return value</span></span>

<span data-ttu-id="6e0d8-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e0d8-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e0d8-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6e0d8-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0d8-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e0d8-139">Remarks</span></span>

<span data-ttu-id="6e0d8-140">Esta función usa la información de adyacencia suministrada para determinar los puntos que se replican.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="6e0d8-141">Los vértices se combinan en función de una comparación de épsilon.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="6e0d8-142">Los vértices con la misma posición deben haberse calculado y representados mediante datos de representadores de puntos.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="6e0d8-143">Esta función combina vértices con soldadura lógica que tienen componentes similares, como normales o coordenadas de textura dentro de pEpsilons.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="6e0d8-144">En el siguiente código de ejemplo se llama a esta función con la soldadura habilitada.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="6e0d8-145">Los vértices se comparan usando valores de épsilon para el vector normal y la posición del vértice.</span><span class="sxs-lookup"><span data-stu-id="6e0d8-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="6e0d8-146">Se devuelve un puntero a una matriz de reasignación de caras (*pFaceRemap*).</span><span class="sxs-lookup"><span data-stu-id="6e0d8-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="6e0d8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e0d8-147">Requirements</span></span>



| <span data-ttu-id="6e0d8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0d8-148">Requirement</span></span> | <span data-ttu-id="6e0d8-149">Value</span><span class="sxs-lookup"><span data-stu-id="6e0d8-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0d8-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e0d8-150">Header</span></span><br/>  | <dl> <span data-ttu-id="6e0d8-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d8-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6e0d8-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e0d8-152">Library</span></span><br/> | <dl> <span data-ttu-id="6e0d8-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e0d8-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e0d8-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e0d8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0d8-155">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="6e0d8-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
