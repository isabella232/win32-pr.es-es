---
description: Calcula una esfera de límite para la malla.
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: Función D3DXComputeBoundingSphere (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c8e59b4d39652d02ce19f4c1bf6b0617fee7772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280444"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="1eaea-103">Función D3DXComputeBoundingSphere (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="1eaea-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="1eaea-104">Calcula una esfera de límite para la malla.</span><span class="sxs-lookup"><span data-stu-id="1eaea-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eaea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1eaea-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="1eaea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1eaea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eaea-107">*pFirstPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eaea-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaea-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eaea-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1eaea-109">Puntero a la primera posición.</span><span class="sxs-lookup"><span data-stu-id="1eaea-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="1eaea-110">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eaea-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaea-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eaea-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eaea-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="1eaea-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="1eaea-113">*dwStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eaea-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaea-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1eaea-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1eaea-115">Número de bytes entre los vectores de posición.</span><span class="sxs-lookup"><span data-stu-id="1eaea-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="1eaea-116">*pCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eaea-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaea-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eaea-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1eaea-118">Estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que define el centro de coordenadas de la esfera de límite devuelta.</span><span class="sxs-lookup"><span data-stu-id="1eaea-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="1eaea-119">*pRadius* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1eaea-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eaea-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eaea-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1eaea-121">Radio de la esfera de límite devuelta.</span><span class="sxs-lookup"><span data-stu-id="1eaea-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eaea-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1eaea-122">Return value</span></span>

<span data-ttu-id="1eaea-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1eaea-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1eaea-124">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1eaea-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1eaea-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1eaea-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eaea-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1eaea-126">Requirements</span></span>



| <span data-ttu-id="1eaea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eaea-127">Requirement</span></span> | <span data-ttu-id="1eaea-128">Value</span><span class="sxs-lookup"><span data-stu-id="1eaea-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eaea-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1eaea-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1eaea-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eaea-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="1eaea-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1eaea-131">Library</span></span><br/> | <dl> <span data-ttu-id="1eaea-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eaea-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eaea-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1eaea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eaea-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="1eaea-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
