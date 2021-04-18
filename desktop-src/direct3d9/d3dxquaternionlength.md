---
description: Devuelve la longitud de un cuaternión.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: Función D3DXQuaternionLength (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424480"
---
# <a name="d3dxquaternionlength-function"></a><span data-ttu-id="abf83-103">D3DXQuaternionLength función)</span><span class="sxs-lookup"><span data-stu-id="abf83-103">D3DXQuaternionLength function</span></span>

<span data-ttu-id="abf83-104">Devuelve la longitud de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="abf83-104">Returns the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf83-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abf83-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="abf83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abf83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf83-107">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abf83-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abf83-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="abf83-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="abf83-109">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="abf83-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf83-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abf83-110">Return value</span></span>

<span data-ttu-id="abf83-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abf83-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abf83-112">Longitud del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="abf83-112">The quaternion's length.</span></span>

## <a name="remarks"></a><span data-ttu-id="abf83-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abf83-113">Remarks</span></span>

<span data-ttu-id="abf83-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="abf83-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="abf83-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abf83-115">Requirements</span></span>



| <span data-ttu-id="abf83-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abf83-116">Requirement</span></span> | <span data-ttu-id="abf83-117">Value</span><span class="sxs-lookup"><span data-stu-id="abf83-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abf83-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abf83-118">Header</span></span><br/>  | <dl> <span data-ttu-id="abf83-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf83-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="abf83-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abf83-120">Library</span></span><br/> | <dl> <span data-ttu-id="abf83-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abf83-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abf83-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="abf83-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf83-123">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="abf83-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="abf83-124">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="abf83-124">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
