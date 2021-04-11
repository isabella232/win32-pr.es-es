---
title: WMT_STATUS la notificación de eventos en DirectShow
description: '\_Notificación de eventos de estado de WMT en DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Media Format SDK, WMT_STATUS notificaciones de eventos en DirectShow
- SDK de Windows Media Format, notificaciones de eventos
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), WMT_STATUS notificaciones de eventos en DirectShow
- ASF (formato de sistemas avanzados), WMT_STATUS notificaciones de eventos en DirectShow
- Advanced Systems Format (ASF), notificaciones de eventos
- ASF (formato de sistemas avanzados), notificaciones de eventos
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, notificaciones de eventos
- DirectShow, WMT_STATUS notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271286"
---
# <a name="wmt_status-event-notification-in-directshow"></a><span data-ttu-id="afb08-114">\_Notificación de eventos de estado de WMT en DirectShow</span><span class="sxs-lookup"><span data-stu-id="afb08-114">WMT\_STATUS Event Notification in DirectShow</span></span>

<span data-ttu-id="afb08-115">Tanto el lector ASF como el escritor ASF reenvían eventos de [**\_ Estado WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="afb08-115">Both the ASF Reader and the ASF Writer forward [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) events to applications.</span></span> <span data-ttu-id="afb08-116">El escritor reenvía todos estos eventos y el lector reenvía solo los que pertenecen a la adquisición de licencias de DRM.</span><span class="sxs-lookup"><span data-stu-id="afb08-116">The writer forwards all such events, and the reader forwards only those that pertain to DRM license acquisition.</span></span> <span data-ttu-id="afb08-117">Para recibir estas notificaciones de eventos en la aplicación, agregue un caso para **el \_ \_ evento WMT de EC** en la función de control de eventos.</span><span class="sxs-lookup"><span data-stu-id="afb08-117">To receive these event notifications in your application, add a case for the **EC\_WMT\_EVENT** in your event-handling function.</span></span> <span data-ttu-id="afb08-118">El parámetro *lParam1* asociado al evento contiene el código **de \_ Estado WMT** (que puede ser **\_ error de WMT**) y lParam2 contiene [**\_ \_ \_ datos de evento WMT AM**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que incluye el **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="afb08-118">The *lParam1* parameter associated with the event contains the **WMT\_STATUS** code (which can be **WMT\_ERROR**) and lParam2 contains an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) that includes the **HRESULT**.</span></span>

 

 