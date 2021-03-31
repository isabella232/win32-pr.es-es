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
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="05afe-103">Evento MEDeviceStreamCreated</span><span class="sxs-lookup"><span data-stu-id="05afe-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="05afe-104">MEDeviceStreamCreated es un tipo de evento multimedia extendido generado con un evento multimedia MEUnknown por el MFT del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05afe-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="05afe-105">Este tipo de evento multimedia extendido no tiene ninguna carga.</span><span class="sxs-lookup"><span data-stu-id="05afe-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="05afe-106">El valor HRESULT adecuado se debe proporcionar a través del método [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="05afe-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="05afe-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05afe-107">Remarks</span></span>

<span data-ttu-id="05afe-108">El MFT del dispositivo debe enviar este evento de medios extendidos como parte de la selección del tipo de medio en el flujo de salida de DMFT.</span><span class="sxs-lookup"><span data-stu-id="05afe-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="05afe-109">Cuando se invoca SetOutputStreamState en la interfaz IMFDeviceTransform, el DMFT es responsable de señalar el cambio en los Estados de flujo de entrada necesarios con el evento de medios [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="05afe-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="05afe-110">Cuando la canalización ha confirmado el cambio de estado del flujo de entrada con la llamada a SetInputStreamState de DMFT, el DMFT es responsable de completar la configuración de estado interna y de generar el tipo de evento de medio extendido **MEDeviceStreamCreated** .</span><span class="sxs-lookup"><span data-stu-id="05afe-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="05afe-111">Si no se genera este tipo de evento de medios extendidos, el administrador de transformaciones de dispositivos no entregará ningún fotograma de entrada a DMFT.</span><span class="sxs-lookup"><span data-stu-id="05afe-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="05afe-112">El tipo de evento multimedia extendido también debe establecerse como un atributo de IMFMediaEvent, el identificador del flujo de salida mediante el atributo **MF_EVENT_MFT_INPUT_STREAM_ID** .</span><span class="sxs-lookup"><span data-stu-id="05afe-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="05afe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05afe-113">Requirements</span></span>



| <span data-ttu-id="05afe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="05afe-114">Requirement</span></span> | <span data-ttu-id="05afe-115">Value</span><span class="sxs-lookup"><span data-stu-id="05afe-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05afe-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05afe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="05afe-117">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="05afe-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05afe-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05afe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="05afe-119">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="05afe-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05afe-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05afe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="05afe-121"><dt>mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="05afe-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05afe-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="05afe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05afe-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05afe-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="05afe-124">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="05afe-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
