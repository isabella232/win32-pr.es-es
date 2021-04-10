---
description: Agrega datos de adyacencia al búfer de índice de la malla. Cuando la malla se va a enviar a un sombreador de geometría que toma datos de adyacencias, es necesario que el búfer de índice de la malla contenga datos de adyacencia.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'ID3DX10Mesh:: GenerateGSAdjacency (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083760"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="ee0fc-104">ID3DX10Mesh:: GenerateGSAdjacency (método)</span><span class="sxs-lookup"><span data-stu-id="ee0fc-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="ee0fc-105">Agrega datos de adyacencia al búfer de índice de la malla.</span><span class="sxs-lookup"><span data-stu-id="ee0fc-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="ee0fc-106">Cuando la malla se va a enviar a un sombreador de geometría que toma datos de adyacencias, es necesario que el búfer de índice de la malla contenga datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="ee0fc-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee0fc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee0fc-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="ee0fc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee0fc-108">Parameters</span></span>

<span data-ttu-id="ee0fc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee0fc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee0fc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee0fc-110">Return value</span></span>

<span data-ttu-id="ee0fc-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee0fc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee0fc-112">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ee0fc-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee0fc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee0fc-113">Requirements</span></span>



| <span data-ttu-id="ee0fc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee0fc-114">Requirement</span></span> | <span data-ttu-id="ee0fc-115">Value</span><span class="sxs-lookup"><span data-stu-id="ee0fc-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0fc-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee0fc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ee0fc-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee0fc-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee0fc-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee0fc-118">Library</span></span><br/> | <dl> <span data-ttu-id="ee0fc-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee0fc-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee0fc-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee0fc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0fc-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ee0fc-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ee0fc-122">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="ee0fc-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




