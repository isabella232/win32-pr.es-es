---
description: Tipo de función que usan las funciones de relleno de textura.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274664"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="f4075-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="f4075-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="f4075-104">Tipo de función que usan las funciones de relleno de textura.</span><span class="sxs-lookup"><span data-stu-id="f4075-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4075-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4075-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="f4075-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4075-106">Parameters</span></span>

<span data-ttu-id="f4075-107">pOut: puntero a un vector, que la función utiliza para devolver el resultado.</span><span class="sxs-lookup"><span data-stu-id="f4075-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="f4075-108">X, Y, Z y W se asignarán a R, G, B y A, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f4075-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="f4075-109">pTexCoord: puntero a un vector que contiene las coordenadas de la textura que se está evaluando actualmente.</span><span class="sxs-lookup"><span data-stu-id="f4075-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="f4075-110">Los componentes de coordenada de textura para texturas y texturas de volumen van de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="f4075-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="f4075-111">Los componentes de coordenadas de textura para las texturas del cubo van de-1 a 1.</span><span class="sxs-lookup"><span data-stu-id="f4075-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="f4075-112">pTexelSize: puntero a un vector que contiene las dimensiones de la textura actual.</span><span class="sxs-lookup"><span data-stu-id="f4075-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="f4075-113">pData: puntero a los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="f4075-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4075-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4075-114">Return Value</span></span>

<span data-ttu-id="f4075-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f4075-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4075-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4075-116">Remarks</span></span>

<span data-ttu-id="f4075-117">Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f4075-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="f4075-118">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="f4075-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f4075-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4075-119">Header</span></span>                   | <span data-ttu-id="f4075-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="f4075-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="f4075-121">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="f4075-121">Import Library</span></span>           | <span data-ttu-id="f4075-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="f4075-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="f4075-123">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="f4075-123">Minimum Operating System</span></span> | <span data-ttu-id="f4075-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f4075-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f4075-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4075-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4075-126">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="f4075-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="f4075-127">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="f4075-127">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
