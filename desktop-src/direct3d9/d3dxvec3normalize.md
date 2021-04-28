---
description: 'Función D3DXVec3Normalize (D3dx9math.h): devuelve la versión normalizada de un vector 3D.'
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: Función D3DXVec3Normalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f39890a92bbff9d27a1150e76092d865dc36c089
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097833"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="22571-103">Función D3DXVec3Normalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="22571-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="22571-104">Devuelve la versión normalizada de un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="22571-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="22571-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22571-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="22571-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22571-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22571-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="22571-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22571-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="22571-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="22571-109">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="22571-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="22571-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="22571-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22571-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="22571-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="22571-112">Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="22571-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22571-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22571-113">Return value</span></span>

<span data-ttu-id="22571-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="22571-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="22571-115">Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es la versión normalizada del vector especificado.</span><span class="sxs-lookup"><span data-stu-id="22571-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="22571-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22571-116">Remarks</span></span>

<span data-ttu-id="22571-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="22571-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="22571-118">De esta manera, la **función D3DXVec3Normalize** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="22571-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22571-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22571-119">Requirements</span></span>



| <span data-ttu-id="22571-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="22571-120">Requirement</span></span> | <span data-ttu-id="22571-121">Value</span><span class="sxs-lookup"><span data-stu-id="22571-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22571-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22571-122">Header</span></span><br/>  | <dl> <span data-ttu-id="22571-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="22571-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="22571-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22571-124">Library</span></span><br/> | <dl> <span data-ttu-id="22571-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="22571-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22571-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22571-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22571-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="22571-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




