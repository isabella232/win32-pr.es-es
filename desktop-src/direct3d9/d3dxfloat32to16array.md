---
description: 'Función D3DXFloat32To16Array (D3dx9math.h): convierte una matriz de flotantes de 32 bits en flotantes de 16 bits.'
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: Función D3DXFloat32To16Array (D3dx9math.h)
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
ms.openlocfilehash: dc00df150c48e285d5478eb9b11df6c5203d6bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094263"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="e6d3d-103">Función D3DXFloat32To16Array (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e6d3d-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="e6d3d-104">Convierte una matriz de flotantes de 32 bits en flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e6d3d-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6d3d-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="e6d3d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6d3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d3d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e6d3d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d3d-108">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6d3d-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="e6d3d-109">Puntero a la matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e6d3d-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="e6d3d-110">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e6d3d-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d3d-111">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6d3d-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e6d3d-112">Puntero a una matriz de flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e6d3d-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="e6d3d-113">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e6d3d-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d3d-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6d3d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6d3d-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e6d3d-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d3d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6d3d-116">Return value</span></span>

<span data-ttu-id="e6d3d-117">Tipo: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6d3d-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="e6d3d-118">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e6d3d-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d3d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d3d-119">Requirements</span></span>



| <span data-ttu-id="e6d3d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d3d-120">Requirement</span></span> | <span data-ttu-id="e6d3d-121">Value</span><span class="sxs-lookup"><span data-stu-id="e6d3d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d3d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6d3d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e6d3d-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e6d3d-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e6d3d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6d3d-124">Library</span></span><br/> | <dl> <span data-ttu-id="e6d3d-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6d3d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6d3d-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e6d3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d3d-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e6d3d-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
