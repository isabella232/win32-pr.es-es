---
description: 'Método ID3DX10Mesh::Optimize: genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: Método ID3DX10Mesh::Optimize (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108053"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="fb45d-103">Método ID3DX10Mesh::Optimize</span><span class="sxs-lookup"><span data-stu-id="fb45d-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="fb45d-104">Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="fb45d-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb45d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb45d-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="fb45d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb45d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb45d-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fb45d-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb45d-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb45d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb45d-109">Especifica el tipo de optimización que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="fb45d-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="fb45d-110">Este parámetro se puede establecer en una combinación de una o varias marcas de D3DXMESHOPT y D3DXMESH (excepto D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY y D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="fb45d-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="fb45d-111">*pFaceRemap* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fb45d-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb45d-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb45d-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fb45d-113">Matriz de UINT, una por cara, que identifica la cara de malla original que corresponde a cada cara de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="fb45d-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="fb45d-114">Si el valor proporcionado para este argumento es **NULL,** no se devuelven los datos de reasignación de caras.</span><span class="sxs-lookup"><span data-stu-id="fb45d-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="fb45d-115">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb45d-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb45d-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="fb45d-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="fb45d-117">Dirección de un puntero a una interfaz [**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), que contiene un DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices antiguos.</span><span class="sxs-lookup"><span data-stu-id="fb45d-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="fb45d-118">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="fb45d-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb45d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb45d-119">Return value</span></span>

<span data-ttu-id="fb45d-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb45d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb45d-121">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="fb45d-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb45d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb45d-122">Remarks</span></span>

<span data-ttu-id="fb45d-123">Este método genera una nueva malla.</span><span class="sxs-lookup"><span data-stu-id="fb45d-123">This method generates a new mesh.</span></span> <span data-ttu-id="fb45d-124">Antes de ejecutar Optimize, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="fb45d-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="fb45d-125">El búfer de adyacencia contiene datos de adyacencia, como una lista de bordes y las caras adyacentes entre sí.</span><span class="sxs-lookup"><span data-stu-id="fb45d-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="fb45d-126">Este método es muy similar al método [**ID3DX10Mesh::CloneMesh,**](id3dx10mesh-clonemesh.md) salvo que puede realizar la optimización al generar el nuevo clon de la malla.</span><span class="sxs-lookup"><span data-stu-id="fb45d-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="fb45d-127">La malla de salida hereda todos los parámetros de creación de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="fb45d-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb45d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb45d-128">Requirements</span></span>



| <span data-ttu-id="fb45d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb45d-129">Requirement</span></span> | <span data-ttu-id="fb45d-130">Value</span><span class="sxs-lookup"><span data-stu-id="fb45d-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb45d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb45d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fb45d-132"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="fb45d-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb45d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb45d-133">Library</span></span><br/> | <dl> <span data-ttu-id="fb45d-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb45d-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb45d-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb45d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb45d-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="fb45d-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="fb45d-137">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="fb45d-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
