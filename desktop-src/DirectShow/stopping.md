---
description: Deteniéndose
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: Deteniéndose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912117"
---
# <a name="stopping"></a>Deteniéndose

El método **Stop** debe desbloquear el método **Receive** y anular la confirmación de los asignadores del filtro. La desconfirmación de un asignador obliga a que se devuelvan las llamadas de **getBuffer** pendientes, lo que desbloquea los filtros ascendentes que están esperando ejemplos. El método **Stop** contiene el bloqueo de filtro y, a continuación, llama al método [**CBaseFilter:: Stop**](cbasefilter-stop.md) , que llama a [**CBasePin:: Inactive**](cbasepin-inactive.md) en todos los PIN del filtro:


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



Invalide el método **inactivo** del PIN de entrada como se indica a continuación:


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



