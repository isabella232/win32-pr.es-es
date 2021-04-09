---
description: El \_ evento DBT USERDEFINED Device identifica un evento definido por el usuario.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Evento DBT_USERDEFINED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080195"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="e8e0d-103">\_Evento USERDEFINED DBT</span><span class="sxs-lookup"><span data-stu-id="e8e0d-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="e8e0d-104">El \_ evento DBT USERDEFINED Device identifica un evento definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="e8e0d-105">Para difundir este evento de dispositivo, llame a la función [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) con el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e0d-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="e8e0d-106">Establezca *wParam* en DBT \_ USERDEFINED y establezca *lParam* como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="e8e0d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8e0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e0d-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="e8e0d-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e0d-109">Identificador a una ventana.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="e8e0d-110">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="e8e0d-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e0d-111">Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e0d-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8e0d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8e0d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e0d-113">Establezca en DBT \_ USERDEFINED.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="e8e0d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8e0d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e0d-115">Un puntero a una estructura [**\_ \_ \_ USERDEFINED de difusión de desarrollo**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) que describe la difusión definida por el usuario en curso.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="e8e0d-116">El miembro **dbud \_ szName** contiene el nombre del mensaje definido por el usuario, seguido de los datos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e0d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8e0d-117">Return value</span></span>

<span data-ttu-id="e8e0d-118">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="e8e0d-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e0d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8e0d-119">Requirements</span></span>



| <span data-ttu-id="e8e0d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e0d-120">Requirement</span></span> | <span data-ttu-id="e8e0d-121">Value</span><span class="sxs-lookup"><span data-stu-id="e8e0d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e8e0d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e0d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e0d-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8e0d-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="e8e0d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e0d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e0d-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8e0d-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="e8e0d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8e0d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e0d-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e0d-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e0d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e0d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e0d-129">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e8e0d-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="e8e0d-130">Eventos de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="e8e0d-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="e8e0d-131">**\_DESARROLLO de \_ difusión \_ USERDEFINED**</span><span class="sxs-lookup"><span data-stu-id="e8e0d-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="e8e0d-132">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e8e0d-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="e8e0d-133">**BroadcastSystemMessage**</span><span class="sxs-lookup"><span data-stu-id="e8e0d-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

