---
description: Indica que un origen multimedia ha empezado a almacenar en búfer los datos.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Evento MEBufferingStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55a691b723fc2e09487752ee8f5226e32504d60a6d68a4652bbb2b5b3e5aa7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724275"
---
# <a name="mebufferingstarted-event"></a>Evento MEBufferingStarted

Indica que un origen multimedia ha empezado a almacenar en búfer los datos.

Un origen de medios puede enviar este evento si el origen almacena en búfer los datos mientras se ejecuta la sesión multimedia. Cuando la sesión multimedia recibe este evento, pausa el reloj de presentación hasta que el origen multimedia envía el [evento MEBufferingStopped.](mebufferingstopped.md) La sesión multimedia también reenvía el evento MEBufferingStarted a la aplicación.

Las secuencias de bytes que implementan [**la interfaz BYTEByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) también envían este evento.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Si un origen multimedia envía el evento MEBufferingStarted, debe enviar el evento [MEBufferingStopped](mebufferingstopped.md) cuando deje de almacenar en búfer los datos. El origen multimedia debe enviar un evento MEBufferingStopped correspondiente para cada evento MEBufferingStarted. El origen de medios no debe reenviar estos eventos antes de que se llame al método [**ODBCMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) del origen o después de llamar al método [**ODBCMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) del origen.

Si está transmitiendo desde el origen Media Foundation de red, puede obtener el progreso del almacenamiento en búfer consultando la estadística DE ID DE **\_ MFNETSOURCE BUFFERPROGRESS. \_** Para obtener más información, [**vea MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="examples"></a>Ejemplos


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




