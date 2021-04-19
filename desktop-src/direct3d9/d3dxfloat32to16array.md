---
description: Convierte una matriz de tipos Float de 32 bits en flotantes de 16 bits.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Función D3DXFloat32To16Array (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721458"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="359b5-103">Función D3DXFloat32To16Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="359b5-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="359b5-104">Convierte una matriz de tipos Float de 32 bits en flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="359b5-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="359b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="359b5-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="359b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="359b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="359b5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="359b5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="359b5-108">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="359b5-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="359b5-109">Puntero a la matriz de los flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="359b5-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="359b5-110">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="359b5-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="359b5-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="359b5-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="359b5-112">Puntero a una matriz de floats de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="359b5-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="359b5-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="359b5-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="359b5-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="359b5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="359b5-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="359b5-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="359b5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="359b5-116">Return value</span></span>

<span data-ttu-id="359b5-117">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="359b5-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="359b5-118">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="359b5-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="359b5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="359b5-119">Requirements</span></span>



| <span data-ttu-id="359b5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="359b5-120">Requirement</span></span> | <span data-ttu-id="359b5-121">Value</span><span class="sxs-lookup"><span data-stu-id="359b5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="359b5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="359b5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="359b5-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="359b5-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="359b5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="359b5-124">Library</span></span><br/> | <dl> <span data-ttu-id="359b5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="359b5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="359b5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="359b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359b5-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="359b5-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
