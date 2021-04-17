---
description: Función de devolución de llamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714731"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="3d305-103">LPD3DXUVATLASCB</span><span class="sxs-lookup"><span data-stu-id="3d305-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="3d305-104">Función de devolución de llamada para UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="3d305-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d305-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d305-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="3d305-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d305-106">Parameters</span></span>

<span data-ttu-id="3d305-107">\[out \] fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre 0 y 100 por ciento).</span><span class="sxs-lookup"><span data-stu-id="3d305-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="3d305-108">\[en \] lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente se usa en una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3d305-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d305-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d305-109">Return Value</span></span>

<span data-ttu-id="3d305-110">Esta función se debe implementar para que se devuelvan \_ los elementos correctos para seguir ejecutando el simulador.</span><span class="sxs-lookup"><span data-stu-id="3d305-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="3d305-111">Cualquier otro valor detendrá el simulador.</span><span class="sxs-lookup"><span data-stu-id="3d305-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d305-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d305-112">Remarks</span></span>

<span data-ttu-id="3d305-113">Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3d305-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="3d305-114">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="3d305-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="3d305-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d305-115">Header</span></span>                   | <span data-ttu-id="3d305-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="3d305-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="3d305-117">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="3d305-117">Import Library</span></span>           | <span data-ttu-id="3d305-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="3d305-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="3d305-119">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="3d305-119">Minimum Operating System</span></span> | <span data-ttu-id="3d305-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3d305-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3d305-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d305-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d305-122">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="3d305-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
