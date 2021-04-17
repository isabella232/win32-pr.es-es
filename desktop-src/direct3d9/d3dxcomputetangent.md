---
description: Calcula los vectores tangentes para las coordenadas de textura especificadas en la fase de textura. Proporcionado para admitir aplicaciones heredadas. Use D3DXComputeTangentFrameEx para obtener mejores resultados.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Función D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717745"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="5b164-105">D3DXComputeTangent función)</span><span class="sxs-lookup"><span data-stu-id="5b164-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="5b164-106">Calcula los vectores tangentes para las coordenadas de textura especificadas en la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="5b164-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="5b164-107">Proporcionado para admitir aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="5b164-107">Provided to support legacy applications.</span></span> <span data-ttu-id="5b164-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obtener mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="5b164-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b164-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b164-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="5b164-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b164-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b164-111">*Malla* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b164-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b164-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5b164-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5b164-113">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b164-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5b164-114">*TexStageIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b164-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b164-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b164-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b164-116">Índice que representa la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="5b164-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="5b164-117">*TangentIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b164-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b164-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b164-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b164-119">Índice que proporciona el índice de uso de los datos de tangente.</span><span class="sxs-lookup"><span data-stu-id="5b164-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="5b164-120">La declaración de vértices implica el uso; Este índice modifica el uso con el índice de uso.</span><span class="sxs-lookup"><span data-stu-id="5b164-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="5b164-121">Para obtener más información sobre una declaración de vértices, vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="5b164-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b164-122">*BinormIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b164-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b164-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b164-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b164-124">Índice que proporciona el índice de uso de los datos binormales.</span><span class="sxs-lookup"><span data-stu-id="5b164-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="5b164-125">La declaración de vértices implica el uso; Este índice modifica el uso con el índice de uso.</span><span class="sxs-lookup"><span data-stu-id="5b164-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="5b164-126">Para obtener más información sobre una declaración de vértices, vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="5b164-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b164-127">*Ajustar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b164-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b164-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b164-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b164-129">Establezca este valor en 0 para ningún ajuste, o en 1 para el ajuste en las direcciones de e.</span><span class="sxs-lookup"><span data-stu-id="5b164-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="5b164-130">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b164-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b164-131">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b164-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5b164-132">Puntero a una matriz de tres DWORD por cada tipo que se va a rellenar con índices de caras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="5b164-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="5b164-133">El número de bytes de esta matriz debe ser al menos ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="5b164-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b164-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b164-134">Return value</span></span>

<span data-ttu-id="5b164-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b164-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b164-136">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b164-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5b164-137">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5b164-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b164-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b164-138">Remarks</span></span>

<span data-ttu-id="5b164-139">Si la declaración del vértice de la malla especifica campos de tangente o binormalización, **D3DXComputeTangent** actualizará los datos de tangente o binormales proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5b164-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="5b164-140">Como alternativa, establezca TangentIndex en [d3dx de \_ forma predeterminada](other-d3dx-constants.md) para no actualizar los datos de tangente proporcionados por el usuario o establezca BinormIndex en d3dx de \_ forma predeterminada para que no actualice los datos binormales proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5b164-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="5b164-141">TexStageIndex no se puede establecer en el \_ valor predeterminado de D3DX.</span><span class="sxs-lookup"><span data-stu-id="5b164-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="5b164-142">**D3DXComputeTangent** depende de la declaración del vértice de la malla que contenga el campo binormal (BinormIndex), el campo tangente (TangentIndex) o ambos.</span><span class="sxs-lookup"><span data-stu-id="5b164-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="5b164-143">Si faltan ambos, se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="5b164-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="5b164-144">Esta función simplemente llama a [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="5b164-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="5b164-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b164-145">Requirements</span></span>



| <span data-ttu-id="5b164-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b164-146">Requirement</span></span> | <span data-ttu-id="5b164-147">Value</span><span class="sxs-lookup"><span data-stu-id="5b164-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b164-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b164-148">Header</span></span><br/>  | <dl> <span data-ttu-id="5b164-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b164-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5b164-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b164-150">Library</span></span><br/> | <dl> <span data-ttu-id="5b164-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b164-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b164-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b164-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b164-153">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="5b164-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
