---
description: Control de las notificaciones de eventos de DVD
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: Control de las notificaciones de eventos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997991"
---
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="52f54-103">Control de las notificaciones de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="52f54-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="52f54-104">El navegador de DVD envía notificaciones a una ventana especificada por la aplicación cuando se producen determinados eventos, como cuando cambia el dominio del DVD, cuando se encuentra un nuevo nivel de administración parental y cuando el navegador de DVD está a punto de especificar un bloque de ángulo.</span><span class="sxs-lookup"><span data-stu-id="52f54-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="52f54-105">Los parámetros de evento pueden contener información adicional relacionada con el evento.</span><span class="sxs-lookup"><span data-stu-id="52f54-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="52f54-106">Los mensajes de error y las advertencias también se envían de esta manera.</span><span class="sxs-lookup"><span data-stu-id="52f54-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="52f54-107">La aplicación especifica la ventana que controlará las notificaciones de eventos mediante el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para llamar a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="52f54-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="52f54-108">En el ejemplo anterior, m \_ hWnd es el HWND de la ventana para recibir los mensajes y el \_ evento de DVD de WM \_ es el mensaje definido por la aplicación (mayor que \_ el usuario de WM) que indica que se ha producido un evento de DVD.</span><span class="sxs-lookup"><span data-stu-id="52f54-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="52f54-109">La aplicación recupera el propio evento a través de una llamada a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="52f54-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="52f54-110">Dado que puede haber más de un evento en la cola de eventos en un momento dado, la aplicación debe llamar a **GetEvent** dentro de un bucle que se repite hasta que se hayan recuperado todos los eventos en cola, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="52f54-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



<span data-ttu-id="52f54-111">Los eventos de DVD pueden contener información adicional en los parámetros *lParam1* o *lParam2* , como se muestra arriba, donde la hora actual está incluida en *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="52f54-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="52f54-112">El ejemplo de código anterior es de la aplicación de ejemplo de DVD en Dvdcore. cpp.</span><span class="sxs-lookup"><span data-stu-id="52f54-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="52f54-113">Para obtener una lista completa de todos los eventos de DVD y sus parámetros, consulte [códigos de notificación de eventos de DVD](dvd-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="52f54-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52f54-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52f54-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f54-115">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="52f54-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



