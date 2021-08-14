---
description: Especifica las características que un cliente puede asignar a una secuencia de audio durante la inicialización de la secuencia.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: AUDCLNT_STREAMFLAGS_XXX constantes (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84817607092c179286f47eb35ef51f5e0f82d44211bcd2345ca3d27ee06b0e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407368"
---
# <a name="audclnt_streamflags_xxx-constants"></a>Constantes XXX \_ de STREAMFLAGS de AUDCLNT \_

Especifica las características que un cliente puede asignar a una secuencia de audio durante la inicialización de la secuencia.



| Constante o valor                                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ StreamFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | La secuencia de audio será miembro de una sesión de audio entre procesos. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ StreamFLAGS \_ LOOPBACK**</dt> <dt>0x00020000</dt> </dl>                                                   | La secuencia de audio funcionará en modo de bucle recuperación. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ StreamFLAGS \_ EVENTCALLBACK**</dt> <dt>0x00040000</dt> </dl>                                    | El procesamiento del búfer de audio por parte del cliente estará controlado por eventos. Para obtener más información, vea la sección Comentarios. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ StreamFLAGS \_ NOPERSIST**</dt> <dt>0x00080000</dt> </dl>                                                | La configuración de volumen y exclusión mutua de una sesión de audio no se conservará entre los reinicios de la aplicación. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Esta constante es nueva en Windows 7. La frecuencia de muestreo de la secuencia se ajusta a la velocidad especificada por una aplicación. Para obtener más información, vea la sección Comentarios. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Se insertan un matrixer de canal y un convertidor de frecuencia de muestreo según sea necesario para convertir entre el formato sin comprimir proporcionado a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) y el formato de combinación del motor de audio.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ SRC \_ DEFAULT QUALITY \_ 0x08000000**</dt> <dt></dt> </dl>                | Cuando se usa con **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM,** se usa un convertidor de frecuencia de muestreo con una mejor calidad que la conversión predeterminada, pero con un costo de rendimiento mayor. Debe usarse si el audio está pensado en última instancia para que lo escuche el ser humano, en lugar de otros escenarios, como el bombeo de silencio o la población de un medidor.<br/> |



## <a name="remarks"></a>Comentarios

El [**método IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) y la estructura [**DIRECTX AUDIO ACTIVATION \_ \_ \_ PARAMS**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) usan las constantes AUDCLNT \_ STREAMFLAGS \_ XXX.

La marca AUDCLNT STREAMFLAGS CROSSPROCESS indica que la sesión de audio de la secuencia \_ es una sesión entre \_ procesos. Una sesión entre procesos puede aceptar secuencias de más de un proceso. Si dos aplicaciones de dos procesos independientes llaman a **IAudioClient::Initialize** con GUID de sesión idénticos y ambas aplicaciones establecen la marca CROSSPROCESS AUDCLNT SHAREMODE, el motor de audio asigna sus secuencias a la misma sesión entre \_ \_ procesos. Esta marca invalida el comportamiento predeterminado, que es asignar la secuencia a una sesión específica del proceso en lugar de a una sesión entre procesos. El bit de marca AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS no es compatible con el modo exclusivo. Para obtener más información sobre las sesiones entre procesos, vea [Sesiones de audio.](audio-sessions.md)

La marca AUDCLNT \_ STREAMFLAGS LOOPBACK habilita \_ la grabación de bucles bucles. En la grabación de bucleback, el motor de audio copia la secuencia de audio que reproduce un dispositivo de punto de conexión de representación en un búfer de punto de conexión de audio para que un cliente [WASAPI](wasapi.md) pueda capturar la secuencia. Si se establece esta marca, el **método IAudioClient::Initialize** intenta abrir un búfer de captura en el dispositivo de representación. Esta marca solo es válida para un dispositivo de representación y solo si la llamada **a Initialize** establece el parámetro *ShareMode* en AUDCLNT \_ SHAREMODE \_ SHARED. De lo **contrario, se** producirá un error en la llamada a Initialize. Si la llamada se realiza correctamente, el cliente puede llamar al método [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obtener una [**interfaz IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) en el dispositivo de representación. Para obtener más información, vea [Loopback Recording](loopback-recording.md).

La marca AUDCLNT \_ STREAMFLAGS EVENTCALLBACK habilita el almacenamiento \_ en búfer controlado por eventos. Si un cliente establece esta marca en la llamada a **IAudioClient::Initialize** que inicializa una secuencia, el cliente debe llamar posteriormente al método [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) para proporcionar un identificador de eventos para la secuencia. Una vez que se inicia la secuencia, el motor de audio señalará al identificador de eventos para notificar al cliente cada vez que un búfer esté listo para que el cliente lo procese. WASAPI admite el almacenamiento en búfer controlado por eventos para los búferes de representación y captura. Tanto las secuencias en modo compartido como las secuencias en modo exclusivo pueden usar el almacenamiento en búfer controlado por eventos. Para obtener un ejemplo de código que usa la marca AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK, vea [Exclusive-Mode Secuencias](exclusive-mode-streams.md).

La marca AUDCLNT \_ STREAMFLAGS NOPERSIST deshabilita la persistencia de la configuración de volumen y exclusión mutua para una sesión que \_ contiene secuencias de representación. De forma predeterminada, el nivel de volumen y el estado muting de una sesión de representación son persistentes en los reinicios de la aplicación. El nivel de volumen y el estado muting de una sesión de captura nunca son persistentes. Para obtener más información sobre la persistencia del volumen de sesión y la configuración de exclusión mutua, vea [Sesiones de audio](audio-sessions.md).

La marca AUDCLNT STREAMFLAGS RATEADJUST permite a una aplicación obtener una referencia a la interfaz \_ \_ [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) que se usa para establecer la frecuencia de muestreo de la secuencia. Para obtener un puntero a esta interace, una aplicación debe inicializar el cliente de audio con esta marca y, a continuación, llamar a [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) especificando el identificador **\_ IID IAudioClockAdjustment.** Para establecer la nueva frecuencia de muestreo, llame [**a IAudioClockAdjustment::SetSampleRate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Esta marca solo es válida para un dispositivo de representación. De lo **contrario, se produce un** error en la llamada a GetService con el código de error AUDCLNT E WRONG ENDPOINT \_ \_ \_ \_ TYPE. La aplicación también debe establecer el *parámetro ShareMode* en AUDCLNT \_ SHAREMODE \_ SHARED durante la llamada [**a Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) **SetSampleRate produce** un error si el cliente de audio no está en modo compartido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioCaptureClient (interfaz)**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




