---
description: Obtiene el número de vértices en la malla.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh:: GetVertexCount (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707985"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="28b66-103">ID3DX10Mesh:: GetVertexCount (método)</span><span class="sxs-lookup"><span data-stu-id="28b66-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="28b66-104">Obtiene el número de vértices en la malla.</span><span class="sxs-lookup"><span data-stu-id="28b66-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="28b66-105">Una malla puede contener varios búferes de vértices (es decir, un búfer de vértices puede contener todos los datos de posición, otro puede contener todos los datos de coordenadas de textura, etc.); sin embargo, cada búfer de vértice contendrá el mismo número de elementos.</span><span class="sxs-lookup"><span data-stu-id="28b66-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b66-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28b66-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="28b66-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28b66-107">Parameters</span></span>

<span data-ttu-id="28b66-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28b66-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28b66-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28b66-109">Return value</span></span>

<span data-ttu-id="28b66-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28b66-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28b66-111">El número de vértices en la malla.</span><span class="sxs-lookup"><span data-stu-id="28b66-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b66-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28b66-112">Requirements</span></span>



| <span data-ttu-id="28b66-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="28b66-113">Requirement</span></span> | <span data-ttu-id="28b66-114">Value</span><span class="sxs-lookup"><span data-stu-id="28b66-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28b66-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28b66-115">Header</span></span><br/>  | <dl> <span data-ttu-id="28b66-116"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="28b66-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="28b66-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28b66-117">Library</span></span><br/> | <dl> <span data-ttu-id="28b66-118"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28b66-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28b66-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="28b66-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b66-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="28b66-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="28b66-121">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="28b66-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
