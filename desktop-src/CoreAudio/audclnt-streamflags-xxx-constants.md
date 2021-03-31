---
description: Especifica las características que un cliente puede asignar a una secuencia de audio durante la inicialización de la secuencia.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: Constantes de AUDCLNT_STREAMFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65faf887c35b4ce1110cecb7d7509eb3dfda1d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153141"
---
# <a name="audclnt_streamflags_xxx-constants"></a>Constantes de AUDCLNT \_ STREAMFLAGS \_ XXX

Especifica las características que un cliente puede asignar a una secuencia de audio durante la inicialización de la secuencia.



| Constante o valor                                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | La secuencia de audio será un miembro de una sesión de audio entre procesos. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ 0x00020000 de \_ bucle invertido STREAMFLAGS**</dt> <dt></dt> </dl>                                                   | La secuencia de audio funcionará en modo de bucle invertido. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK**</dt> <dt>0x00040000</dt> </dl>                                    | El procesamiento del búfer de audio por parte del cliente estará orientado a eventos. Para obtener más información, vea la sección Comentarios. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ nopersist**</dt> <dt>0x00080000</dt> </dl>                                                | La configuración de volumen y silenciar para una sesión de audio no se conservará entre los reinicios de la aplicación. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Esta constante es nueva en Windows 7. La velocidad de muestra de la secuencia se ajusta a la velocidad especificada por una aplicación. Para obtener más información, vea la sección Comentarios. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Una matriz de canales y un convertidor de velocidad de muestra se insertan según sea necesario para realizar la conversión entre el formato sin comprimir proporcionado a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) y el formato de combinación del motor de audio.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ src \_ 0x08000000 \_ calidad predeterminada**</dt> <dt></dt> </dl>                | Cuando se usa con **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**, se usa un convertidor de velocidad de muestra con mejor calidad que la conversión predeterminada pero con un costo de rendimiento mayor. Debe usarse si el audio está pensado en última instancia para ser escuchado por el hombre en lugar de otros escenarios, como bombear el silencio o rellenar un medidor.<br/> |



## <a name="remarks"></a>Observaciones

El método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) y la estructura de parámetros de activación de audio de DirectX usan las constantes de AUDCLNT [**\_ \_ \_**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) \_ STREAMFLAGS \_ xxx.

La \_ \_ marca CROSSPROCESS de STREAMFLAGS de AUDCLNT indica que la sesión de audio de la secuencia es una sesión entre procesos. Una sesión entre procesos puede aceptar secuencias de más de un proceso. Si dos aplicaciones de dos procesos independientes llaman a **IAudioClient:: Initialize** con GUID de sesión idénticos, y ambas aplicaciones establecen la \_ marca AUDCLNT SHAREMODE \_ CROSSPROCESS, el motor de audio asigna sus flujos a la misma sesión entre procesos. Esta marca invalida el comportamiento predeterminado, que consiste en asignar la secuencia a una sesión específica del proceso en lugar de a una sesión entre procesos. El \_ bit de marca CROSSPROCESS de STREAMFLAGS de AUDCLNT \_ es incompatible con el modo exclusivo. Para obtener más información sobre las sesiones entre procesos, vea [sesiones de audio](audio-sessions.md).

La \_ marca de \_ bucle invertido AUDCLNT STREAMFLAGS habilita la grabación de bucle invertido. En la grabación de bucle invertido, el motor de audio copia la secuencia de audio que reproduce un dispositivo de punto de conexión de representación en un búfer de punto de conexión de audio para que un cliente de [WASAPI](wasapi.md) pueda capturar el flujo. Si se establece esta marca, el método **IAudioClient:: Initialize** intenta abrir un búfer de captura en el dispositivo de representación. Esta marca solo es válida para un dispositivo de representación y solo si la llamada **Initialize** establece el parámetro *ShareMode* en AUDCLNT \_ ShareMode \_ Shared. De lo contrario, se producirá un error en la llamada **Initialize** . Si la llamada se realiza correctamente, el cliente puede llamar al método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obtener una interfaz [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) en el dispositivo de representación. Para obtener más información, vea [grabación de bucle invertido](loopback-recording.md).

La \_ marca EVENTCALLBACK de STREAMFLAGS de AUDCLNT \_ habilita el almacenamiento en búfer basado en eventos. Si un cliente establece esta marca en la llamada a **IAudioClient:: Initialize** que Inicializa una secuencia, el cliente debe llamar posteriormente al método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) para proporcionar un identificador de evento para la secuencia. Una vez que se inicia el flujo, el motor de audio señalará el identificador de evento para notificar al cliente cada vez que un búfer esté listo para que lo procese el cliente. WASAPI admite el almacenamiento en búfer basado en eventos para la representación y los búferes de captura. Tanto los flujos en modo compartido como los de modo exclusivo pueden utilizar el almacenamiento en búfer basado en eventos. Para obtener un ejemplo de código que usa la \_ marca EVENTCALLBACK de STREAMFLAGS de AUDCLNT \_ , consulte [flujos de modo exclusivo](exclusive-mode-streams.md).

La \_ marca AUDCLNT STREAMFLAGS \_ nopersist deshabilita la persistencia de los valores Volume y MUTE para una sesión que contiene secuencias de representación. De forma predeterminada, el nivel de volumen y el estado de silencio para una sesión de representación son persistentes en los reinicios de la aplicación. El nivel de volumen y el estado de silencio para una sesión de captura nunca son persistentes. Para obtener más información sobre la persistencia de los valores de configuración de volumen y silencio de sesión, vea [sesiones de audio](audio-sessions.md).

La \_ marca RATEADJUST de STREAMFLAGS de AUDCLNT \_ permite a una aplicación obtener una referencia a la interfaz de [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) que se usa para establecer la velocidad de muestra de la secuencia. Para obtener un puntero a este interfaz, una aplicación debe inicializar el cliente de audio con esta marca y, a continuación, llamar a [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) especificando el identificador de **\_ IAudioClockAdjustment de IID** . Para establecer la nueva frecuencia de muestreo, llame a [**IAudioClockAdjustment:: SetSampleRate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Esta marca solo es válida para un dispositivo de representación. De lo contrario, se producirá un error en la llamada **GetService** con el código de error AUDCLNT \_ E \_ incorrecto \_ \_ . La aplicación también debe establecer el parámetro *ShareMode* en AUDCLNT \_ ShareMode \_ Shared durante la llamada de [**inicialización**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . **SetSampleRate** produce un error si el cliente de audio no está en modo compartido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**Interfaz IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




