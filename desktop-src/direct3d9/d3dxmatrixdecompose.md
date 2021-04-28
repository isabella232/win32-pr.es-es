---
description: 'Función D3DXMatrixDecompose (D3dx9math.h): divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.'
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Función D3DXMatrixDecompose (D3dx9math.h)
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
ms.openlocfilehash: aaaa1059c4ffeafa453694d9c348656c856decaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098193"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="737f9-103">Función D3DXMatrixDecompose (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="737f9-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="737f9-104">Divide una matriz de transformación 3D general en sus componentes escalares, rotacionales y traslacionales.</span><span class="sxs-lookup"><span data-stu-id="737f9-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="737f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="737f9-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="737f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="737f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737f9-107">*pOutScale* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="737f9-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="737f9-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="737f9-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="737f9-109">Puntero a la [**salida D3DXVECTOR3**](d3dxvector3.md) que contiene los factores de escalado aplicados a lo largo de los ejes x, y y z.</span><span class="sxs-lookup"><span data-stu-id="737f9-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="737f9-110">*pOutRotation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="737f9-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="737f9-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="737f9-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="737f9-112">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que describe la rotación.</span><span class="sxs-lookup"><span data-stu-id="737f9-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="737f9-113">*pOutTranslation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="737f9-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="737f9-114">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="737f9-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="737f9-115">Puntero al vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traducción.</span><span class="sxs-lookup"><span data-stu-id="737f9-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="737f9-116">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="737f9-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="737f9-117">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="737f9-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="737f9-118">Puntero a una matriz [**D3DXMATRIX de**](d3dxmatrix.md) entrada para descomponer.</span><span class="sxs-lookup"><span data-stu-id="737f9-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737f9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="737f9-119">Return value</span></span>

<span data-ttu-id="737f9-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="737f9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="737f9-121">Si la función se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="737f9-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="737f9-122">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="737f9-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="737f9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="737f9-123">Requirements</span></span>



| <span data-ttu-id="737f9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="737f9-124">Requirement</span></span> | <span data-ttu-id="737f9-125">Value</span><span class="sxs-lookup"><span data-stu-id="737f9-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="737f9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="737f9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="737f9-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="737f9-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="737f9-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="737f9-128">Library</span></span><br/> | <dl> <span data-ttu-id="737f9-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="737f9-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="737f9-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="737f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737f9-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="737f9-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




