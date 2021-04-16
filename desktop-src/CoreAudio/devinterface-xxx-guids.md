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
# <a name="devinterface_xxx-guids"></a>GUID de DEVINTERFACE \_ XXX

Los \_ GUID de DEVINTERFACE xxx se usan para representar los GUID de las interfaces de dispositivo.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_captura de audio DEVINTERFACE \_**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los dispositivos de captura de audio en el sistema. [**MediaDevice:: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)devuelve este valor.

Al pasar este valor a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) se activa la interfaz solicitada en el dispositivo de captura de audio predeterminado.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_representación de audio DEVINTERFACE \_**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los dispositivos de representación de audio en el sistema. [**MediaDevice:: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)devuelve este valor.

Al pasar este valor a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) se activa la interfaz solicitada en el dispositivo de representación de audio predeterminado.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_entrada MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los objetos [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) del sistema. [**MidiInPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)devuelve este valor.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_salida MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Especifica la cadena de consulta utilizada para enumerar todos los objetos [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) del sistema. [**MidiOutPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)devuelve este valor.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



 

