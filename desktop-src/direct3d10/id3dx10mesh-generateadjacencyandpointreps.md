---
description: 'Método ID3DX10Mesh::GenerateAdjacencyAndPointReps: genera una lista de bordes de malla, así como una lista de caras que comparten cada borde.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: Método ID3DX10Mesh::GenerateAdjacencyAndPointReps (D3DX10.h)
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
ms.openlocfilehash: e496f96f36805d411c71e9aba1e2560b0dcbe3c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083983"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="3bbc1-103">Método ID3DX10Mesh::GenerateAdjacencyAndPointReps</span><span class="sxs-lookup"><span data-stu-id="3bbc1-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="3bbc1-104">Genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.</span><span class="sxs-lookup"><span data-stu-id="3bbc1-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbc1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bbc1-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="3bbc1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bbc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbc1-107">*Epsilon* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3bbc1-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbc1-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bbc1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bbc1-109">Especifica que los vértices que difieren en posición por menos de epsilon deben tratarse como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="3bbc1-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbc1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bbc1-110">Return value</span></span>

<span data-ttu-id="3bbc1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bbc1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bbc1-112">El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="3bbc1-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbc1-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bbc1-113">Remarks</span></span>

<span data-ttu-id="3bbc1-114">Una vez que una aplicación genera información de adyacencia para una malla, los datos de la malla se pueden optimizar para mejorar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="3bbc1-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="3bbc1-115">El orden de las entradas del búfer de adyacencia viene determinado por el orden de los índices de vértices en el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="3bbc1-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="3bbc1-116">El triángulo adyacente 0 siempre se corresponde con el borde entre los índices de las esquinas 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="3bbc1-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="3bbc1-117">El triángulo adyacente 1 siempre se corresponde con el borde entre los índices de las esquinas 1 y 2, mientras que el triángulo adyacente 2 se corresponde con el borde entre los índices de las esquinas 2 y 0.</span><span class="sxs-lookup"><span data-stu-id="3bbc1-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbc1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bbc1-118">Requirements</span></span>



| <span data-ttu-id="3bbc1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bbc1-119">Requirement</span></span> | <span data-ttu-id="3bbc1-120">Value</span><span class="sxs-lookup"><span data-stu-id="3bbc1-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbc1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bbc1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3bbc1-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="3bbc1-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3bbc1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bbc1-123">Library</span></span><br/> | <dl> <span data-ttu-id="3bbc1-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bbc1-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bbc1-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3bbc1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbc1-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3bbc1-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3bbc1-127">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="3bbc1-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
