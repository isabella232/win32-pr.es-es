---
description: El sistema difunde el \_ evento de dispositivo DBT CONFIGCHANGECANCELED cuando se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Evento DBT_CONFIGCHANGECANCELED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907223"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="256b9-103">\_Evento DBT CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="256b9-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="256b9-104">El sistema difunde el \_ evento de dispositivo DBT CONFIGCHANGECANCELED cuando se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="256b9-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="256b9-105">Para difundir este evento de dispositivo, el sistema usa el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) con *wParam* establecido en DBT \_ CONFIGCHANGECANCELED y *lParam* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="256b9-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="256b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="256b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256b9-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="256b9-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="256b9-108">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="256b9-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="256b9-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="256b9-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="256b9-110">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="256b9-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="256b9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="256b9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="256b9-112">Establézcalo en DBT \_ CONFIGCHANGECANCELED.</span><span class="sxs-lookup"><span data-stu-id="256b9-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="256b9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="256b9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="256b9-114">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="256b9-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256b9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="256b9-115">Return value</span></span>

<span data-ttu-id="256b9-116">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="256b9-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="256b9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="256b9-117">Requirements</span></span>



| <span data-ttu-id="256b9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="256b9-118">Requirement</span></span> | <span data-ttu-id="256b9-119">Value</span><span class="sxs-lookup"><span data-stu-id="256b9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="256b9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="256b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="256b9-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="256b9-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="256b9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="256b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="256b9-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="256b9-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="256b9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="256b9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="256b9-125"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="256b9-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256b9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="256b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256b9-127">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="256b9-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="256b9-128">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="256b9-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="256b9-129">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="256b9-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




