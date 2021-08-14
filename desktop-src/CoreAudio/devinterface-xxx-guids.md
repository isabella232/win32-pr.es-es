---
description: Los GUID XXX de DEVINTERFACE \_ se usan para representar los GUID de las interfaces de dispositivo.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: DEVINTERFACE_XXX GUID (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cef6a105ed8e34519a2ca0a06d9d4f43a7aa91495fae9f54eedfa44d79b043c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406798"
---
# <a name="devinterface_xxx-guids"></a>GUID XXX de DEVINTERFACE \_

Los GUID XXX de DEVINTERFACE \_ se usan para representar los GUID de las interfaces de dispositivo.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**CAPTURA DE AUDIO DEVINTERFACE \_ \_**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los dispositivos de captura de audio en el sistema. [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)devuelve este valor.

Al pasar este valor a [**ActivateAudioInterfaceAsync,**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) se activa la interfaz solicitada en el dispositivo de captura de audio predeterminado.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**REPRESENTACIÓN DE AUDIO DEVINTERFACE \_ \_**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los dispositivos de representación de audio en el sistema. [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)devuelve este valor.

Al pasar este valor a [**ActivateAudioInterfaceAsync,**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) se activa la interfaz solicitada en el dispositivo de representación de audio predeterminado.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**ENTRADA DE DEVINTERFACE \_ MIDI \_**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los [**objetos MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) del sistema. Este valor lo devuelve [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**SALIDA DE DEVINTERFACE \_ MIDI \_**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los objetos [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) del sistema. Este valor lo devuelve [**MidiOutPort::GetDeviceSelector.**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



 

