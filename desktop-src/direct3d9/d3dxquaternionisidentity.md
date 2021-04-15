---
description: Determina si un cuaternión es un cuaternión de identidad.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Función D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708021"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="1d392-103">D3DXQuaternionIsIdentity función)</span><span class="sxs-lookup"><span data-stu-id="1d392-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="1d392-104">Determina si un cuaternión es un cuaternión de identidad.</span><span class="sxs-lookup"><span data-stu-id="1d392-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d392-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d392-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="1d392-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d392-107">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d392-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d392-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d392-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1d392-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) cuya identidad se probará.</span><span class="sxs-lookup"><span data-stu-id="1d392-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d392-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d392-110">Return value</span></span>

<span data-ttu-id="1d392-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d392-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d392-112">Si el cuaternión es un cuaternión de identidad, esta función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="1d392-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="1d392-113">De lo contrario, esta función devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1d392-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d392-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d392-114">Remarks</span></span>

<span data-ttu-id="1d392-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="1d392-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d392-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d392-116">Requirements</span></span>



| <span data-ttu-id="1d392-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d392-117">Requirement</span></span> | <span data-ttu-id="1d392-118">Value</span><span class="sxs-lookup"><span data-stu-id="1d392-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d392-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d392-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1d392-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d392-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1d392-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d392-121">Library</span></span><br/> | <dl> <span data-ttu-id="1d392-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d392-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d392-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d392-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d392-124">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1d392-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1d392-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="1d392-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 
