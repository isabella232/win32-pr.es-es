---
description: Una ventana de vídeo se está activando o desactivando.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680266"
---
# <a name="ec_activate"></a><span data-ttu-id="d2642-103">activación de EC \_</span><span class="sxs-lookup"><span data-stu-id="d2642-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="d2642-104">Una ventana de vídeo se está activando o desactivando.</span><span class="sxs-lookup"><span data-stu-id="d2642-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2642-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2642-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2642-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d2642-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d2642-107">(**Bool**) **True** si la ventana está activada o **false** si la ventana está desactivada.</span><span class="sxs-lookup"><span data-stu-id="d2642-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="d2642-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d2642-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d2642-109">(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador.</span><span class="sxs-lookup"><span data-stu-id="d2642-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d2642-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="d2642-110">Default Action</span></span>

<span data-ttu-id="d2642-111">El administrador de gráficos de filtro establece el foco a través de la interfaz [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="d2642-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="d2642-112">No envía la notificación de eventos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2642-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2642-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2642-113">Remarks</span></span>

<span data-ttu-id="d2642-114">Un representador de vídeo envía este evento cada vez que su ventana está activada o desactivada (es decir, cuando recibe un mensaje de ACTIVATEAPP de WM \_ ).</span><span class="sxs-lookup"><span data-stu-id="d2642-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="d2642-115">La activación o desactivación de ventanas puede producirse porque la ventana ha ganado o perdido el foco, o porque el representador ha cambiado entre el modo de pantalla completa y el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="d2642-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="d2642-116">Este evento permite al administrador de gráficos de filtro asignar recursos que dependen del foco de la ventana, como dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="d2642-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2642-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2642-117">Requirements</span></span>



| <span data-ttu-id="d2642-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2642-118">Requirement</span></span> | <span data-ttu-id="d2642-119">Value</span><span class="sxs-lookup"><span data-stu-id="d2642-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2642-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2642-120">Header</span></span><br/> | <dl> <span data-ttu-id="d2642-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2642-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2642-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2642-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2642-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="d2642-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d2642-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d2642-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




