---
description: Se genera después de que el método IMFMediaSession::SetTopology se complete de forma asincrónica. La sesión multimedia genera este evento después de resolver la topología en una topología completa y poner en cola la topología para su reproducción.
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2b5454309855ff472c633388cddabe0c12fab09e2ae462aacd2de49c3c9bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957405"
---
# <a name="mesessiontopologyset-event"></a>Evento MESessionTopologySet

Se genera después de que [**el método IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se complete de forma asincrónica. La sesión multimedia genera este evento después de resolver la topología en una topología completa y poner en cola la topología para su reproducción.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Sin datos del evento.<br/> <br/>                                                                    |
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz DETOPOLOGY**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología completa.<br/> <br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se recupera el puntero [**DETOPOLOGY**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de un evento MESessionTopologySet.


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




