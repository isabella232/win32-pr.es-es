---
description: Se quitó un dispositivo Plug and Play o estaba disponible de nuevo.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680811"
---
# <a name="ec_device_lost"></a><span data-ttu-id="acd01-103">\_dispositivo EC \_ perdido</span><span class="sxs-lookup"><span data-stu-id="acd01-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="acd01-104">Se quitó un dispositivo Plug and Play o estaba disponible de nuevo.</span><span class="sxs-lookup"><span data-stu-id="acd01-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="acd01-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acd01-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd01-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="acd01-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="acd01-107">(**IUnknown** \* ) Puntero a la interfaz **IUnknown** del filtro que representa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="acd01-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="acd01-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="acd01-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="acd01-109">Cero si se quitó el dispositivo o 1 si el dispositivo vuelve a estar disponible.</span><span class="sxs-lookup"><span data-stu-id="acd01-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="acd01-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="acd01-110">Default Action</span></span>

<span data-ttu-id="acd01-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="acd01-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="acd01-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acd01-112">Remarks</span></span>

<span data-ttu-id="acd01-113">Cuando el dispositivo vuelve a estar disponible, el estado anterior del filtro del dispositivo ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="acd01-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="acd01-114">La aplicación debe volver a generar el gráfico para poder usar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="acd01-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd01-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acd01-115">Requirements</span></span>



| <span data-ttu-id="acd01-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="acd01-116">Requirement</span></span> | <span data-ttu-id="acd01-117">Value</span><span class="sxs-lookup"><span data-stu-id="acd01-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="acd01-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acd01-118">Header</span></span><br/> | <dl> <span data-ttu-id="acd01-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="acd01-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acd01-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="acd01-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd01-121">Notificación de eliminación de dispositivo</span><span class="sxs-lookup"><span data-stu-id="acd01-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="acd01-122">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="acd01-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="acd01-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="acd01-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




