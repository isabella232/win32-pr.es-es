---
description: Función de devolución de llamada para simulación y compresión precalculadas de Radiance Transfer (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495317"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="e9f2d-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="e9f2d-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="e9f2d-104">Función de devolución de llamada para simulación y compresión precalculadas de Radiance Transfer (PRT).</span><span class="sxs-lookup"><span data-stu-id="e9f2d-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f2d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9f2d-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="e9f2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9f2d-106">Parameters</span></span>

<span data-ttu-id="e9f2d-107">fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre 0 y 100 por ciento).</span><span class="sxs-lookup"><span data-stu-id="e9f2d-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="e9f2d-108">lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada. lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9f2d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9f2d-109">Return Value</span></span>

<span data-ttu-id="e9f2d-110">Esta función se debe implementar para que se devuelvan \_ los elementos correctos para seguir ejecutando el simulador.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="e9f2d-111">Cualquier otro valor detendrá el simulador.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f2d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9f2d-112">Remarks</span></span>

<span data-ttu-id="e9f2d-113">Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="e9f2d-114">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="e9f2d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9f2d-115">Header</span></span>                   | <span data-ttu-id="e9f2d-116">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="e9f2d-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="e9f2d-117">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="e9f2d-117">Import Library</span></span>           | <span data-ttu-id="e9f2d-118">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="e9f2d-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="e9f2d-119">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="e9f2d-119">Minimum Operating System</span></span> | <span data-ttu-id="e9f2d-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e9f2d-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e9f2d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9f2d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9f2d-122">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="e9f2d-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
