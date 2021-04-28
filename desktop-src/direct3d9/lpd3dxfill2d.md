---
description: 'LPD3DXFILL2D: tipo de función que usan las funciones de relleno de textura.'
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046c324511f2b308243d62fec1b6508a1d483ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087973"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="e7a47-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="e7a47-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="e7a47-104">Tipo de función utilizado por las funciones de relleno de textura.</span><span class="sxs-lookup"><span data-stu-id="e7a47-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7a47-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="e7a47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">Parameters</span></span>

<span data-ttu-id="e7a47-107">pOut: puntero a un vector, que la función usa para devolver su resultado.</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="e7a47-108">X, Y, Z y W se asignarán a R, G, B y A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="e7a47-109">pTexCoord: puntero a un vector que contiene las coordenadas del texel que se está evaluando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="e7a47-110">Los componentes de coordenadas de textura para texturas y texturas de volumen oscilan entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="e7a47-111">Los componentes de coordenadas de textura para texturas de cubo oscilan entre -1 y 1.</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="e7a47-112">pTexelSize: puntero a un vector que contiene las dimensiones del texel actual.</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="e7a47-113">pData: puntero a los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7a47-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">Return Value</span></span>

<span data-ttu-id="e7a47-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7a47-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">Remarks</span></span>

<span data-ttu-id="e7a47-117">Asegúrese de especificar la convención de llamada tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="e7a47-118">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e7a47-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7a47-119">Header</span></span>                   | <span data-ttu-id="e7a47-120">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="e7a47-121">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">Import Library</span></span>           | <span data-ttu-id="e7a47-122">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="e7a47-123">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">Minimum Operating System</span></span> | <span data-ttu-id="e7a47-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e7a47-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7a47-126">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="e7a47-127">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="e7a47-127">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
