---
description: Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Función D3DXMatrixDecompose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698344"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="73d95-103">Función D3DXMatrixDecompose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="73d95-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="73d95-104">Divide una matriz de transformación 3D general en sus componentes escalares, de rotación y de conversión.</span><span class="sxs-lookup"><span data-stu-id="73d95-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73d95-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="73d95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73d95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73d95-107">*pOutScale* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73d95-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73d95-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="73d95-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="73d95-109">Puntero al [**D3DXVECTOR3**](d3dxvector3.md) de salida que contiene los factores de escala que se aplican a lo largo de los ejes x, y y z.</span><span class="sxs-lookup"><span data-stu-id="73d95-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="73d95-110">*pOutRotation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73d95-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73d95-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="73d95-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="73d95-112">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que describe la rotación.</span><span class="sxs-lookup"><span data-stu-id="73d95-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="73d95-113">*pOutTranslation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73d95-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73d95-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="73d95-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="73d95-115">Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traducción.</span><span class="sxs-lookup"><span data-stu-id="73d95-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="73d95-116">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73d95-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73d95-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="73d95-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="73d95-118">Puntero a una matriz de entrada [**D3DXMATRIX**](d3dxmatrix.md) para descomponer.</span><span class="sxs-lookup"><span data-stu-id="73d95-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73d95-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73d95-119">Return value</span></span>

<span data-ttu-id="73d95-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73d95-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73d95-121">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73d95-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="73d95-122">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="73d95-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d95-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73d95-123">Requirements</span></span>



| <span data-ttu-id="73d95-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d95-124">Requirement</span></span> | <span data-ttu-id="73d95-125">Value</span><span class="sxs-lookup"><span data-stu-id="73d95-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73d95-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73d95-126">Header</span></span><br/>  | <dl> <span data-ttu-id="73d95-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="73d95-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="73d95-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73d95-128">Library</span></span><br/> | <dl> <span data-ttu-id="73d95-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73d95-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73d95-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="73d95-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d95-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="73d95-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




