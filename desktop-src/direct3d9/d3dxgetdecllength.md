---
description: Devuelve el número de elementos en la declaración de vértice.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: Función D3DXGetDeclLength (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5576b4b86d5238d4942e09d605f695c66136799a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718197"
---
# <a name="d3dxgetdecllength-function"></a><span data-ttu-id="dd6b8-103">D3DXGetDeclLength función)</span><span class="sxs-lookup"><span data-stu-id="dd6b8-103">D3DXGetDeclLength function</span></span>

<span data-ttu-id="dd6b8-104">Devuelve el número de elementos en la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-104">Returns the number of elements in the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd6b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd6b8-105">Syntax</span></span>


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a><span data-ttu-id="dd6b8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd6b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd6b8-107">*pDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd6b8-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd6b8-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="dd6b8-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="dd6b8-109">Puntero a la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="dd6b8-110">Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="dd6b8-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd6b8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd6b8-111">Return value</span></span>

<span data-ttu-id="dd6b8-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd6b8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd6b8-113">El número de elementos en la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-113">The number of elements in the vertex declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6b8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd6b8-114">Requirements</span></span>



| <span data-ttu-id="dd6b8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd6b8-115">Requirement</span></span> | <span data-ttu-id="dd6b8-116">Value</span><span class="sxs-lookup"><span data-stu-id="dd6b8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6b8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd6b8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="dd6b8-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd6b8-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dd6b8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd6b8-119">Library</span></span><br/> | <dl> <span data-ttu-id="dd6b8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd6b8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd6b8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd6b8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6b8-122">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="dd6b8-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
