---
description: Se usa con los resultados comprimidos de la versión de vértice del simulador Radiance Transfer (PRT) precalculado.
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Función D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424367"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="302f3-103">D3DXSHPRTCompSplitMeshSC función)</span><span class="sxs-lookup"><span data-stu-id="302f3-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="302f3-104">Se usa con los resultados comprimidos de la versión de vértice del simulador Radiance Transfer (PRT) precalculado.</span><span class="sxs-lookup"><span data-stu-id="302f3-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="302f3-105">Después de llamar a [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) , esta función se puede usar para dividir la malla en un grupo de caras/vértices por superclúster.</span><span class="sxs-lookup"><span data-stu-id="302f3-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="302f3-106">Cada superclúster contiene todas las caras que contienen cualquier vértice clasificado en uno de sus clústeres.</span><span class="sxs-lookup"><span data-stu-id="302f3-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="302f3-107">Todos los vértices conectados a este conjunto de caras también se incluyen con el ppVertStatus de matriz devuelto, que indica si el vértice pertenece al superclúster.</span><span class="sxs-lookup"><span data-stu-id="302f3-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="302f3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="302f3-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="302f3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="302f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="302f3-110">*pClusterIDs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="302f3-112">Identificadores de clúster de *NumVertices* (extraídos de un búfer comprimido).</span><span class="sxs-lookup"><span data-stu-id="302f3-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="302f3-113">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-115">Número de vértices en la malla original.</span><span class="sxs-lookup"><span data-stu-id="302f3-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-116">*NumCs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-118">Número de clústeres (parámetro de entrada para compresión).</span><span class="sxs-lookup"><span data-stu-id="302f3-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="302f3-119">*pSClusterIDs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="302f3-121">Matriz de tamaño *NumCs* que contendrá los identificadores de superclúster.</span><span class="sxs-lookup"><span data-stu-id="302f3-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-122">*NumSCs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-124">Número de clústeres superpuestos asignados en [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="302f3-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="302f3-125">*pInputIB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-127">Búfer de índice sin formato para la malla.</span><span class="sxs-lookup"><span data-stu-id="302f3-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="302f3-128">El formato depende de *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="302f3-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-129">*InputIBIs32Bit* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-130">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-131">Si es **true**, el búfer de índice se establece en 32 bits; de lo contrario, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="302f3-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-132">*NumFaces* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="302f3-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-134">Número de caras de la malla original (*pInputIB* es 3 veces esta longitud).</span><span class="sxs-lookup"><span data-stu-id="302f3-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="302f3-135">*ppIBData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="302f3-137">Búfer de índice sin formato que contendrá los rostros de división resultantes.</span><span class="sxs-lookup"><span data-stu-id="302f3-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="302f3-138">Formato determinado por *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="302f3-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="302f3-139">Asignado por función.</span><span class="sxs-lookup"><span data-stu-id="302f3-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-140">*pIBDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="302f3-142">Longitud de *ppIBData*, asignada en la función.</span><span class="sxs-lookup"><span data-stu-id="302f3-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-143">*OutputIBIs32Bit* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-144">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="302f3-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="302f3-145">Si **es true**, asigna una matriz de enteros sin signo; de lo contrario, asigna una matriz corta sin signo.</span><span class="sxs-lookup"><span data-stu-id="302f3-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-146">*ppFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-147">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="302f3-148">Asignación de cada cara de *ppIBData* a caras originales.</span><span class="sxs-lookup"><span data-stu-id="302f3-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="302f3-149">La longitud es \* *pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="302f3-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-150">*ppVertData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="302f3-152">Nueva estructura de datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="302f3-152">New vertex data structure.</span></span> <span data-ttu-id="302f3-153">Tamaño de *pVertDataLength*.</span><span class="sxs-lookup"><span data-stu-id="302f3-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-154">*pVertDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-155">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="302f3-156">Número de nuevos vértices en la malla dividida.</span><span class="sxs-lookup"><span data-stu-id="302f3-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="302f3-157">Asignada en la función.</span><span class="sxs-lookup"><span data-stu-id="302f3-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-158">*pSCClusterList* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-159">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="302f3-160">Matriz de longitud *NumCs* que *pSCData* indexa en (campos *pClusterIDs* \* ) para cada superclúster, contiene clústeres ordenados por supercluster.</span><span class="sxs-lookup"><span data-stu-id="302f3-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="302f3-161">*pSCData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="302f3-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="302f3-162">Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="302f3-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="302f3-163">Estructura por Super cluster.</span><span class="sxs-lookup"><span data-stu-id="302f3-163">Structure per super cluster.</span></span> <span data-ttu-id="302f3-164">Contiene índices en *ppIBData*, *pSCClusterList* y *ppVertData*.</span><span class="sxs-lookup"><span data-stu-id="302f3-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="302f3-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="302f3-165">Return value</span></span>

<span data-ttu-id="302f3-166">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="302f3-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="302f3-167">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="302f3-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="302f3-168">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="302f3-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="302f3-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="302f3-169">Requirements</span></span>



| <span data-ttu-id="302f3-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="302f3-170">Requirement</span></span> | <span data-ttu-id="302f3-171">Value</span><span class="sxs-lookup"><span data-stu-id="302f3-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="302f3-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="302f3-172">Header</span></span><br/>  | <dl> <span data-ttu-id="302f3-173"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="302f3-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="302f3-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="302f3-174">Library</span></span><br/> | <dl> <span data-ttu-id="302f3-175"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="302f3-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="302f3-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="302f3-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="302f3-177">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="302f3-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
