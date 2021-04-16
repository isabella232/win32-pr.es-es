---
description: Los \_ GUID de DEVINTERFACE xxx se usan para representar los GUID de las interfaces de dispositivo.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: GUID de DEVINTERFACE_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649950"
---
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="d0134-103">GUID de DEVINTERFACE \_ XXX</span><span class="sxs-lookup"><span data-stu-id="d0134-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="d0134-104">Los \_ GUID de DEVINTERFACE xxx se usan para representar los GUID de las interfaces de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0134-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="d0134-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_captura de audio DEVINTERFACE \_**</span><span class="sxs-lookup"><span data-stu-id="d0134-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d0134-106">Especifica la cadena de consulta utilizada para enumerar todos los dispositivos de captura de audio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d0134-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="d0134-107">[**MediaDevice:: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="d0134-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="d0134-108">Al pasar este valor a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) se activa la interfaz solicitada en el dispositivo de captura de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d0134-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0134-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_representación de audio DEVINTERFACE \_**</span><span class="sxs-lookup"><span data-stu-id="d0134-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d0134-110">Especifica la cadena de consulta utilizada para enumerar todos los dispositivos de representación de audio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d0134-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="d0134-111">[**MediaDevice:: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="d0134-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="d0134-112">Al pasar este valor a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) se activa la interfaz solicitada en el dispositivo de representación de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d0134-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0134-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_entrada MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="d0134-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d0134-114">Especifica la cadena de consulta utilizada para enumerar todos los objetos [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0134-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="d0134-115">[**MidiInPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="d0134-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0134-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_salida MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="d0134-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d0134-117">Especifica la cadena de consulta utilizada para enumerar todos los objetos [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0134-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="d0134-118">[**MidiOutPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="d0134-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0134-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0134-119">Requirements</span></span>



| <span data-ttu-id="d0134-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0134-120">Requirement</span></span> | <span data-ttu-id="d0134-121">Value</span><span class="sxs-lookup"><span data-stu-id="d0134-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0134-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0134-122">Header</span></span><br/> | <dl> <span data-ttu-id="d0134-123"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0134-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 

