---
description: Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh:: GenerateAdjacencyAndPointReps (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548014"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="cd989-103">ID3DX10Mesh:: GenerateAdjacencyAndPointReps (método)</span><span class="sxs-lookup"><span data-stu-id="cd989-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="cd989-104">Generar una lista de bordes de la malla, así como una lista de caras que comparten cada borde.</span><span class="sxs-lookup"><span data-stu-id="cd989-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd989-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd989-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="cd989-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd989-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd989-107">*Épsilon* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd989-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd989-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd989-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd989-109">Especifica que los vértices que difieren en la posición inferior al épsilon se deben tratar como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="cd989-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd989-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd989-110">Return value</span></span>

<span data-ttu-id="cd989-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd989-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd989-112">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cd989-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd989-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd989-113">Remarks</span></span>

<span data-ttu-id="cd989-114">Una vez que una aplicación genera información de adyacencias para una malla, los datos de la malla pueden optimizarse para mejorar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="cd989-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="cd989-115">El orden de las entradas en el búfer de adyacencia viene determinado por el orden de los índices de vértice en el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="cd989-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="cd989-116">El triángulo 0 adyacente siempre corresponde al borde entre los índices de las esquinas 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="cd989-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="cd989-117">El triángulo 1 adyacente siempre corresponde al borde entre los índices de las esquinas 1 y 2, mientras que el triángulo 2 adyacente se corresponde con el borde entre los índices de las esquinas 2 y 0.</span><span class="sxs-lookup"><span data-stu-id="cd989-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd989-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd989-118">Requirements</span></span>



| <span data-ttu-id="cd989-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd989-119">Requirement</span></span> | <span data-ttu-id="cd989-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd989-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd989-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd989-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cd989-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd989-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd989-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd989-123">Library</span></span><br/> | <dl> <span data-ttu-id="cd989-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd989-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd989-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd989-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd989-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="cd989-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="cd989-127">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="cd989-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
