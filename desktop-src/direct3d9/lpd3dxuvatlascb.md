---
description: Función de devolución de llamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3D LPVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342800"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="8911d-103">LPD3D LPVATLASCB</span><span class="sxs-lookup"><span data-stu-id="8911d-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="8911d-104">Función de devolución de llamada para UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="8911d-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="8911d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8911d-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="8911d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8911d-106">Parameters</span></span>

<span data-ttu-id="8911d-107">\[out fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de \] cálculos completados (entre 0 y 100 por ciento).</span><span class="sxs-lookup"><span data-stu-id="8911d-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="8911d-108">\[en lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de \] llamada.</span><span class="sxs-lookup"><span data-stu-id="8911d-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="8911d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8911d-109">Return Value</span></span>

<span data-ttu-id="8911d-110">Esta función debe implementarse para devolver S \_ OK para seguir ejecutando el simulador.</span><span class="sxs-lookup"><span data-stu-id="8911d-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="8911d-111">Cualquier otro valor detendrá el simulador.</span><span class="sxs-lookup"><span data-stu-id="8911d-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="8911d-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8911d-112">Remarks</span></span>

<span data-ttu-id="8911d-113">Asegúrese de especificar la convención de llamada tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8911d-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="8911d-114">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="8911d-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="8911d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8911d-115">Requirement</span></span>                         | <span data-ttu-id="8911d-116">Value</span><span class="sxs-lookup"><span data-stu-id="8911d-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="8911d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8911d-117">Header</span></span>                   | <span data-ttu-id="8911d-118">d3dx9mesh.h</span><span class="sxs-lookup"><span data-stu-id="8911d-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="8911d-119">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="8911d-119">Import Library</span></span>           | <span data-ttu-id="8911d-120">d3dx9.lib</span><span class="sxs-lookup"><span data-stu-id="8911d-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="8911d-121">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="8911d-121">Minimum Operating System</span></span> | <span data-ttu-id="8911d-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8911d-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="8911d-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8911d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8911d-124">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="8911d-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
