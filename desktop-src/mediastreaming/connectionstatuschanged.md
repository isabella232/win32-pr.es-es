---
title: Evento ConnectionStatusChanged
description: Se produce cuando cambia el estado de la conexión de red del dispositivo.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- ConnectionStatusChanged Event media streaming API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791223"
---
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="b6716-104">Evento ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="b6716-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="b6716-105">Se produce cuando cambia el estado de la conexión de red del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6716-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6716-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6716-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="b6716-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6716-107">Parameters</span></span>

<span data-ttu-id="b6716-108">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b6716-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6716-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6716-109">Return value</span></span>

<span data-ttu-id="b6716-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b6716-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6716-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6716-111">Remarks</span></span>

<span data-ttu-id="b6716-112">Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) mediante el método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="b6716-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="b6716-113">Para anular el registro del controlador de eventos, use el método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="b6716-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 