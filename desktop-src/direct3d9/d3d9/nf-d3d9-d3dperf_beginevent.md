---
title: D3DPERF_BeginEvent función)
description: Marca el principio de un evento definido por el usuario. PIX puede utilizar este evento para desencadenar una acción.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104420397"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="6c1ab-104">D3DPERF_BeginEvent función)</span><span class="sxs-lookup"><span data-stu-id="6c1ab-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="6c1ab-105">Marca el principio de un evento definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="6c1ab-106">PIX puede utilizar este evento para desencadenar una acción.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c1ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c1ab-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="6c1ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c1ab-108">Parameters</span></span>

`col`

<span data-ttu-id="6c1ab-109">Color del evento.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-109">Event color.</span></span> <span data-ttu-id="6c1ab-110">Este es el color para mostrar el evento en la vista de eventos.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="6c1ab-111">Nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c1ab-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c1ab-112">Return value</span></span>

<span data-ttu-id="6c1ab-113">Nivel de base cero de la jerarquía en la que se inicia este evento.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="6c1ab-114">Si se produce un error, el valor devuelto será negativo.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1ab-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c1ab-115">Remarks</span></span>

<span data-ttu-id="6c1ab-116">Los eventos definidos por el usuario agrupan otros eventos de una manera significativa para el programa de destino, de modo que puedan representarse mejor en las herramientas de generación de perfiles de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="6c1ab-117">Por ejemplo, un evento de *espacio de dibujo* podría corchete varias llamadas de Direct3D que controlan el espacio de un juego.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="6c1ab-118">Los eventos se pueden anidar.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-118">Events can be nested.</span></span>

<span data-ttu-id="6c1ab-119">Cada llamada **D3DPERF_BeginEvent** debe tener una llamada **D3DPERF_EndEvent** coincidente.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="6c1ab-120">Los eventos instantáneos (que no corcheten otros eventos) deben etiquetarse mediante **D3DPERF_SetMarker** en lugar de **D3DPERF_BeginEvent** y **D3DPERF_EndEvent**.</span><span class="sxs-lookup"><span data-stu-id="6c1ab-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1ab-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c1ab-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6c1ab-122">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="6c1ab-122">**Target Platform**</span></span> | <span data-ttu-id="6c1ab-123">Windows</span><span class="sxs-lookup"><span data-stu-id="6c1ab-123">Windows</span></span> |
| <span data-ttu-id="6c1ab-124">**Header**</span><span class="sxs-lookup"><span data-stu-id="6c1ab-124">**Header**</span></span> | <span data-ttu-id="6c1ab-125">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="6c1ab-125">d3d9.h</span></span> |
| <span data-ttu-id="6c1ab-126">**Library**</span><span class="sxs-lookup"><span data-stu-id="6c1ab-126">**Library**</span></span> | <span data-ttu-id="6c1ab-127">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="6c1ab-127">d3d9.lib</span></span> |
| <span data-ttu-id="6c1ab-128">**DLL**</span><span class="sxs-lookup"><span data-stu-id="6c1ab-128">**DLL**</span></span> | <span data-ttu-id="6c1ab-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="6c1ab-129">d3d9.dll</span></span> |