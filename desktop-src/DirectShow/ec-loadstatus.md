---
description: Notifica a la aplicación de progreso cuando se abre un archivo de red.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680994"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="afc00-103">LOADSTATUS de EC \_</span><span class="sxs-lookup"><span data-stu-id="afc00-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="afc00-104">Notifica a la aplicación de progreso cuando se abre un archivo de red.</span><span class="sxs-lookup"><span data-stu-id="afc00-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="afc00-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afc00-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="afc00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="afc00-107">Código de estado.</span><span class="sxs-lookup"><span data-stu-id="afc00-107">Status code.</span></span> <span data-ttu-id="afc00-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="afc00-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="afc00-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="afc00-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="afc00-110">Cero.</span><span class="sxs-lookup"><span data-stu-id="afc00-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="afc00-111">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="afc00-111">Default Action</span></span>

<span data-ttu-id="afc00-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afc00-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc00-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afc00-113">Remarks</span></span>

<span data-ttu-id="afc00-114">El filtro de [lector ASF de WM](wm-asf-reader-filter.md) y el filtro de [origen de medios de Windows](windows-media-source-filter.md) heredado envían este evento.</span><span class="sxs-lookup"><span data-stu-id="afc00-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="afc00-115">El primer parámetro de evento tiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="afc00-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="afc00-116">Value</span><span class="sxs-lookup"><span data-stu-id="afc00-116">Value</span></span>                        | <span data-ttu-id="afc00-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="afc00-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="afc00-118">AM \_ LOADSTATUS \_ cerrado</span><span class="sxs-lookup"><span data-stu-id="afc00-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="afc00-119">El filtro de origen ha cerrado el archivo.</span><span class="sxs-lookup"><span data-stu-id="afc00-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="afc00-120">\_conexión LOADSTATUS \_ AM</span><span class="sxs-lookup"><span data-stu-id="afc00-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="afc00-121">El filtro de origen se está conectando al servidor.</span><span class="sxs-lookup"><span data-stu-id="afc00-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="afc00-122">\_LOADINGDESCR LOADSTATUS \_ AM</span><span class="sxs-lookup"><span data-stu-id="afc00-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="afc00-123">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="afc00-123">Not used.</span></span>                                      |
| <span data-ttu-id="afc00-124">\_LOADINGMCAST LOADSTATUS \_ AM</span><span class="sxs-lookup"><span data-stu-id="afc00-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="afc00-125">No se usa</span><span class="sxs-lookup"><span data-stu-id="afc00-125">Not used</span></span>                                       |
| <span data-ttu-id="afc00-126">LOADSTATUS de AM \_ \_</span><span class="sxs-lookup"><span data-stu-id="afc00-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="afc00-127">El filtro de origen está buscando los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="afc00-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="afc00-128">AM \_ LOADSTATUS \_ abierto</span><span class="sxs-lookup"><span data-stu-id="afc00-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="afc00-129">El filtro de origen ha abierto el archivo.</span><span class="sxs-lookup"><span data-stu-id="afc00-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="afc00-130">\_abrir LOADSTATUS \_ AM</span><span class="sxs-lookup"><span data-stu-id="afc00-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="afc00-131">El filtro de origen está abriendo el archivo.</span><span class="sxs-lookup"><span data-stu-id="afc00-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="afc00-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afc00-132">Requirements</span></span>



| <span data-ttu-id="afc00-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc00-133">Requirement</span></span> | <span data-ttu-id="afc00-134">Value</span><span class="sxs-lookup"><span data-stu-id="afc00-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afc00-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afc00-135">Header</span></span><br/> | <dl> <span data-ttu-id="afc00-136"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc00-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc00-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="afc00-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc00-138">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="afc00-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="afc00-139">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="afc00-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




