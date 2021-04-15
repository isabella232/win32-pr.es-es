---
description: Calcula la esfera de límite de todas las mallas de la jerarquía de fotogramas.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Función D3DXFrameCalculateBoundingSphere (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707883"
---
# <a name="d3dxframecalculateboundingsphere-function"></a><span data-ttu-id="65b90-103">D3DXFrameCalculateBoundingSphere función)</span><span class="sxs-lookup"><span data-stu-id="65b90-103">D3DXFrameCalculateBoundingSphere function</span></span>

<span data-ttu-id="65b90-104">Calcula la esfera de límite de todas las mallas de la jerarquía de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="65b90-104">Computes the bounding sphere of all the meshes in the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b90-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65b90-105">Syntax</span></span>


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a><span data-ttu-id="65b90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65b90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b90-107">*pFrameRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65b90-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b90-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="65b90-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="65b90-109">Puntero al nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="65b90-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="65b90-110">*pObjectCenter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65b90-110">*pObjectCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b90-111">Tipo: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="65b90-111">Type: **[**LPD3DXVECTOR3**](d3dxvector3.md)**</span></span>

<span data-ttu-id="65b90-112">Devuelve el centro de la esfera de límite.</span><span class="sxs-lookup"><span data-stu-id="65b90-112">Returns the center of the bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="65b90-113">*pObjectRadius* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65b90-113">*pObjectRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b90-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="65b90-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="65b90-115">Devuelve el radio de la esfera de límite.</span><span class="sxs-lookup"><span data-stu-id="65b90-115">Returns the radius of the bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b90-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65b90-116">Return value</span></span>

<span data-ttu-id="65b90-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65b90-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65b90-118">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65b90-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65b90-119">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="65b90-119">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b90-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b90-120">Requirements</span></span>



| <span data-ttu-id="65b90-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b90-121">Requirement</span></span> | <span data-ttu-id="65b90-122">Value</span><span class="sxs-lookup"><span data-stu-id="65b90-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b90-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65b90-123">Header</span></span><br/>  | <dl> <span data-ttu-id="65b90-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b90-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="65b90-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65b90-125">Library</span></span><br/> | <dl> <span data-ttu-id="65b90-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65b90-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65b90-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="65b90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b90-128">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="65b90-128">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
