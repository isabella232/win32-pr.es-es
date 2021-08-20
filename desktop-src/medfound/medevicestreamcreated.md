---
description: MEDeviceStreamCreated es un tipo de evento multimedia extendido generado con un evento multimedia MEUnknown por el MFT del dispositivo.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Evento MEDeviceStreamCreated (mftransform.h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 99e13dae5db9d680909a435d5520f6b07d7d4b6c11782c340b72fcdd0eddc53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878072"
---
# <a name="medevicestreamcreated-event"></a>Evento MEDeviceStreamCreated

MEDeviceStreamCreated es un tipo de evento multimedia extendido generado con un evento multimedia MEUnknown por el MFT del dispositivo.

Este tipo de evento multimedia extendido no tiene ninguna carga.  Se debe proporcionar HRESULT adecuado a través del [**método IMFMediaEvent::GetStatus.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)




## <a name="remarks"></a>Comentarios

El MFT del dispositivo debe enviar este evento multimedia extendido como parte de la selección de tipo de medio en el flujo de salida de DMFT.  Cuando se invoca SetOutputStreamState en la interfaz IMFDeviceTransform, DMFT es responsable de señalar el cambio en los estados de flujo de entrada necesarios con el evento multimedia [METransformInputStreamStateChanged.](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) Cuando la canalización ha reconocido el cambio de estado del flujo de entrada con la llamada a SetInputStreamState de la DMFT, dmft es responsable de completar su configuración de estado interno y generar el tipo de evento multimedia **extendido MEDeviceStreamCreated.**

Si no se genera este tipo de evento multimedia extendido, Device Transform Manager no entregará ningún fotograma de entrada a DMFT.
El tipo de evento multimedia extendido también debe establecerse como un atributo de LANMEDIAEVENT, el identificador del flujo de salida mediante **el MF_EVENT_MFT_INPUT_STREAM_ID** atributo.

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
