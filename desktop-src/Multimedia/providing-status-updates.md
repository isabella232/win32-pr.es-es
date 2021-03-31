---
title: Proporcionar actualizaciones de estado
description: Proporcionar actualizaciones de estado
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer (macro)
- MCIWndSetInactiveTimer (macro)
- MCIWndGetActiveTimer (macro)
- MCIWndGetInactiveTimer (macro)
- MCIWndSetTimers (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418623"
---
# <a name="providing-status-updates"></a><span data-ttu-id="2ed8e-108">Proporcionar actualizaciones de estado</span><span class="sxs-lookup"><span data-stu-id="2ed8e-108">Providing Status Updates</span></span>

<span data-ttu-id="2ed8e-109">MCIWnd usa temporizadores para actualizar periódicamente la información en la barra de título y la barra de desplazamiento de la ventana, y para enviar mensajes de notificación a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="2ed8e-110">Un temporizador controla el período de actualización de la ventana de MCIWnd activa y un segundo temporizador controla el período de actualización de las ventanas MCIWnd que están inactivas.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="2ed8e-111">La aplicación puede usar las macros de temporizador de MCIWnd para recuperar la configuración actual del temporizador y ajustar los períodos de actualización.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="2ed8e-112">Puede establecer el período de actualización utilizado por el temporizador de la ventana activa mediante la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="2ed8e-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="2ed8e-113">Esta macro establece el período utilizado por MCIWnd para actualizar el control TrackBar, para actualizar la posición de reproducción notificada en la barra de título de la ventana y para notificar a la ventana primaria que el medio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="2ed8e-114">Puede recuperar el período de actualización actual usado por el temporizador de la ventana activa mediante la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="2ed8e-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="2ed8e-115">El período de actualización predeterminado para el temporizador de la ventana activa es de 500 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="2ed8e-116">Puede establecer el período de actualización utilizado por el temporizador de la ventana inactiva mediante la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="2ed8e-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="2ed8e-117">Esta macro establece el período utilizado por MCIWnd para actualizar la barra de control, para actualizar la posición de reproducción notificada en el título de la ventana y para notificar a la ventana primaria que el medio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="2ed8e-118">Puede recuperar el período de actualización actual usado por el temporizador de la ventana inactiva mediante la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="2ed8e-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="2ed8e-119">El período de actualización predeterminado para el temporizador de la ventana inactiva es de 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="2ed8e-120">La aplicación puede establecer simultáneamente el período de actualización de ambos temporizadores mediante la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="2ed8e-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="2ed8e-121">El almacenamiento para el valor del período de actualización está limitado a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="2ed8e-122">Si se necesita una cantidad mayor para cada período de actualización, establezca los temporizadores individualmente.</span><span class="sxs-lookup"><span data-stu-id="2ed8e-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




