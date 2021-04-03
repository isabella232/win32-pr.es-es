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
# <a name="handling-dvd-event-notifications"></a>Control de las notificaciones de eventos de DVD

El navegador de DVD envía notificaciones a una ventana especificada por la aplicación cuando se producen determinados eventos, como cuando cambia el dominio del DVD, cuando se encuentra un nuevo nivel de administración parental y cuando el navegador de DVD está a punto de especificar un bloque de ángulo. Los parámetros de evento pueden contener información adicional relacionada con el evento. Los mensajes de error y las advertencias también se envían de esta manera. La aplicación especifica la ventana que controlará las notificaciones de eventos mediante el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para llamar a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), como se indica a continuación:


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



En el ejemplo anterior, m \_ hWnd es el HWND de la ventana para recibir los mensajes y el \_ evento de DVD de WM \_ es el mensaje definido por la aplicación (mayor que \_ el usuario de WM) que indica que se ha producido un evento de DVD. La aplicación recupera el propio evento a través de una llamada a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Dado que puede haber más de un evento en la cola de eventos en un momento dado, la aplicación debe llamar a **GetEvent** dentro de un bucle que se repite hasta que se hayan recuperado todos los eventos en cola, tal y como se muestra en el ejemplo de código siguiente.


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



Los eventos de DVD pueden contener información adicional en los parámetros *lParam1* o *lParam2* , como se muestra arriba, donde la hora actual está incluida en *lParam1*. El ejemplo de código anterior es de la aplicación de ejemplo de DVD en Dvdcore. cpp. Para obtener una lista completa de todos los eventos de DVD y sus parámetros, consulte [códigos de notificación de eventos de DVD](dvd-notification-codes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



