---
description: 'Función D3DXSHPRTCompSplitMeshSC: se usa con los resultados comprimidos de la versión de vértice del simulador de transferencia de radiaciones precalciadas (PRT).'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Función D3DXSHPRTCompSplitMeshSC (D3DX9Mesh.h)
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
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093903"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="40b36-103">Función D3DXSHPRTCompSplitMeshSC</span><span class="sxs-lookup"><span data-stu-id="40b36-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="40b36-104">Se usa con resultados comprimidos de la versión de vértice del simulador de transferencia de radiancia precalutada (PRT).</span><span class="sxs-lookup"><span data-stu-id="40b36-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="40b36-105">Después de llamar a [**D3DXSHPRTCompSuperCluster,**](d3dxshprtcompsupercluster.md) esta función se puede usar para dividir la malla en un grupo de caras o vértices por superclúster.</span><span class="sxs-lookup"><span data-stu-id="40b36-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="40b36-106">Cada superc cluster contiene todas las caras que contienen cualquier vértice clasificado en uno de sus clústeres.</span><span class="sxs-lookup"><span data-stu-id="40b36-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="40b36-107">Todos los vértices conectados a este conjunto de caras también se incluyen con la matriz ppVertStatus devuelta que indica si el vértice pertenece o no al super clúster.</span><span class="sxs-lookup"><span data-stu-id="40b36-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b36-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40b36-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="40b36-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40b36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40b36-110">*pClusterIDs* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="40b36-112">*Los IDs de clúster NumVertices* (extraídos de un búfer comprimido).</span><span class="sxs-lookup"><span data-stu-id="40b36-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="40b36-113">*NumVertices* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-115">Número de vértices en la malla original.</span><span class="sxs-lookup"><span data-stu-id="40b36-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-116">*NumCs* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-118">Número de clústeres (parámetro de entrada a compresión).</span><span class="sxs-lookup"><span data-stu-id="40b36-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="40b36-119">*pSClusterIDs* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-120">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="40b36-121">Matriz de *numcs de tamaño* que contendrá los valores de super cluster ID.</span><span class="sxs-lookup"><span data-stu-id="40b36-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-122">*NumSCs* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-124">Número de superclústeres asignados en [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="40b36-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b36-125">*pInputIB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-127">Búfer de índice sin procesar para mesh.</span><span class="sxs-lookup"><span data-stu-id="40b36-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="40b36-128">El formato depende de *InputIBIs32Bit.*</span><span class="sxs-lookup"><span data-stu-id="40b36-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-129">*InputIBIs32Bit* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-130">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-131">Si **es TRUE,** el búfer de índice se establece en 32 bits; de lo contrario, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="40b36-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-132">*NumFaces* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="40b36-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-133">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-134">Número de caras en la malla original *(pInputIB* es tres veces esta longitud).</span><span class="sxs-lookup"><span data-stu-id="40b36-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="40b36-135">*ppIBData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="40b36-137">Búfer de índice sin formato que contendrá las caras divididas resultantes.</span><span class="sxs-lookup"><span data-stu-id="40b36-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="40b36-138">Formato determinado por *InputIBIs32Bit.*</span><span class="sxs-lookup"><span data-stu-id="40b36-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="40b36-139">Asignado por función.</span><span class="sxs-lookup"><span data-stu-id="40b36-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-140">*pIBDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-141">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="40b36-142">Longitud de *ppIBData*, asignada en la función .</span><span class="sxs-lookup"><span data-stu-id="40b36-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-143">*OutputIBIs32Bit* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-144">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40b36-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40b36-145">Si **es TRUE,** asigna una matriz de enteros sin signo; de lo contrario, asigna una matriz corta sin signo.</span><span class="sxs-lookup"><span data-stu-id="40b36-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-146">*ppFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-147">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="40b36-148">Asignación de cada cara de *ppIBData* a caras originales.</span><span class="sxs-lookup"><span data-stu-id="40b36-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="40b36-149">La longitud \* *es pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="40b36-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-150">*ppVertData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="40b36-152">Nueva estructura de datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="40b36-152">New vertex data structure.</span></span> <span data-ttu-id="40b36-153">Tamaño de *pVertDataLength.*</span><span class="sxs-lookup"><span data-stu-id="40b36-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-154">*pVertDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-155">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="40b36-156">Número de nuevos vértices en malla dividida.</span><span class="sxs-lookup"><span data-stu-id="40b36-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="40b36-157">Se asigna en la función .</span><span class="sxs-lookup"><span data-stu-id="40b36-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-158">*pSCClusterList* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-159">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="40b36-160">Matriz de *numcs* de longitud en la que *pSCData* indexa *(campos pClusterIDs)* para cada superclúster, contiene clústeres \* ordenados por superclúster.</span><span class="sxs-lookup"><span data-stu-id="40b36-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="40b36-161">*pSCData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40b36-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b36-162">Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="40b36-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="40b36-163">Estructura por superc cluster.</span><span class="sxs-lookup"><span data-stu-id="40b36-163">Structure per super cluster.</span></span> <span data-ttu-id="40b36-164">Contiene índices en *ppIBData,* *pSCClusterList* y *ppVertData.*</span><span class="sxs-lookup"><span data-stu-id="40b36-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40b36-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40b36-165">Return value</span></span>

<span data-ttu-id="40b36-166">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40b36-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40b36-167">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40b36-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="40b36-168">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="40b36-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="40b36-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40b36-169">Requirements</span></span>



| <span data-ttu-id="40b36-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="40b36-170">Requirement</span></span> | <span data-ttu-id="40b36-171">Value</span><span class="sxs-lookup"><span data-stu-id="40b36-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40b36-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40b36-172">Header</span></span><br/>  | <dl> <span data-ttu-id="40b36-173"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="40b36-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="40b36-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40b36-174">Library</span></span><br/> | <dl> <span data-ttu-id="40b36-175"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="40b36-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40b36-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="40b36-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b36-177">Funciones de transferencia de radiancia precalcaladas</span><span class="sxs-lookup"><span data-stu-id="40b36-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
