---
description: Cuenta el número de fotogramas de un subárbol que tienen nombres no nulos.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: Función D3DXFrameNumNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003816"
---
# <a name="d3dxframenumnamedmatrices-function"></a><span data-ttu-id="2656c-103">D3DXFrameNumNamedMatrices función)</span><span class="sxs-lookup"><span data-stu-id="2656c-103">D3DXFrameNumNamedMatrices function</span></span>

<span data-ttu-id="2656c-104">Cuenta el número de fotogramas de un subárbol que tienen nombres no nulos.</span><span class="sxs-lookup"><span data-stu-id="2656c-104">Counts number of frames in a subtree that have non-null names.</span></span>

## <a name="syntax"></a><span data-ttu-id="2656c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2656c-105">Syntax</span></span>


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a><span data-ttu-id="2656c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2656c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2656c-107">*pFrameRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2656c-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2656c-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="2656c-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="2656c-109">Puntero al nodo raíz del subárbol.</span><span class="sxs-lookup"><span data-stu-id="2656c-109">Pointer to the root node of the subtree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2656c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2656c-110">Return value</span></span>

<span data-ttu-id="2656c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2656c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2656c-112">Devuelve el número de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2656c-112">Returns the frame count.</span></span>

## <a name="requirements"></a><span data-ttu-id="2656c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2656c-113">Requirements</span></span>



| <span data-ttu-id="2656c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2656c-114">Requirement</span></span> | <span data-ttu-id="2656c-115">Value</span><span class="sxs-lookup"><span data-stu-id="2656c-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2656c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2656c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2656c-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2656c-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2656c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2656c-118">Library</span></span><br/> | <dl> <span data-ttu-id="2656c-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2656c-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2656c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2656c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2656c-121">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="2656c-121">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
