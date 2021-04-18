---
description: Devuelve el cuadrado de la longitud de un cuaternión.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Función D3DXQuaternionLengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718423"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="6ff84-103">D3DXQuaternionLengthSq función)</span><span class="sxs-lookup"><span data-stu-id="6ff84-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="6ff84-104">Devuelve el cuadrado de la longitud de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="6ff84-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ff84-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="6ff84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ff84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff84-107">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ff84-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff84-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ff84-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6ff84-109">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="6ff84-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff84-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ff84-110">Return value</span></span>

<span data-ttu-id="6ff84-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ff84-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ff84-112">Longitud cuadrada del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="6ff84-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff84-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ff84-113">Remarks</span></span>

<span data-ttu-id="6ff84-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="6ff84-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff84-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ff84-115">Requirements</span></span>



| <span data-ttu-id="6ff84-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff84-116">Requirement</span></span> | <span data-ttu-id="6ff84-117">Value</span><span class="sxs-lookup"><span data-stu-id="6ff84-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff84-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ff84-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6ff84-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff84-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6ff84-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ff84-120">Library</span></span><br/> | <dl> <span data-ttu-id="6ff84-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ff84-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ff84-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ff84-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff84-123">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6ff84-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6ff84-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="6ff84-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 
