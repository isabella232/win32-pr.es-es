---
description: Devuelve el tamaño de un vértice a partir de la declaración de vértice.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Función D3DXGetDeclVertexSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718195"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="50ccb-103">D3DXGetDeclVertexSize función)</span><span class="sxs-lookup"><span data-stu-id="50ccb-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="50ccb-104">Devuelve el tamaño de un vértice a partir de la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="50ccb-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ccb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50ccb-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="50ccb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50ccb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50ccb-107">*pDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50ccb-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ccb-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="50ccb-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="50ccb-109">Puntero a la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="50ccb-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="50ccb-110">Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="50ccb-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="50ccb-111">*Flujo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="50ccb-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50ccb-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50ccb-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50ccb-113">Índice de la secuencia de base cero.</span><span class="sxs-lookup"><span data-stu-id="50ccb-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50ccb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50ccb-114">Return value</span></span>

<span data-ttu-id="50ccb-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50ccb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50ccb-116">Tamaño de la declaración de vértices, en bytes.</span><span class="sxs-lookup"><span data-stu-id="50ccb-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ccb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50ccb-117">Requirements</span></span>



| <span data-ttu-id="50ccb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="50ccb-118">Requirement</span></span> | <span data-ttu-id="50ccb-119">Value</span><span class="sxs-lookup"><span data-stu-id="50ccb-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50ccb-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50ccb-120">Header</span></span><br/>  | <dl> <span data-ttu-id="50ccb-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="50ccb-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="50ccb-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50ccb-122">Library</span></span><br/> | <dl> <span data-ttu-id="50ccb-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50ccb-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50ccb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="50ccb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ccb-125">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="50ccb-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
