---
description: Busca el marco secundario de un fotograma raíz.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Función D3DXFrameFind (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718205"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="07d1d-103">D3DXFrameFind función)</span><span class="sxs-lookup"><span data-stu-id="07d1d-103">D3DXFrameFind function</span></span>

<span data-ttu-id="07d1d-104">Busca el marco secundario de un fotograma raíz.</span><span class="sxs-lookup"><span data-stu-id="07d1d-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07d1d-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="07d1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d1d-107">*pFrameRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="07d1d-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d1d-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="07d1d-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="07d1d-109">Puntero al marco raíz.</span><span class="sxs-lookup"><span data-stu-id="07d1d-109">Pointer to the root frame.</span></span> <span data-ttu-id="07d1d-110">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="07d1d-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d1d-111">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="07d1d-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d1d-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07d1d-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07d1d-113">Nombre del marco secundario que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="07d1d-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d1d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07d1d-114">Return value</span></span>

<span data-ttu-id="07d1d-115">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="07d1d-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="07d1d-116">Devuelve el marco secundario si se encuentra o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="07d1d-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="07d1d-117">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="07d1d-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07d1d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07d1d-118">Requirements</span></span>



| <span data-ttu-id="07d1d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d1d-119">Requirement</span></span> | <span data-ttu-id="07d1d-120">Value</span><span class="sxs-lookup"><span data-stu-id="07d1d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07d1d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07d1d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="07d1d-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d1d-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="07d1d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07d1d-123">Library</span></span><br/> | <dl> <span data-ttu-id="07d1d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07d1d-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07d1d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="07d1d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d1d-126">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="07d1d-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
