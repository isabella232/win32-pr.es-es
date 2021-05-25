---
description: Función de devolución de llamada para la simulación y compresión de transferencia de radiancia precalutadas (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342810"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="456c2-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="456c2-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="456c2-104">Función de devolución de llamada para la simulación y compresión de transferencia de radiancia precalutadas (PRT).</span><span class="sxs-lookup"><span data-stu-id="456c2-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="456c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="456c2-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="456c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="456c2-106">Parameters</span></span>

<span data-ttu-id="456c2-107">fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre el 0 y el 100 %).</span><span class="sxs-lookup"><span data-stu-id="456c2-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="456c2-108">lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="456c2-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="456c2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="456c2-109">Return Value</span></span>

<span data-ttu-id="456c2-110">Esta función debe implementarse para devolver S \_ OK para seguir ejecutando el simulador.</span><span class="sxs-lookup"><span data-stu-id="456c2-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="456c2-111">Cualquier otro valor detendrá el simulador.</span><span class="sxs-lookup"><span data-stu-id="456c2-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="456c2-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="456c2-112">Remarks</span></span>

<span data-ttu-id="456c2-113">Asegúrese de especificar la convención de llamada de tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="456c2-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="456c2-114">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="456c2-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="456c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="456c2-115">Requirement</span></span>                         | <span data-ttu-id="456c2-116">Value</span><span class="sxs-lookup"><span data-stu-id="456c2-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="456c2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="456c2-117">Header</span></span>                   | <span data-ttu-id="456c2-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="456c2-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="456c2-119">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="456c2-119">Import Library</span></span>           | <span data-ttu-id="456c2-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="456c2-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="456c2-121">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="456c2-121">Minimum Operating System</span></span> | <span data-ttu-id="456c2-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="456c2-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="456c2-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="456c2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="456c2-124">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="456c2-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
