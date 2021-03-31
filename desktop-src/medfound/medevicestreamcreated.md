---
description: MEDeviceStreamCreated es un tipo de evento multimedia extendido generado con un evento multimedia MEUnknown por el MFT del dispositivo.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Evento MEDeviceStreamCreated (mftransform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275694"
---
# <a name="medevicestreamcreated-event"></a>Evento MEDeviceStreamCreated

MEDeviceStreamCreated es un tipo de evento multimedia extendido generado con un evento multimedia MEUnknown por el MFT del dispositivo.

Este tipo de evento multimedia extendido no tiene ninguna carga.  El valor HRESULT adecuado se debe proporcionar a través del método [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .




## <a name="remarks"></a>Observaciones

El MFT del dispositivo debe enviar este evento de medios extendidos como parte de la selección del tipo de medio en el flujo de salida de DMFT.  Cuando se invoca SetOutputStreamState en la interfaz IMFDeviceTransform, el DMFT es responsable de señalar el cambio en los Estados de flujo de entrada necesarios con el evento de medios [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) . Cuando la canalización ha confirmado el cambio de estado del flujo de entrada con la llamada a SetInputStreamState de DMFT, el DMFT es responsable de completar la configuración de estado interna y de generar el tipo de evento de medio extendido **MEDeviceStreamCreated** .

Si no se genera este tipo de evento de medios extendidos, el administrador de transformaciones de dispositivos no entregará ningún fotograma de entrada a DMFT.
El tipo de evento multimedia extendido también debe establecerse como un atributo de IMFMediaEvent, el identificador del flujo de salida mediante el atributo **MF_EVENT_MFT_INPUT_STREAM_ID** .

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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
