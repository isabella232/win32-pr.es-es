---
description: Proyecta una función representada en un mapa de cubo en armónicos esféricos (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: Función D3DXSHProjectCubeMap (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718418"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="23827-103">D3DXSHProjectCubeMap función)</span><span class="sxs-lookup"><span data-stu-id="23827-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="23827-104">Proyecta una función representada en un mapa de cubo en armónicos esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="23827-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="23827-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23827-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="23827-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23827-107">*Pedido* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="23827-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23827-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23827-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23827-109">Orden de evaluación de armónicos esférico (SH).</span><span class="sxs-lookup"><span data-stu-id="23827-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="23827-110">Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="23827-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="23827-111">La evaluación genera coeficientes de pedido ².</span><span class="sxs-lookup"><span data-stu-id="23827-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="23827-112">El grado de evaluación es order-1.</span><span class="sxs-lookup"><span data-stu-id="23827-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="23827-113">*pCubeMap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23827-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23827-114">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="23827-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="23827-115">Puntero a una textura del cubo de origen.</span><span class="sxs-lookup"><span data-stu-id="23827-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="23827-116">Vea [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span><span class="sxs-lookup"><span data-stu-id="23827-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="23827-117">*pROut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23827-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23827-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="23827-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23827-119">Puntero al vector SH de salida para el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="23827-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="23827-120">*pGOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23827-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23827-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="23827-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23827-122">Puntero al vector SH de salida del componente verde.</span><span class="sxs-lookup"><span data-stu-id="23827-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="23827-123">*pBOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23827-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23827-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="23827-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23827-125">Puntero al vector SH de salida para el componente azul.</span><span class="sxs-lookup"><span data-stu-id="23827-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23827-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23827-126">Return value</span></span>

<span data-ttu-id="23827-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23827-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23827-128">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23827-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23827-129">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="23827-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="23827-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23827-130">Requirements</span></span>



| <span data-ttu-id="23827-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="23827-131">Requirement</span></span> | <span data-ttu-id="23827-132">Value</span><span class="sxs-lookup"><span data-stu-id="23827-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23827-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23827-133">Header</span></span><br/>  | <dl> <span data-ttu-id="23827-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="23827-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="23827-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23827-135">Library</span></span><br/> | <dl> <span data-ttu-id="23827-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23827-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23827-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="23827-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23827-138">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="23827-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="23827-139">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23827-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
