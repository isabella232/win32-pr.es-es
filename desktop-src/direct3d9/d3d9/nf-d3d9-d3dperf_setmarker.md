---
title: D3DPERF_SetMarker función)
description: Marque un evento instantáneo. PIX puede utilizar este evento para desencadenar una acción.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104420398"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="33fe9-104">D3DPERF_SetMarker función)</span><span class="sxs-lookup"><span data-stu-id="33fe9-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="33fe9-105">Marque un evento instantáneo.</span><span class="sxs-lookup"><span data-stu-id="33fe9-105">Mark an instantaneous event.</span></span> <span data-ttu-id="33fe9-106">PIX puede utilizar este evento para desencadenar una acción.</span><span class="sxs-lookup"><span data-stu-id="33fe9-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="33fe9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33fe9-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="33fe9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33fe9-108">Parameters</span></span>

`col`

<span data-ttu-id="33fe9-109">Color del evento.</span><span class="sxs-lookup"><span data-stu-id="33fe9-109">Event color.</span></span> <span data-ttu-id="33fe9-110">Este es el color para mostrar el evento en la vista de eventos.</span><span class="sxs-lookup"><span data-stu-id="33fe9-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="33fe9-111">Nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="33fe9-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="33fe9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33fe9-112">Return value</span></span>

<span data-ttu-id="33fe9-113">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="33fe9-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33fe9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33fe9-114">Remarks</span></span>

<span data-ttu-id="33fe9-115">Los eventos de usuario instantáneos no se corcheten ni agrupan otros eventos.</span><span class="sxs-lookup"><span data-stu-id="33fe9-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="33fe9-116">Por ejemplo, cuando el usuario activa un arma en un juego, una llamada **D3DPERF_SetMarker** podría crear un evento *Shot desencadenado* .</span><span class="sxs-lookup"><span data-stu-id="33fe9-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="33fe9-117">Para agrupar varios eventos con un único nombre definido por el usuario, use **D3DPERF_BeginEvent** y **D3DPERF_EndEvent** en lugar de **D3DPERF_SetMarker**.</span><span class="sxs-lookup"><span data-stu-id="33fe9-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33fe9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33fe9-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="33fe9-119">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="33fe9-119">**Target Platform**</span></span> | <span data-ttu-id="33fe9-120">Windows</span><span class="sxs-lookup"><span data-stu-id="33fe9-120">Windows</span></span> |
| <span data-ttu-id="33fe9-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="33fe9-121">**Header**</span></span> | <span data-ttu-id="33fe9-122">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="33fe9-122">d3d9.h</span></span> |
| <span data-ttu-id="33fe9-123">**Library**</span><span class="sxs-lookup"><span data-stu-id="33fe9-123">**Library**</span></span> | <span data-ttu-id="33fe9-124">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="33fe9-124">d3d9.lib</span></span> |
| <span data-ttu-id="33fe9-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="33fe9-125">**DLL**</span></span> | <span data-ttu-id="33fe9-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="33fe9-126">d3d9.dll</span></span> |