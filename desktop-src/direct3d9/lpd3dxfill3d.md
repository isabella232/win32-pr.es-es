---
description: 'LPD3DXFILL3D: tipo de función utilizado por las funciones de relleno de textura.'
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed5845f04486a6ac9cf1c984178fb0ed98447a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342770"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="c9832-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="c9832-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="c9832-104">Tipo de función utilizado por las funciones de relleno de textura.</span><span class="sxs-lookup"><span data-stu-id="c9832-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9832-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9832-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="c9832-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9832-106">Parameters</span></span>

<span data-ttu-id="c9832-107">pOut: puntero a un vector, que la función usa para devolver su resultado.</span><span class="sxs-lookup"><span data-stu-id="c9832-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="c9832-108">X, Y, Z y W se asignarán a R, G, B y A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c9832-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="c9832-109">pTexCoord: puntero a un vector que contiene las coordenadas del texel que se está evaluando actualmente.</span><span class="sxs-lookup"><span data-stu-id="c9832-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="c9832-110">Los componentes de coordenadas de textura para texturas y texturas de volumen oscilan entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="c9832-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="c9832-111">Los componentes de coordenadas de textura para texturas de cubo oscilan entre -1 y 1.</span><span class="sxs-lookup"><span data-stu-id="c9832-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="c9832-112">pTexelSize: puntero a un vector que contiene las dimensiones del texel actual.</span><span class="sxs-lookup"><span data-stu-id="c9832-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="c9832-113">pData: puntero a datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="c9832-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9832-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9832-114">Return Value</span></span>

<span data-ttu-id="c9832-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c9832-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9832-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9832-116">Remarks</span></span>

<span data-ttu-id="c9832-117">Asegúrese de especificar la convención de llamada de tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c9832-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="c9832-118">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="c9832-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="c9832-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9832-119">Requirement</span></span>                         | <span data-ttu-id="c9832-120">Value</span><span class="sxs-lookup"><span data-stu-id="c9832-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c9832-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9832-121">Header</span></span>                   | <span data-ttu-id="c9832-122">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="c9832-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="c9832-123">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="c9832-123">Import Library</span></span>           | <span data-ttu-id="c9832-124">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="c9832-124">d3dx9.lib</span></span>  |
| <span data-ttu-id="c9832-125">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="c9832-125">Minimum Operating System</span></span> | <span data-ttu-id="c9832-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c9832-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c9832-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9832-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9832-128">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="c9832-128">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="c9832-129">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="c9832-129">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
