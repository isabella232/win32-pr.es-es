---
description: 'Función D3DXMatrixDecompose (D3DX10Math.h): divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.'
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Función D3DXMatrixDecompose (D3DX10Math.h)
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
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113213"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="69b2b-103">Función D3DXMatrixDecompose (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="69b2b-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="69b2b-104">Divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.</span><span class="sxs-lookup"><span data-stu-id="69b2b-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69b2b-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="69b2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69b2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b2b-107">*pOutScale* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69b2b-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b2b-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="69b2b-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69b2b-109">Puntero a la salida [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que contiene los factores de escalado aplicados a lo largo de los ejes x, y y z.</span><span class="sxs-lookup"><span data-stu-id="69b2b-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="69b2b-110">*pOutRotation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69b2b-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b2b-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="69b2b-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="69b2b-112">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que describe la rotación.</span><span class="sxs-lookup"><span data-stu-id="69b2b-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="69b2b-113">*pOutTranslation* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69b2b-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b2b-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="69b2b-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69b2b-115">Puntero al vector D3DXVECTOR3 que describe la traducción.</span><span class="sxs-lookup"><span data-stu-id="69b2b-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="69b2b-116">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69b2b-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b2b-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="69b2b-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="69b2b-118">Puntero a una matriz [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) entrada para descomponer.</span><span class="sxs-lookup"><span data-stu-id="69b2b-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b2b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69b2b-119">Return value</span></span>

<span data-ttu-id="69b2b-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69b2b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69b2b-121">Si la función se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69b2b-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="69b2b-122">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="69b2b-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b2b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b2b-123">Requirements</span></span>



| <span data-ttu-id="69b2b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b2b-124">Requirement</span></span> | <span data-ttu-id="69b2b-125">Value</span><span class="sxs-lookup"><span data-stu-id="69b2b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69b2b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69b2b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="69b2b-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="69b2b-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="69b2b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69b2b-128">Library</span></span><br/> | <dl> <span data-ttu-id="69b2b-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="69b2b-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69b2b-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69b2b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b2b-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="69b2b-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
