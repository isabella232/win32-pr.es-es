---
description: Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Función D3DXMatrixDecompose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280471"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="1d0a3-103">Función D3DXMatrixDecompose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1d0a3-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="1d0a3-104">Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d0a3-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1d0a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d0a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0a3-107">*pOutScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d0a3-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0a3-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d0a3-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1d0a3-109">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) de salida que contiene los factores de escala que se aplican a lo largo de los ejes x, y y z.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="1d0a3-110">*pOutRotation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d0a3-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0a3-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d0a3-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1d0a3-112">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que describe la rotación.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="1d0a3-113">*pOutTranslation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d0a3-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0a3-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d0a3-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1d0a3-115">Puntero al vector D3DXVECTOR3 que describe la traducción.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="1d0a3-116">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d0a3-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0a3-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d0a3-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1d0a3-118">Puntero a una matriz de entrada [**D3DXMATRIX**](d3d10-d3dxmatrix.md) para descomponer.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0a3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d0a3-119">Return value</span></span>

<span data-ttu-id="1d0a3-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d0a3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d0a3-121">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1d0a3-122">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1d0a3-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0a3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d0a3-123">Requirements</span></span>



| <span data-ttu-id="1d0a3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0a3-124">Requirement</span></span> | <span data-ttu-id="1d0a3-125">Value</span><span class="sxs-lookup"><span data-stu-id="1d0a3-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0a3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d0a3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1d0a3-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d0a3-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1d0a3-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d0a3-128">Library</span></span><br/> | <dl> <span data-ttu-id="1d0a3-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d0a3-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d0a3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d0a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0a3-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1d0a3-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
