---
description: Se envía cuando una aplicación usa el filtro de escritor ASF de WM para indizar Windows Media Video archivos.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679537"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="e868c-103">EC_WMT_INDEX_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="e868c-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="e868c-104">Se envía cuando una aplicación usa el filtro de [escritor ASF de WM](wm-asf-writer-filter.md) para indizar Windows Media Video archivos.</span><span class="sxs-lookup"><span data-stu-id="e868c-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="e868c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e868c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e868c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e868c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e868c-107">Puede ser uno de los siguientes mensajes de **\_ Estado de WMT** .</span><span class="sxs-lookup"><span data-stu-id="e868c-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="e868c-108">Value</span><span class="sxs-lookup"><span data-stu-id="e868c-108">Value</span></span>                | <span data-ttu-id="e868c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e868c-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="e868c-110">WMT \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="e868c-110">WMT\_STARTED</span></span>         | <span data-ttu-id="e868c-111">La indización ha comenzado.</span><span class="sxs-lookup"><span data-stu-id="e868c-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="e868c-112">WMT \_ cerrado</span><span class="sxs-lookup"><span data-stu-id="e868c-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="e868c-113">La indización ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e868c-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="e868c-114">\_progreso del índice WMT \_</span><span class="sxs-lookup"><span data-stu-id="e868c-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="e868c-115">La indexación está en curso.</span><span class="sxs-lookup"><span data-stu-id="e868c-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e868c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e868c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e868c-117">Si *lParam1* es WMT \_ Closed o WMT \_ iniciado, entonces *lParam2* es cero.</span><span class="sxs-lookup"><span data-stu-id="e868c-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="e868c-118">Si *lParam1* es \_ \_ el progreso del índice WMT, *lParam2* es un **valor DWORD** que especifica el progreso actual como un porcentaje del tamaño total de la descarga.</span><span class="sxs-lookup"><span data-stu-id="e868c-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e868c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e868c-119">Requirements</span></span>



| <span data-ttu-id="e868c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e868c-120">Requirement</span></span> | <span data-ttu-id="e868c-121">Value</span><span class="sxs-lookup"><span data-stu-id="e868c-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e868c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e868c-122">Header</span></span><br/> | <dl> <span data-ttu-id="e868c-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e868c-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e868c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e868c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e868c-125">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="e868c-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e868c-126">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e868c-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




