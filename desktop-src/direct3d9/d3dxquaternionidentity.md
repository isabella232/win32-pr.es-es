---
description: Devuelve el cuaternión de identidad.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: Función D3DXQuaternionIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362528"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="f9a35-103">D3DXQuaternionIdentity función)</span><span class="sxs-lookup"><span data-stu-id="f9a35-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="f9a35-104">Devuelve el cuaternión de identidad.</span><span class="sxs-lookup"><span data-stu-id="f9a35-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a35-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9a35-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="f9a35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9a35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a35-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9a35-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a35-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9a35-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f9a35-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f9a35-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a35-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9a35-110">Return value</span></span>

<span data-ttu-id="f9a35-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9a35-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f9a35-112">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el cuaternión de identidad.</span><span class="sxs-lookup"><span data-stu-id="f9a35-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9a35-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9a35-113">Remarks</span></span>

<span data-ttu-id="f9a35-114">Dado un cuaternión (x, y, z, w), la función **D3DXQuaternionIdentity** devolverá el cuaternión (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="f9a35-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="f9a35-115">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="f9a35-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f9a35-116">De esta manera, la función **D3DXQuaternionIdentity** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="f9a35-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f9a35-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="f9a35-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a35-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9a35-118">Requirements</span></span>



| <span data-ttu-id="f9a35-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9a35-119">Requirement</span></span> | <span data-ttu-id="f9a35-120">Value</span><span class="sxs-lookup"><span data-stu-id="f9a35-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a35-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9a35-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f9a35-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a35-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f9a35-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9a35-123">Library</span></span><br/> | <dl> <span data-ttu-id="f9a35-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9a35-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f9a35-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9a35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a35-126">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f9a35-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f9a35-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="f9a35-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




