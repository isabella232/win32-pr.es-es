---
description: Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Método ID3DX10Mesh:: Optimize (D3DX10. h)'
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
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362654"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="1357e-103">ID3DX10Mesh:: Optimize (método)</span><span class="sxs-lookup"><span data-stu-id="1357e-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="1357e-104">Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="1357e-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="1357e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1357e-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="1357e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1357e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1357e-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1357e-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1357e-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1357e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1357e-109">Especifica el tipo de optimización que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="1357e-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="1357e-110">Este parámetro se puede establecer en una combinación de una o varias marcas de D3DXMESHOPT y D3DXMESH (excepto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WRITEONLY y D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="1357e-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="1357e-111">*pFaceRemap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1357e-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1357e-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1357e-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1357e-113">Matriz de UINT, uno por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="1357e-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="1357e-114">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.</span><span class="sxs-lookup"><span data-stu-id="1357e-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="1357e-115">*ppVertexRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1357e-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1357e-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="1357e-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="1357e-117">Dirección de un puntero a una [**interfaz ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores.</span><span class="sxs-lookup"><span data-stu-id="1357e-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="1357e-118">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="1357e-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1357e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1357e-119">Return value</span></span>

<span data-ttu-id="1357e-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1357e-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1357e-121">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1357e-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1357e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1357e-122">Remarks</span></span>

<span data-ttu-id="1357e-123">Este método genera una nueva malla.</span><span class="sxs-lookup"><span data-stu-id="1357e-123">This method generates a new mesh.</span></span> <span data-ttu-id="1357e-124">Antes de ejecutar optimizar, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DX10Mesh:: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="1357e-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="1357e-125">El búfer de adyacencia contiene datos de adyacencias, como una lista de bordes y las caras adyacentes entre sí.</span><span class="sxs-lookup"><span data-stu-id="1357e-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="1357e-126">Este método es muy similar al método [**ID3DX10Mesh:: CloneMesh**](id3dx10mesh-clonemesh.md) , salvo que puede realizar la optimización mientras genera el nuevo clon de la malla.</span><span class="sxs-lookup"><span data-stu-id="1357e-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="1357e-127">La malla de salida hereda todos los parámetros de creación de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="1357e-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="1357e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1357e-128">Requirements</span></span>



| <span data-ttu-id="1357e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1357e-129">Requirement</span></span> | <span data-ttu-id="1357e-130">Value</span><span class="sxs-lookup"><span data-stu-id="1357e-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1357e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1357e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1357e-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1357e-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1357e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1357e-133">Library</span></span><br/> | <dl> <span data-ttu-id="1357e-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1357e-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1357e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1357e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1357e-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="1357e-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="1357e-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="1357e-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
