---
description: El gráfico de filtro se está cerrando antes de ser destruido.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653555"
---
# <a name="ec_shutting_down"></a><span data-ttu-id="d30f7-103">\_cierre de EC \_</span><span class="sxs-lookup"><span data-stu-id="d30f7-103">EC\_SHUTTING\_DOWN</span></span>

<span data-ttu-id="d30f7-104">El gráfico de filtro se está cerrando antes de ser destruido.</span><span class="sxs-lookup"><span data-stu-id="d30f7-104">The filter graph is shutting down, prior to being destroyed.</span></span>

## <a name="parameters"></a><span data-ttu-id="d30f7-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d30f7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d30f7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d30f7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d30f7-107">Cero.</span><span class="sxs-lookup"><span data-stu-id="d30f7-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="d30f7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d30f7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d30f7-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="d30f7-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d30f7-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="d30f7-110">Default Action</span></span>

<span data-ttu-id="d30f7-111">Este evento no se envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d30f7-111">This event is not sent to the application.</span></span> <span data-ttu-id="d30f7-112">El administrador de gráficos de filtros lo envía a los distribuidores de complementos para notificarles que el gráfico se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="d30f7-112">The filter graph manager sends it to plug-in distributors, to notify them that the graph is shutting down.</span></span> <span data-ttu-id="d30f7-113">Las aplicaciones no pueden reemplazar la acción predeterminada de este evento.</span><span class="sxs-lookup"><span data-stu-id="d30f7-113">Applications cannot override the default action of this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d30f7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d30f7-114">Requirements</span></span>



| <span data-ttu-id="d30f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d30f7-115">Requirement</span></span> | <span data-ttu-id="d30f7-116">Value</span><span class="sxs-lookup"><span data-stu-id="d30f7-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d30f7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d30f7-117">Header</span></span><br/> | <dl> <span data-ttu-id="d30f7-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d30f7-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d30f7-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d30f7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30f7-120">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="d30f7-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d30f7-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d30f7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




