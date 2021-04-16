---
description: Proyecta una función representada en un mapa de cubo en armónicos esféricos.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Función D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689888"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="3a224-103">D3DX10SHProjectCubeMap función)</span><span class="sxs-lookup"><span data-stu-id="3a224-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="3a224-104">Proyecta una función representada en un mapa de cubo en armónicos esféricos.</span><span class="sxs-lookup"><span data-stu-id="3a224-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a224-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a224-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="3a224-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a224-107">*Pedido*</span><span class="sxs-lookup"><span data-stu-id="3a224-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="3a224-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a224-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a224-109">Orden de la evaluación de SH, genera el orden ^ 2 coefs, Degree es el orden 1.</span><span class="sxs-lookup"><span data-stu-id="3a224-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="3a224-110">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="3a224-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="3a224-111">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="3a224-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="3a224-112">Mapa que se va a proyectar en armónicos esféricos.</span><span class="sxs-lookup"><span data-stu-id="3a224-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="3a224-113">Vea [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="3a224-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="3a224-114">*pROut*</span><span class="sxs-lookup"><span data-stu-id="3a224-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="3a224-115">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a224-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3a224-116">Salida SH vector para rojo.</span><span class="sxs-lookup"><span data-stu-id="3a224-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="3a224-117">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="3a224-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="3a224-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a224-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3a224-119">Salida SH vector para verde.</span><span class="sxs-lookup"><span data-stu-id="3a224-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="3a224-120">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="3a224-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="3a224-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a224-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3a224-122">Salida SH vector para azul.</span><span class="sxs-lookup"><span data-stu-id="3a224-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a224-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a224-123">Return value</span></span>

<span data-ttu-id="3a224-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a224-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a224-125">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3a224-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a224-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a224-126">Requirements</span></span>



| <span data-ttu-id="3a224-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a224-127">Requirement</span></span> | <span data-ttu-id="3a224-128">Value</span><span class="sxs-lookup"><span data-stu-id="3a224-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a224-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a224-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3a224-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a224-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3a224-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a224-131">Library</span></span><br/> | <dl> <span data-ttu-id="3a224-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a224-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3a224-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a224-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a224-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3a224-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
