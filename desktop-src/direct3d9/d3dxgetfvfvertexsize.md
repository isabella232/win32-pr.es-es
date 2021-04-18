---
description: Devuelve el tamaño de un vértice para un formato de vértice flexible (FVF).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Función D3DXGetFVFVertexSize (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718192"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="1834b-103">D3DXGetFVFVertexSize función)</span><span class="sxs-lookup"><span data-stu-id="1834b-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="1834b-104">Devuelve el tamaño de un vértice para un formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="1834b-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="1834b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1834b-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="1834b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1834b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1834b-107">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1834b-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1834b-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1834b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1834b-109">FVF que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="1834b-109">FVF to be queried.</span></span> <span data-ttu-id="1834b-110">Combinación de [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="1834b-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1834b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1834b-111">Return value</span></span>

<span data-ttu-id="1834b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1834b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1834b-113">Tamaño del vértice de FVF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="1834b-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1834b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1834b-114">Requirements</span></span>



| <span data-ttu-id="1834b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1834b-115">Requirement</span></span> | <span data-ttu-id="1834b-116">Value</span><span class="sxs-lookup"><span data-stu-id="1834b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1834b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1834b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1834b-118"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1834b-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1834b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1834b-119">Library</span></span><br/> | <dl> <span data-ttu-id="1834b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1834b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1834b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1834b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1834b-122">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="1834b-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
