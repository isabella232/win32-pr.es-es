---
description: Compila una matriz usando los desplazamientos especificados.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: Función D3DXMatrixTranslation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362556"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="14519-103">Función D3DXMatrixTranslation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="14519-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="14519-104">Compila una matriz usando los desplazamientos especificados.</span><span class="sxs-lookup"><span data-stu-id="14519-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="14519-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14519-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="14519-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14519-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14519-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="14519-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14519-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="14519-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="14519-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="14519-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="14519-110">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="14519-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14519-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14519-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14519-112">Desplazamiento de la coordenada X.</span><span class="sxs-lookup"><span data-stu-id="14519-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="14519-113">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="14519-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14519-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14519-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14519-115">Desplazamiento de la coordenada Y.</span><span class="sxs-lookup"><span data-stu-id="14519-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="14519-116">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="14519-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14519-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14519-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14519-118">Desplazamiento de la coordenada Z.</span><span class="sxs-lookup"><span data-stu-id="14519-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14519-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14519-119">Return value</span></span>

<span data-ttu-id="14519-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="14519-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="14519-121">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene una matriz de transformación traducida.</span><span class="sxs-lookup"><span data-stu-id="14519-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="14519-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14519-122">Remarks</span></span>

<span data-ttu-id="14519-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="14519-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="14519-124">De esta manera, D3DXMATRIXTranslation se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="14519-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14519-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14519-125">Requirements</span></span>



| <span data-ttu-id="14519-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="14519-126">Requirement</span></span> | <span data-ttu-id="14519-127">Value</span><span class="sxs-lookup"><span data-stu-id="14519-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14519-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14519-128">Header</span></span><br/>  | <dl> <span data-ttu-id="14519-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="14519-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="14519-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14519-130">Library</span></span><br/> | <dl> <span data-ttu-id="14519-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14519-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14519-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="14519-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14519-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="14519-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
