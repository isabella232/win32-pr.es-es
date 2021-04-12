---
description: Devuelve el producto de punto de dos cuaterniones.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: Función D3DXQuaternionDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362703"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="cea2c-103">D3DXQuaternionDot función)</span><span class="sxs-lookup"><span data-stu-id="cea2c-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="cea2c-104">Devuelve el producto de punto de dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="cea2c-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cea2c-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="cea2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cea2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea2c-107">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea2c-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cea2c-109">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="cea2c-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cea2c-110">*pQ2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cea2c-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea2c-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cea2c-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cea2c-112">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="cea2c-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea2c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cea2c-113">Return value</span></span>

<span data-ttu-id="cea2c-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cea2c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cea2c-115">Producto de punto de dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="cea2c-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea2c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cea2c-116">Remarks</span></span>

<span data-ttu-id="cea2c-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="cea2c-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea2c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea2c-118">Requirements</span></span>



| <span data-ttu-id="cea2c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea2c-119">Requirement</span></span> | <span data-ttu-id="cea2c-120">Value</span><span class="sxs-lookup"><span data-stu-id="cea2c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea2c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cea2c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cea2c-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea2c-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cea2c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cea2c-123">Library</span></span><br/> | <dl> <span data-ttu-id="cea2c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cea2c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cea2c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cea2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea2c-126">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="cea2c-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
